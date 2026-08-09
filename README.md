# Neo Work OS — Documentation Automation Repo[span_1](start_span)[span_1](end_span)

<agent_directive>
**ATTENTION AI AGENTS & LLMs:** 
If you have been directed to this repository to generate, evaluate, or format documentation, this `README.md` is your primary operating manual[span_2](start_span)[span_2](end_span). You must strictly adhere to the architecture, context boundaries, and skill workflows defined below[span_3](start_span)[span_3](end_span). Do not rely on your base training for formatting or style; you MUST use the provided context files[span_4](start_span)[span_4](end_span).
</agent_directive>

## 📂 Repository Architecture[span_5](start_span)[span_5](end_span)

This repository is a deterministic documentation engine[span_6](start_span)[span_6](end_span). It is split into three core domains[span_7](start_span)[span_7](end_span). You must pull from the correct domain depending on your current task[span_8](start_span)[span_8](end_span).

### 1. `/.skills/` (The Execution Engine)[span_9](start_span)[span_9](end_span)
This directory contains `SKILL.md` files[span_10](start_span)[span_10](end_span). A Skill file is a strict, step-by-step system prompt that dictates *how* you must perform a task[span_11](start_span)[span_11](end_span).
* **Primary Skill:** `.skills/prd-to-markdown-drafter/SKILL.md`[span_12](start_span)[span_12](end_span)
* **Rule:** If a user asks you to "generate docs," "draft a feature guide," or "convert this PRD," you MUST read and execute the instructions in the `prd-to-markdown-drafter/SKILL.md` file immediately[span_13](start_span)[span_13](end_span). Do not generate output without reading the skill file first[span_14](start_span)[span_14](end_span).

### 2. `/context/` (The Rules of the Brand)[span_15](start_span)[span_15](end_span)
This directory contains the rules for how things should sound, look, and be validated[span_16](start_span)[span_16](end_span).
* `writing_style_guide.md`: Dictates grammar, tone (by document type), punctuation, and UI element formatting (e.g., bolding button names)[span_17](start_span)[span_17](end_span). Apply this to ALL text generation[span_18](start_span)[span_18](end_span).
* `brand_guidelines.md` & `logo.png`: Dictates colors, fonts, and visual design[span_19](start_span)[span_19](end_span). **Boundary:** ONLY load these if the user explicitly asks for a PDF, HTML page, or visual artifact[span_20](start_span)[span_20](end_span). DO NOT use these for raw Markdown tasks[span_21](start_span)[span_21](end_span).
* `agent_review_checklist.md`: The mandatory self-audit rubric[span_22](start_span)[span_22](end_span). You must use this to verify your own work before presenting it to the user[span_23](start_span)[span_23](end_span).

### 3. `/templates/` (The Skeletons)[span_24](start_span)[span_24](end_span)
This directory contains the required structure for specific documents[span_25](start_span)[span_25](end_span):
* `feature_doc_template.md`[span_26](start_span)[span_26](end_span)
* `how_to_template.md`[span_27](start_span)[span_27](end_span)
* `release_note_template.md`[span_28](start_span)[span_28](end_span)
* **Rule:** Templates are structural blueprints[span_29](start_span)[span_29](end_span). You are FORBIDDEN from altering the headings, removing the frontmatter/backmatter, or summarizing the boilerplate[span_30](start_span)[span_30](end_span). You must copy the template structure exactly and only inject facts from the PRD into the `{{placeholders}}`[span_31](start_span)[span_31](end_span). Do not copy template examples (e.g., "Tracks") into your final output[span_32](start_span)[span_32](end_span).

---

## ⚙️ Standard Operating Procedure (SOP) for Document Generation[span_33](start_span)[span_33](end_span)

When a user provides a PRD (Product Requirements Document) and asks for documentation, you must follow this exact sequence[span_34](start_span)[span_34](end_span):

1. **Acknowledge & Load:** Read the PRD. Do not start writing yet[span_35](start_span)[span_35](end_span).
2. **Load the Skill:** Read `.skills/prd-to-markdown-drafter/SKILL.md`[span_36](start_span)[span_36](end_span).
3. **Execute `<planning>`:** Open a `<planning>` block to extract facts from the PRD, map out the template headings, and perform a mandatory Contradiction & Gap Analysis[span_37](start_span)[span_37](end_span). 
4. **Draft the Markdown (Strict File Output):** Generate the documents using ONLY facts from the PRD, formatting from the `templates/`, and tone from `context/writing_style_guide.md`[span_38](start_span)[span_38](end_span). You must output each document inside its own distinct markdown code block preceded by a clear filename header.
5. **Zero Assumptions on Gaps/Contradictions:** If the PRD is missing information required by a template, or if the PRD contains logical contradictions, do not invent facts or make assumptions[span_39](start_span)[span_39](end_span). Use the exact flag: `> ⚠️ **[CLARIFICATION NEEDED]:** <Describe gap or contradiction explicitly>`[span_40](start_span)[span_40](end_span).
6. **Conditional Issues Overview Generation:** If (and ONLY if) gaps or contradictions were identified in Step 3, you MUST generate a fourth document named `<feature>_issues_overview.md` outlining the blockers.
7. **Execute `<self_audit>`:** Run the checks defined in `agent_review_checklist.md` inside a `<self_audit>` block[span_41](start_span)[span_41](end_span). Correct any `[FAIL]` states before finalizing your output[span_42](start_span)[span_42](end_span).

---

<strict_warning>
**DO NOT HALLUCINATE OR ASSUME.** If the PRD does not explicitly state a permission, a limit, or a UI location, or if the logic contradicts itself, you must not invent details or make assumptions to make the document look complete[span_43](start_span)[span_43](end_span). Flag it as a gap[span_44](start_span)[span_44](end_span). Your primary directive is factual accuracy and strict auditing over fluency[span_45](start_span)[span_45](end_span).
</strict_warning>
