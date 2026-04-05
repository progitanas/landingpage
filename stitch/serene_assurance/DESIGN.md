# Design System: Editorial Assurance

## 1. Overview & Creative North Star: "The Digital Concierge"
This design system moves away from the chaotic, high-density layout typical of insurance tools. Our Creative North Star is **"The Digital Concierge."** We are creating an experience that feels like a private consultation in a quiet, sunlit office—not a spreadsheet.

To break the "template" look, we utilize **Editorial Asymmetry**. Instead of centering everything, we use generous, intentional whitespace and off-center typography to guide the eye. By pairing high-contrast typography scales with a "soft-touch" interface, we ensure the experience is senior-friendly (legible and calm) while remaining modern and high-end.

---

## 2. Colors & Surface Philosophy
The palette is built on a foundation of stability (`primary`) and vitality (`secondary`), accented by warmth (`tertiary`).

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Traditional "boxed" layouts create visual noise that exhausts senior users. Boundaries must be defined solely through background color shifts.
*   **The Transition:** Use a transition from `surface` to `surface-container-low` to signal a new content area.
*   **Signature Textures:** Use subtle gradients for Hero sections, transitioning from `primary` (#00425e) to `primary_container` (#005b7f). This adds a "soulful" depth that flat color cannot achieve.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine paper. 
*   **Base:** `surface` (#f7f9fb)
*   **Sections:** `surface-container-low` (#f2f4f6)
*   **Interaction Cards:** `surface-container-lowest` (#ffffff)
By nesting a `lowest` (white) card inside a `low` (off-white) section, you create a natural lift that feels premium and intentional.

### The "Glass & Gradient" Rule
For floating elements (like a sticky "Save Quote" bar), use **Glassmorphism**. Apply a semi-transparent `surface` color with a 12px-16px backdrop-blur. This ensures the insurance process feels "immersive" and fluid, rather than fragmented.

---

## 3. Typography: The Editorial Voice
We use a "High-Contrast Pairing" to establish authority and utility.

*   **The Authority (Serif):** `newsreader`. Used for `display` and `headline` tiers. This serif face conveys the "Trustworthy" nature of a legacy insurance firm. The large scale (`display-lg` at 3.5rem) ensures effortless readability for seniors.
*   **The Utility (Sans-Serif):** `manrope`. Used for `title`, `body`, and `label`. It is a clean, modern geometric sans that remains legible at smaller scales for UI metadata.

**Pro-Tip:** Always use `on_surface_variant` (#40484e) for body text to reduce harsh contrast against pure white, which can be taxing for aging eyes.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are forbidden unless an element is truly "floating" (e.g., a modal).

*   **Layering Principle:** Stacking tiers (e.g., `surface_container` on top of `surface`) creates depth through chroma rather than shadow.
*   **Ambient Shadows:** If a floating effect is required, use a shadow with a 32px-48px blur at 6% opacity, tinted with `primary` (#00425e). This mimics natural light.
*   **The "Ghost Border":** If accessibility requires a container edge, use `outline_variant` at 15% opacity. Never use 100% opaque lines.

---

## 5. Components: Tactile & Spacious

### Buttons: The "Confidence" Component
*   **Primary:** Uses `primary` (#00425e) with `on_primary` (#ffffff). Minimum height: 64px. Radius: `md` (0.75rem).
*   **Signature Styling:** Apply a subtle inner-glow gradient to Primary buttons to make them feel "pressable" and tactile.
*   **Secondary:** Uses `secondary_container` (#81f3e5) with `on_secondary_container` (#006f66). Perfect for "Back" or "Save" actions.

### Input Fields: "Typeform-Inspired"
*   **Styling:** No bottom-line only inputs. Use large, filled containers (`surface_container_highest`) with no border. 
*   **Focus State:** Transition the background to `primary_fixed` (#c6e7ff).
*   **Spacing:** Ensure 24px of internal padding to make the tap target massive.

### Progress Indicators: "The Encourager"
*   **Track:** `surface_container_high`.
*   **Indicator:** Use `tertiary_fixed_dim` (#ffb95f). This warm gold provides an "encouraging" psychological nudge that the user is making progress.

### Cards & Lists: The "Fluid" List
*   **Rule:** Forbid divider lines.
*   **Alternative:** Use `1.5rem` (xl) vertical spacing and alternating `surface` and `surface_container_low` backgrounds to distinguish between different insurance policy results.

---

## 6. Do’s and Don’ts

### Do:
*   **Use Asymmetry:** Place your headers slightly off-center to create an editorial, high-end feel.
*   **Embrace the "Large":** If in doubt, make the font larger. Senior-friendly design is about reducing the cognitive load of squinting.
*   **Use Warmth:** Use the `tertiary` gold (#593600) for highlights to make the insurance process feel less "clinical."

### Don't:
*   **Don't use Dividers:** Never use a 1px line to separate list items. Use white space.
*   **Don't use Pure Black:** Avoid `#000000`. Use `on_surface` (#191c1e) for deep contrast that doesn't vibrate on screen.
*   **Don't Over-Animate:** Use slow, purposeful fades (300ms+). Fast, snappy animations can be disorienting for users with declining motor or visual processing speeds.