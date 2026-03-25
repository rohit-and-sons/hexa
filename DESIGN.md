# Design System Document: Dr. Prabhudas Clinic

## 1. Overview & Creative North Star: "The Heritage Sanctuary"
The design system for Dr. Prabhudas Clinic rejects the sterile, "disposable" aesthetic of modern health-tech. Instead, it adopts **The Heritage Sanctuary** as its North Star. This creative direction blends the clinical precision of a high-end medical institution with the warm, grounded reliability of a 25-year practice in Shimla.

To achieve this, the system moves away from rigid, boxed-in grids. We utilize **intentional asymmetry**, where large editorial type balances against generous whitespace. Layouts should feel like a premium medical journal—authoritative yet breathable. We break the "template" look by layering surfaces like sheets of fine vellum, using soft tonal shifts rather than harsh lines to guide the eye.

---

## 2. Colors & Surface Philosophy
The palette is rooted in deep, trust-inducing blues (`primary`) and the restorative greens of the Shimla landscape (`secondary`).

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections. Layout boundaries must be established solely through:
- **Background Color Shifts:** Transitioning from `surface` to `surface-container-low`.
- **Nesting:** Placing a `surface-container-lowest` card inside a `surface-container` section.

### Surface Hierarchy & Layering
Treat the UI as a physical environment. Importance is dictated by "height" through color, not shadows:
- **Level 0 (Base):** `surface` (#f7f9fb) – Used for global page backgrounds.
- **Level 1 (Subtle Inset):** `surface-container-low` (#f2f4f6) – For large secondary content areas.
- **Level 2 (The Interactive Surface):** `surface-container-lowest` (#ffffff) – Reserved for primary cards and input fields to make them "pop" against the off-white base.

### The "Glass & Gradient" Rule
To elevate the experience, use **Glassmorphism** for floating headers or navigation bars. Use `surface` at 80% opacity with a `backdrop-blur` of 20px. 
- **Signature Gradient:** For primary CTAs and Hero sections, use a subtle linear gradient from `primary` (#003178) to `primary_container` (#0d47a1) at a 135-degree angle. This adds "soul" and depth that prevents the design from feeling flat or "SaaS-like."

---

## 3. Typography: Editorial Authority
We use a high-contrast pairing of **Manrope** for structure and **Public Sans** for clarity.

*   **Display & Headlines (Manrope):** Large-scale, tight tracking (-2%). These should feel like titles in a premium publication. Use `display-lg` (3.5rem) for hero statements to convey 25 years of undisputed expertise.
*   **Body & Titles (Public Sans):** Chosen for its exceptional legibility. `body-lg` (1rem) is the workhorse for patient information.
*   **The "Compassionate Scale":** Always err on the side of larger type. Use `title-lg` (1.375rem) for testimonial quotes to ensure the "voice" of the patient is prominent and readable for all age demographics.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are largely replaced by **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by stacking. A `primary_fixed` button sits on a `surface_container_lowest` card, which sits on a `surface` background. This creates a sophisticated, "quiet" hierarchy.
*   **Ambient Shadows:** If a component (like a booking modal) must float, use a "Cloud Shadow": `Y: 20px, Blur: 40px, Color: rgba(25, 28, 30, 0.06)`. It should feel like a soft glow, not a hard edge.
*   **The "Ghost Border" Fallback:** If a divider is functionally required, use `outline_variant` at **15% opacity**. Never use 100% opaque lines.

---

## 5. Signature Components

### Appointment Booking Module
- **Style:** Instead of a standard form, use a "Stepper" approach housed in a `surface_container_lowest` container.
- **Inputs:** Use "Underline" style inputs where only the bottom border exists (using `outline_variant`), or floating labels with `surface_container_high` backgrounds.
- **CTA:** The "Confirm Appointment" button uses the `primary` gradient with `xl` (0.75rem) roundedness.

### Service Cards
- **Construction:** No borders. Use a `surface_container_low` background. 
- **Interaction:** On hover, the background shifts to `secondary_fixed` (#97f3e2) with a subtle `2.5` (0.85rem) vertical lift using an Ambient Shadow.
- **Typography:** Service titles use `headline-sm`.

### Patient Testimonials
- **Layout:** Asymmetrical. The quote (in `primary`) uses `headline-md`, while the patient's name and "Verified Patient" tag use `label-md` in `on_surface_variant`.
- **Accents:** Use a large, 10% opacity "quotation mark" icon in `secondary` as a background element to break the grid.

### Buttons & Chips
- **Primary Button:** `primary` fill, `on_primary` text, `lg` (0.5rem) roundedness. 
- **Selection Chips:** For choosing time slots. Unselected: `surface-container-high`. Selected: `secondary` with `on_secondary` text.

---

## 6. Do’s and Don’ts

### Do
- **Do** use `20` (7rem) or `24` (8.5rem) spacing between major sections to create an elite, "unrushed" feeling.
- **Do** use images with soft, natural lighting—ideally showing Dr. Prabhudas in a professional yet warm environment.
- **Do** utilize the `secondary` (teal) color for "Success" states and health-related accents to reinforce the clinical-nature.

### Don’t
- **Don’t** use pure black (#000000). Always use `on_surface` (#191c1e) for text to maintain a premium softness.
- **Don’t** use `none` roundedness. Even the most "serious" elements should have at least `sm` (0.125rem) corners to feel compassionate.
- **Don’t** use standard "Blue/Red" for everything. Use the `tertiary` scale (#30372d) for neutral, grounded elements like footer links or metadata.