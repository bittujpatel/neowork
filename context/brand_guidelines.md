# Brand Guidelines — Neo Work OS

**Purpose:** This document defines the Neo brand identity, voice, typography, color, and visual system that every generated document must follow. It is loaded as context by the doc-suite generator so that a feature guide, how-to guide, and release note produced from *any* PRD all look and sound like one product.

**How agents should use this file:** Treat the tokens below (colors, fonts, radii, shadows, gradients) as the single source of truth. Apply them when rendering or styling any output (HTML, PDF, DOCX theming, slides). Text-only Markdown outputs must still follow the **voice, tone, naming, and callout** rules in sections 2–8.

> **Source:** Visual tokens captured from **neo.work** using the Peek design-inspection extension. Brand is white-dominant with a blue accent and a signature blue gradient.

---

## 0. Brand assets

### Logo

- **Primary logo file:** `context/logo.png`
  *Place the Neo logo here. Agents must reference this path when a logo is needed (document headers, cover pages, footers, slide masters).*
- **Placeholder token:** `{{BRAND_LOGO}}` → resolves to `context/logo.png`.

**Logo usage rules**

- Maintain clear space around the logo equal to at least the logo's cap height on all sides.
- Do not stretch, recolor, rotate, or add effects to the logo.
- On white/light backgrounds use the standard logo; on dark or gradient backgrounds use a white/knockout version if available.
- Minimum size: keep the logo legible; never render below 24px height in digital docs.

> **Note:** If `context/logo.png` is missing, fall back to the text wordmark **Neo** set in Inter, weight 600.

---

## 1. Who we are

- **Company:** Neo Work OS.
- **Product family:** Tasket (work management), Friday (AI assistant), Studio (documents), Drive (files), Scribe (meetings).
- **What we make:** An AI-native, integrated suite of work products.

**Copyright / confidentiality line (formal documents):**
`© 2026 Neo Work OS. Confidential and Proprietary.`

---

## 2. Color system

Neo is **white-dominant (94%)** with a **blue accent** and a small amount of near-black for text. Blue is the primary brand color and the basis of all gradients.

### Core tokens

| Token | Hex | Role |
|---|---|---|
| `--color-white` | `#ffffff` | Dominant background (94%). Default page/surface. |
| `--color-ink` | `#1a1814` | Primary body text (warm near-black). |
| `--color-black` | `#000000` | Headlines, high-contrast text, borders, gradient depth. |
| `--color-royal-blue` | `#0a7aff` | **Primary brand blue.** Accent, links, primary CTAs. |
| `--color-medium-blue` | `#0047c7` | Deep blue. Gradient end-stop, hover/active states. |

### Usage ratio (keep the brand feeling airy)

- **~94% white** surfaces and negative space.
- **~3% ink/black** for text and structure.
- **~3% blue** for accents, links, and CTAs — used sparingly for emphasis, never as a full background wash except in gradient hero areas.

### Semantic mapping

| Purpose | Token |
|---|---|
| Page background | `--color-white` |
| Body text | `--color-ink` |
| Headings | `--color-black` |
| Links / accent | `--color-royal-blue` |
| Primary CTA background | `--color-royal-blue` (or brand gradient) |
| Primary CTA text | `--color-white` |
| Borders / dividers | `--color-black` at low opacity, or `--color-ink` |

---

## 3. Gradients

Neo's **signature gradient blends a neutral grey into the accent blue** (`#0a7aff`). The grey base keeps the brand calm and airy, and the blue accent (the 3% accent color) glows through to create the distinctive Neo look. Use gradients for hero areas, CTA fills, and accent surfaces — not behind body text.

### Grey stop token (tune to taste)

The Peek capture did not report an exact grey for the fade, so this token is defined here and can be adjusted. Default is a soft neutral grey.

```css
--color-grey: #8a8f98;  /* signature-gradient grey stop — adjust to match neo.work exactly */
```

### Primary brand gradient (grey → blue)

```css
--gradient-brand: linear-gradient(135deg, #8a8f98 0%, #0a7aff 100%);
```

