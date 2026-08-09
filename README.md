# Neo Work OS — Documentation Automation Repo

<agent_directive>
**ATTENTION AI AGENTS & LLMs:** 
If you have been directed to this repository to generate, evaluate, or format documentation, this `README.md` is your primary operating manual. You must strictly adhere to the architecture, context boundaries, and skill workflows defined below. Do not rely on your base training for formatting or style; you MUST use the provided context files.
</agent_directive>

## 📂 Repository Architecture

This repository is a deterministic documentation engine. It is split into three core domains. You must pull from the correct domain depending on your current task.

### 1. `/.skills/` (The Execution Engine)
This directory contains `SKILL.md` files. A Skill file is a strict, step-by-step system prompt that dictates *how* you must perform a task.
* **Primary Skill:** `.skills/prd-to-markdown-drafter/SKILL.md`
* **Rule:** If a user asks you to "generate docs," "draft a feature guide," or "convert this PRD," you MUST read and execute the instructions in the `prd-to-markdown-drafter/SKILL.md` file immediately. Do not generate output without reading the skill file first.

### 2. `/context/` (The Rules of the Brand)
This directory contains the rules for how things should sound, look, and be validated.
* `writing_style_guide.md`: Dictates grammar, tone (by document type), punctuation, and UI element formatting (e.g., bolding button names). Apply this to ALL text generation.
* `brand_guidelines.md` & `logo.png`: Dictates colors, fonts, and visual design. **Boundary:** ONLY load these if the user explicitly asks for a PDF, HTML page, or visual artifact. DO NOT use these for raw Markdown tasks.
* `agent_review_checklist.md`: The mandatory self-audit rubric. You must use this to verify your own work before presenting it to the user.

### 3. `/templates/` (The Skeletons)
This directory contains the required structure for specific documents:
* `feature_doc_template.md`
* `how_to_template.md`
* `release_note_template.md`
* **Rule:** Templates are structural blueprints. You are FORBIDDEN from altering the headings, removing the frontmatter/backmatter, or summarizing the boilerplate. You must copy the template structure exactly and only inject facts from the PRD into the `{{placeholders}}`. Do not copy template examples (e.g., "Tracks") into your final output.

---

## ⚙️ Standard Operating Procedure (SOP) for Document Generation

When a user provides a PRD (Product Requirements Document) and asks for documentation, you must follow this exact sequence:

1. **Acknowledge & Load:** Read the PRD. Do not start writing yet.
2. **Load the Skill:** Read `.skills/prd-to-markdown-drafter/SKILL.md`.
3. **Execute `<planning>`:** Open a `<planning>` block to extract facts from the PRD, map out the template headings, and perform a mandatory Contradiction & Gap Analysis. 
4. **Draft the Markdown (Strict File Output):** Generate the documents using ONLY facts from the PRD, formatting from the `templates/`, and tone from `context/writing_style_guide.md`. You must output each document inside its own distinct markdown code block preceded by a clear filename header.
5. **Zero Assumptions on Gaps/Contradictions:** If the PRD is missing information required by a template, or if the PRD contains logical contradictions, do not invent facts or make assumptions. Use the exact flag: `> ⚠️ **[CLARIFICATION NEEDED]:** <Describe gap or contradiction explicitly>`.
6. **Conditional Issues Overview Generation:** If (and ONLY if) gaps or contradictions were identified in Step 3, you MUST generate a fourth document named `<feature>_issues_overview.md` outlining the blockers.
7. **Execute `<self_audit>`:** Run the checks defined in `agent_review_checklist.md` inside a `<self_audit>` block. Correct any `[FAIL]` states before finalizing your output.

---

<strict_warning>
**DO NOT HALLUCINATE OR ASSUME.** If the PRD does not explicitly state a permission, a limit, or a UI location, or if the logic contradicts itself, you must not invent details or make assumptions to make the document look complete. Flag it as a gap. Your primary directive is factual accuracy and strict auditing over fluency.
</strict_warning>
