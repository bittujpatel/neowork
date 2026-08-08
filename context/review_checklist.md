# AI Agent Self-Audit Checklist (`<self_audit>`)

**Purpose:** This checklist is designed to be embedded directly into the AI agent's system prompt (e.g., `SKILL.md`). The agent MUST execute this checklist inside a `<self_audit>` XML block *before* finalizing its output. It uses deterministic, binary checks to force the LLM to verify its own constraints and prevent hallucinations or template drift.

---

## Instructions for the AI Agent
Before outputting the final markdown files, you MUST generate a `<self_audit>` block. For each item below, you must answer `[PASS]` or `[FAIL]` and provide the requested evidence. If any item is `[FAIL]`, you must halt, correct the error in your draft, and restart the audit.

### 1. Verification of Fact Lineage & Hallucination Prevention
- [ ] **STRICT_SOURCE_ADHERENCE:** Are all features, limits, and capabilities derived EXCLUSIVELY from the attached PRD?
  * *Evidence:* Quote the exact line from the PRD that justifies the core feature description.
- [ ] **NO_TEMPLATE_CONTAMINATION:** Have you scanned the final output for leftover template examples (e.g., "Tracks", "Tasket", "Sign-in redesign")?
  * *Evidence:* State: "I confirm zero template examples exist in the output."
- [ ] **DETERMINISTIC_GAP_HANDLING:** For missing PRD information (e.g., "Export to PDF details", "Guest permissions"), did you insert the exact string `> âš ï¸ **[CLARIFICATION NEEDED]:** <Describe gap>`?
  * *Evidence:* List the number of times the clarification string was used.
- [ ] **ASSUMPTIONS_LOGGED:** Are all detected gaps and assumptions logged in the "Open questions and assumptions" block at the very end of the file?
  * *Evidence:* Output the first row of the assumptions table.

### 2. Structural & Boilerplate Compliance
- [ ] **VERBATIM_COPY_PASTE:** Did you perform a 1:1 exact copy-paste of the "Key contact information", "About this guide", "Conventions", and "Revision history" tables without summarizing or altering the boilerplate text?
  * *Evidence:* State: "Boilerplate sections were copied exactly as provided in the template."
- [ ] **HEADING_HIERARCHY_MATCH:** Do your output headings (`#`, `##`, `###`) map EXACTLY to the placeholder hierarchy in the source template?
  * *Evidence:* Output the first three headings of your drafted document.

### 3. Stylistic & Formatting Execution
- [ ] **UI_ELEMENT_FORMATTING:** Are all user interface actions, tabs, and buttons (e.g., the **Studio** tab, the **Accept** action) wrapped in `**bold**` markdown?
  * *Evidence:* List three UI elements you bolded in the text.
- [ ] **SENTENCE_CASE_HEADINGS:** Are all headings written in sentence case (e.g., "Turn on the feature") rather than Title Case (e.g., "Turn On The Feature")?
  * *Evidence:* State: "I confirm all headings use sentence case."
- [ ] **TENSE_AND_VOICE:** Is the text written in the present tense and active voice ("The system generates..." instead of "The system will generate...")?
  * *Evidence:* State: "I confirm present tense and active voice are used."