- Use for: primary CTAs, hero banners, cover-page accents, callout highlights.
- Direction: 135° (top-left → bottom-right) by default. A radial variant may center on focal points.

### Radial accent variant (grey → blue)

```css
--gradient-brand-radial: radial-gradient(85% 75% at 50% 42%, #8a8f98 0%, #0a7aff 100%);
```

- The blue focal point sits toward the centre with grey falling off to the edges — matching the Neo hero look.

### Deep-blue variant (optional)

For places that need a fuller blue emphasis, blend the two brand blues instead:

```css
--gradient-brand-blue: linear-gradient(135deg, #0a7aff 0%, #0047c7 100%);
```

> **Important:** The original Peek capture read the hero radial as pure black (`#000000` stops) — an overlay artifact. The **true signature gradient is grey → blue** (`--color-grey` → `#0a7aff`). Use `--gradient-brand` as the default. Set `--color-grey` to the exact neo.work value once you have it.

---

## 4. Typography

**Font family:** **Inter** (single family across the brand). Load Inter for all headings, body, and UI text. Fallback stack:

```css
font-family: "Inter", -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
```

- **Scale type:** Minor Third (~1.2 ratio).
- **Size range:** 15–66px.
- **Weights in use:** 400 (regular), 500 (medium), 600 (semibold).
- Headings use **tight negative letter-spacing**; body uses normal spacing.

### Type scale (from neo.work)

| Token | Use | Font | Size | Weight | Line height | Letter spacing |
|---|---|---|---|---|---|---|
| `large-title` | Hero / cover title | Inter | 66px | 400 | 69.3px | −2.64px |
| `h1` | Page title | Inter | 46px | 400 | 49.68px | −1.84px |
| `h2` | Section heading | Inter | 34px | 400 | 37.4px | normal |
| `body-lg` | Lead paragraph | Inter | 30px | 400 | 48.75px | normal |
| `body` | Body text | Inter | 24px | 400 | 39px | normal |
| `body-sm` | Secondary body | Inter | 22px | 400 | 35.75px | normal |
| `body-xs` | Dense body | Inter | 20px | 400 | 32.5px | normal |
| `overline` | Eyebrow / header label | Inter | 16px | 400 | 24px | normal |
| `button` | CTA label | Inter | 15px | 600 | 24px | normal |
| `caption` | Small body / meta | Inter | 15px | 500 | 24.375px | normal |
| `button-alt` | Secondary button | Inter | 15px | 400 | 15px | normal |

**Rules**

- One family only — **Inter**. Never mix in a second typeface.
- Large display sizes (46px+) use the tight negative tracking above; do not apply it to body text.
- For print/document contexts, scale the ratio down proportionally but keep the same steps and weights.
- Headings in **sentence case**, not Title Case.

---

## 5. Shape, radius, and elevation

### Corner radius

| Token | Value | Use |
|---|---|---|
| `--radius-md` | `16px` | Cards, surfaces, inputs. |
| `--radius-lg` | `24px` | Large panels, hero cards, modals. |
| `--radius-pill` | `9999px` | Buttons, pills, tags (fully rounded). |

Neo favors **contrasting shapes**: soft 16–24px surfaces paired with fully rounded (`9999px`) pill CTAs.

### Shadow / elevation

```css
--shadow-high: 0px 25px 50px -12px rgba(0, 0, 0, 0.1);
```

- Use `--shadow-high` for elevated cards, popovers, and hero elements.
- Keep shadows soft and low-opacity; the brand reads clean and airy, not heavy.

---

## 6. Buttons & CTAs

- **Primary CTA:** `--gradient-brand` (or `--color-royal-blue`) background, `--color-white` text, `--radius-pill`, label in `button` type (Inter 15/600).
- **Secondary CTA:** white or `--color-ink` background, blue or ink text, 1px border, `--radius-pill`.
- **CTA colors available:** `#000000`, `#1a1814`, `#ffffff`, `#0a7aff`.
- Keep CTA labels short and action-led ("Get started", "Turn on Tracks").

---

## 7. Voice — how we always sound

Voice is constant; only *tone* flexes by audience (section 8).

