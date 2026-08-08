# Writing Style Guide — Neo Work OS

**Purpose:** This guide defines the mechanical writing rules — grammar, structure, punctuation, and formatting — for every document the doc-suite generator produces. It is loaded as context alongside `brand_guidelines.md`.

**How this file relates to the others:**

- `brand_guidelines.md` → identity, voice, tone, color, typography, logo.
- **`writing_style_guide.md` (this file)** → how to actually write the sentences and structure the pages.
- `review_checklist.md` → the pass/fail checks before a doc is done.

**Baseline:** When this guide is silent on a point, follow the **Microsoft Writing Style Guide (MSTP)**, then the Chicago Manual of Style.

---

## 1. Core principles

1. **Write for the reader's task, not the system's design.** Say what the user does and gets.
2. **Front-load.** Put the most important information first — in the doc, the section, and the sentence.
3. **One idea per sentence.** Short sentences beat clever ones.
4. **Be consistent.** Same term, same capitalization, same structure, every time.
5. **Cut what doesn't help.** No filler, no throat-clearing, no restating the obvious.

---

## 2. Grammar and mechanics

### Person and voice

- **Second person** ("you"), **active voice**, **present tense** by default.
  - Do: "You can start a task on several tracks."
  - Don't: "Tasks may be started by the user."
- Use **imperative mood** for instructions: "Open the project," "Select **Add track**."

### Tense

- Describe what happens **now**, in present tense, even for results: "The task moves to the Done section," not "The task will move…".

### Articles and completeness

- Write complete sentences in body text. Steps may use imperative fragments but must be grammatically clean.

### Contractions

- Use common contractions ("you're," "it's," "don't") to stay human — but not in warnings, where clarity is paramount.

---

## 3. Capitalization

- **Sentence case for all headings** ("Turn on Tracks for a project"), never Title Case.
- **Product and feature names** are capitalized: **Tasket**, **Friday**, **Studio**, **Tracks**.
- **In-product states and objects** match the UI: **Not started**, **In Progress**, **Done**; **Open**, **Completed**, **Discarded**.
- **UI element and action names** match the interface exactly and are **bold**: the **Tracks** tab, the **Mark Done** action.
- Do **not** capitalize generic nouns (project, task, member) unless they begin a sentence or are a defined product term.

---

## 4. Punctuation

- **Oxford comma:** always ("spec, design, and QA").
- **En dash (–):** for a strong break or aside. No spaces in print style, or consistent spaced style — pick one and keep it. *(Default: spaced en dash.)*
- **Colons:** to introduce a list or explanation. The lead-in should be a complete clause.
- **Periods in lists:** full sentences get periods; short fragments (three words or fewer) do not — but be consistent within a list.
- **No exclamation points** in user documentation.
- **Ampersands (&):** avoid in body text; spell out "and." Fine in table headers if space-constrained.

---

## 5. Numbers

- Spell out **zero through nine**; use numerals for **10 and above**.
- Always use numerals for: UI values, versions, measurements, and anything the user must match exactly ("up to 10 assignees").
- Use numerals in **steps and counters** ("Step 3", "3 out of 8").
- Percentages: use the numeral and symbol ("94%").

---

## 6. Lists

- **Numbered lists** for sequential steps (order matters).
- **Bulleted lists** for non-sequential, parallel items.
- Keep items **grammatically parallel** — all start with a verb, or all are noun phrases.
- **One action per step.** If a step has "and then," split it.
- Introduce a list with a lead-in sentence ending in a colon.
- Aim for **no more than 7–9 steps** per procedure; break longer tasks into stages.

---

## 7. Procedures (how-to writing)

Every procedure follows this shape:

1. **Task heading** — imperative, task-based ("Create a track").
2. **One-line context** — why or when you'd do this.
3. **Prerequisites** — only if specific to that task.
4. **Numbered steps** — imperative, one action each. Bold the UI targets.
5. **Result** — a short line stating what the user should see.
6. **Note / Important / Warning** — only if genuinely needed.

**Step-writing rules**

- Start each step with the action verb, not the location, when possible: "Select **Add track**," not "In the panel, there is an option to…".
- State **where** before **what** if location matters: "On the **Tracks** tab, select…".
- Describe the **result of a step** only when it's not obvious or when the next step depends on it.

---

## 8. Word choice

### Preferred verbs (UI actions)

| Use | Not |
|---|---|
| **Select** | click, tap, press, choose |
| **Enter** (text) | type, input, key in |
| **Open** | navigate to, go into |
| **Turn on / turn off** | activate, deactivate, toggle |
| **Sign in / sign out** | log in, log out |

### Avoid

- **Corporate filler:** leverage, utilize, empower, seamless, robust, world-class.
- **Engineering jargon in user text:** "write queue," "reconciliation," "idempotent," "LWW." Translate to plain outcomes ("your changes sync when you reconnect").
- **Vague pointers:** "simply," "just," "easily" (they can feel dismissive), and "obviously."
- **Latin abbreviations** in body text: use "for example" (not e.g.), "that is" (not i.e.), "and so on" (not etc.) — abbreviations are fine in tables.
- **Directional-only references:** name the element, don't say "the button on the right."

---

## 9. Cross-references and links

- Refer to documents by their real title in italics or as a link: *Tracks how-to guide*.
- Link text should describe the destination ("see [Turn on Tracks](#…)"), never "click here."
- Keep in-document anchors lowercase and hyphenated.

---

## 10. Callouts

Use only these three, formatted as a bold-labelled blockquote:

- `> **Note:** …` — helpful, non-critical info or a pointer.
- `> **Important:** …` — essential to completing a task or understanding a concept.
- `> **Warning:** …` — risk of irreversible loss or major impact.

Rules: keep them short, one idea each, and don't stack multiple callouts back-to-back. A **Warning** is reserved for genuinely destructive, unrecoverable actions (e.g., deleting a track).

---

## 11. Tables

- Use for reference material: permissions, terminology, who-can-do-what, options.
- Give every table a clear header row.
- Keep cell text terse; full sentences belong in body copy.
- Left-align text columns; keep parallel phrasing down each column.

---

## 12. Accessibility in writing

- Don't convey meaning by color or position alone.
- Write descriptive link text and meaningful headings (they double as navigation).
- Expand an acronym on first use: "Microsoft Writing Style Guide (MSTP)."
- Keep language simple for a global, translation-bound audience: short sentences, common words, no idioms.

---

## 13. Handling draft / uncertain source material

- When the PRD is a **working draft**, state it and note the doc will be updated when the spec is final.
- **Never present an assumption as confirmed fact.** If a behavior is assumed, phrase it as documented behavior but log the assumption for the clarifications list.
- Where the source contradicts itself, follow the assumption recorded in the project's clarifications table and stay consistent across all three documents.

> **Note:** This guide is based on a working-draft process and will be refined as the doc suite matures.

---

## 14. Quick do / don't reference

| Do | Don't |
|---|---|
| "Select **Mark Done**." | "Click on the Mark Done button." |
| "You can work offline." | "Offline capability is supported." |
| "The task moves to Done." | "The task will be moved to the Done state by the system." |
| "For example, spec and design." | "e.g. spec & design." |
| Sentence-case heading | Title-Case Heading |
| "up to 10 assignees" | "up to ten assignees" (UI value) |

