# Design System Specification: The Editorial Guardian

## 1. Overview & Creative North Star
**Creative North Star: "The Curated Sanctuary"**

This design system rejects the clinical, cold aesthetic often associated with insurance. Instead, it positions itself as a "Curated Sanctuary"—a digital space that feels like a premium French lifestyle magazine mixed with the precision of a high-end private bank. 

We move beyond the "template" look by embracing **Intentional Asymmetry** and **Tonal Depth**. The goal is to provide a senior audience (55+) with a sense of calm authority. We achieve this through a "High-End Editorial" approach: expansive white space, over-scaled serif typography, and a rejection of traditional UI "boxes" in favor of layered, organic surfaces. This is not just a tool; it is a reassuring consultation.

---

## 2. Colors & Surface Philosophy

### The "No-Line" Rule
To maintain a premium, seamless feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through tonal shifts. For instance, a `surface-container-low` section should sit directly against a `surface` background. This forces the eye to recognize structure through mass and color rather than artificial lines.

### Surface Hierarchy & Nesting
Treat the UI as a physical desk of fine stationery. Use the `surface-container` tiers to create depth:
- **`surface-container-lowest` (#ffffff):** Reserved for the most important interactive cards or floating elements.
- **`surface` (#f6faff):** The base canvas for the entire application.
- **`surface-container-high` (#e2e9f1):** Used for "recessed" areas like sidebars or secondary content blocks.

### The "Glass & Gradient" Rule
For floating navigation or modals, utilize **Glassmorphism**. Use a semi-transparent `surface` color with a `backdrop-blur` (20px–40px). 
**Signature Textures:** For primary CTAs and Hero backgrounds, do not use flat colors. Apply a subtle linear gradient (135°) from `primary` (#001b12) to `primary_container` (#003224) to add a "soulful" depth that feels expensive and intentional.

---

## 3. Typography: The Editorial Voice

We prioritize legibility without sacrificing sophistication. By pairing **Noto Serif** with **Inter**, we bridge the gap between traditional French heritage and modern fintech precision.

- **Display & Headlines (Noto Serif):** Use `display-lg` to `headline-sm` for all major section entries. The Serif's high contrast communicates authority and "The Guardian" personality. 
- **Body & Labels (Inter):** All functional text uses Inter. For the 55+ demographic, the `body-lg` (1rem/16px) is our absolute minimum for standard reading.
- **Hierarchy as Identity:** Use extreme scale differences. A `display-md` headline paired with a `body-lg` sub-header creates an editorial look that guides the user’s eye effortlessly.

---

## 4. Elevation & Depth

### The Layering Principle
Hierarchy is achieved through "Tonal Stacking." 
*   **Level 0:** `surface` (The Base)
*   **Level 1:** `surface-container-low` (The Section)
*   **Level 2:** `surface-container-lowest` (The Card)

### Ambient Shadows
When a card must float (e.g., a "Recommended" insurance plan), use an **Ambient Shadow**:
- **Color:** `on-surface` (#151c22) at 6% opacity.
- **Blur:** 32px to 48px.
- **Spread:** -4px.
This mimics natural light falling on thick paper, avoiding the "cheap" look of heavy, dark shadows.

### The "Ghost Border" Fallback
If a border is required for accessibility (e.g., in high-contrast mode), use a **Ghost Border**: `outline-variant` (#c5c6ce) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons: The Signature Action
- **Primary:** A gradient from `primary` to `primary_container`. High-contrast `on_primary` (#ffffff) text. Corner radius: `md` (0.375rem) for a bespoke, tailored look.
- **Tertiary (The "Underline" Action):** No box. Use `title-sm` in `primary` with a 2px underline offset by 4px.

### Cards: The Information Vessel
- **Rule:** No borders. Use `surface-container-lowest` on a `surface-container-low` background. 
- **Spacing:** Generous internal padding (2rem/32px) to ensure seniors never feel "crowded" by the data.

### Input Fields: Sophisticated Input
- **State:** Instead of a heavy border, active inputs should use a subtle background shift to `surface-container-highest` and a `tertiary` (#735c00) "Gold" indicator line (2px) at the bottom.

### Comparison Chips
- Use `secondary_container` (#cadaff) with `on_secondary_container` text. These should have a `full` (9999px) radius to contrast against the architectural squareness of the cards.

---

## 6. Do’s and Don’ts

### Do:
- **Do** use `tertiary` (#735c00 / Gold) sparingly. It is a "jewelry" accent for awards, high-tier ratings, or final CTA highlights.
- **Do** lean into white space. If you think there is enough space, add 20% more.
- **Do** use `notoSerif` for numbers in insurance premiums to make the costs feel more "stately" and less aggressive.

### Don’t:
- **Don’t** use pure black (#000000). Use `on_surface` (#151c22) for all "black" text to maintain a softer, premium feel.
- **Don’t** use standard "Success Green." Use the `primary` Deep Emerald variants for a more sophisticated health-reassurance tone.
- **Don’t** stack more than two cards horizontally. For a 55+ audience, vertical scanning is more reliable and feels less overwhelming.