- **Clear over clever.** Plain words win.
- **Human, not robotic.** Second person ("you"), no corporate filler.
- **Confident, not boastful.** State what the product does; skip "revolutionary," "world-class."
- **Respectful of the reader's time.** Lead with the point.
- **Benefit-first for users, precise for tasks.**

---

## 8. Tone by document type

| Document | Reader | Tone |
|---|---|---|
| **Feature guide** | First-time user | Explanatory, reassuring. Build a mental model first. |
| **How-to guide** | User with a task in hand | Direct, imperative, step-by-step. |
| **Release note** | Existing user scanning changes | Brief, benefit-led. Announce outcome; hide mechanism. |

---

## 9. Naming and terminology

- **Product/feature names are proper nouns:** **Tasket**, **Friday**, **Studio**, **Tracks**. Never lowercase or mis-pluralize.
- **Capitalize in-product objects/states as the UI does:** **Track**, **Not started**, **In Progress**, **Done**; **Open**, **Completed**, **Discarded**.
- **UI actions are bold, matching the label exactly:** the **Tracks** tab, the **Mark Done** action.
- **One term per concept** within a document — no drift (e.g., don't swap "lane"/"column"/"track" undefined).

---

## 10. Preferred vs. avoided words

| Prefer | Avoid |
|---|---|
| **Select** | click, tap, press |
| **Turn on / turn off**, **enable** | activate/deactivate (inconsistently) |
| **Sign in** | log in / login (verb) |
| use, help, start | leverage, utilize, empower |
| concrete benefits | "seamless," "world-class," "revolutionary" |

- **No internal engineering jargon** in user-facing text (e.g., "write queue," "reconciliation," "LWW"). Translate to what the user experiences.

---

## 11. Callout conventions

| Callout | Use it for |
|---|---|
| **Note** | Helpful info or a pointer to related material. |
| **Important** | Info essential to a task or concept. |
| **Warning** | Irreversible data loss or major impact. |

Format as a blockquote with a bold label: `> **Warning:** ...`

---

## 12. Formatting brand rules

- **Headings:** Sentence case, not Title Case.
- **Bold:** UI elements and action names only.
- **Italic:** Introducing/emphasizing a new term, sparingly.
- **Lists:** Parallel structure; use for steps and parallel items.
- **Tables:** For reference material (permissions, terms).
- **One idea per sentence.**

---

## 13. Accessibility

- Global audience: avoid idioms, slang, region-specific references.
- People-first, gender-neutral language ("they" or second person).
- Never rely on color alone (blue links must also be underlined or labeled).
- Ensure text/background contrast meets WCAG AA (white bg + `--color-ink`/`--color-black` passes; avoid low-contrast blue-on-white for small body text).

---

## 14. Draft-status honesty

When generating from a **working-draft** PRD, say so and note it will be updated when final. Never present assumptions as confirmed fact.

> **Note:** This document is based on a working-draft specification and will be updated once the specification is final.

---

## Appendix — Design token quick reference

```css
:root {
  /* Colors */
  --color-white:       #ffffff;
  --color-ink:         #1a1814;
  --color-black:       #000000;
  --color-royal-blue:  #0a7aff;  /* primary brand blue / accent */
  --color-medium-blue: #0047c7;
  --color-grey:        #8a8f98;  /* signature-gradient grey stop — tune to neo.work */

  /* Gradients */
  --gradient-brand:        linear-gradient(135deg, #8a8f98 0%, #0a7aff 100%);       /* signature grey -> blue */
  --gradient-brand-radial: radial-gradient(85% 75% at 50% 42%, #8a8f98 0%, #0a7aff 100%);
  --gradient-brand-blue:   linear-gradient(135deg, #0a7aff 0%, #0047c7 100%);       /* optional fuller blue */

  /* Typography */
  --font-family: "Inter", -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;

  /* Radius */
  --radius-md:   16px;
  --radius-lg:   24px;
  --radius-pill: 9999px;

  /* Elevation */
  --shadow-high: 0px 25px 50px -12px rgba(0, 0, 0, 0.1);

  /* Assets */
  --brand-logo: url("context/logo.png");
}
```

