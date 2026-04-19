# Design System Specification: Urban Kinetic

## 1. Overview & Creative North Star
The visual identity of this design system is anchored in a concept we call **"The Tactical Kinetic."** In the world of high-performance distribution, precision and momentum are everything. We are moving away from the "safe" corporate grid to create a digital environment that feels like a high-end tactical interface—authoritative, dark, and exceptionally professional.

This design system avoids the "template" look by embracing **intentional asymmetry** and **tonal depth**. We treat the screen not as a flat canvas, but as a multi-layered command center. By utilizing overlapping elements, massive typography scales, and a strictly dark "Urban" palette, we create an editorial experience that feels custom-built for the elite industrial sector.

## 2. Colors & Surface Logic
The palette is a sophisticated interplay between the "Urban" darkness of the city and the high-visibility energy of a logistics hub.

*   **Primary Core:** The Brand Deep Blue (`primary_container`: `#1B365D`) serves as our foundation, representing stability and depth.
*   **The Ignition Point:** The Brand Orange (`secondary_container`: `#F27024`) is used exclusively for high-priority actions. It is the "spark" in the dark.
*   **The "No-Line" Rule:** To achieve a premium, high-end feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined solely through background color shifts. For example, a `surface_container_low` section sitting on a `surface` background provides all the separation a professional eye needs.
*   **Surface Hierarchy & Nesting:** We treat the UI as a series of physical layers. 
    *   Base layer: `surface` (`#10141a`).
    *   Secondary grouping: `surface_container_low` (`#181c22`).
    *   Interactive/Floating: `surface_container_high` (`#262a31`).
*   **The Glass & Gradient Rule:** For hero sections and floating navigation, use **Glassmorphism**. Apply `surface_bright` at 40% opacity with a `20px` backdrop-blur. This allows the primary blue tones to bleed through, softening the tactical edge with a modern, high-tech polish.

## 3. Typography: The Editorial Edge
Typography is our primary tool for expressing "High Performance." We use a high-contrast scale to create an authoritative hierarchy.

*   **Display & Headlines (Space Grotesk):** This is our "Tactical" voice. Space Grotesk’s geometric quirks and wide stance suggest engineering precision. 
    *   *Usage:* Use `display-lg` (3.5rem) with tight tracking (-2%) for hero statements. It should feel massive and immovable.
*   **Body & Utility (Inter):** Inter provides the "Professional" balance. It is neutral, highly legible, and efficient.
    *   *Usage:* `body-md` (0.875rem) for all technical data and descriptions.
*   **Labels (Space Grotesk):** All labels (`label-md`) should be uppercase with slightly increased letter spacing (5-10%) to mimic technical instrumentation.

## 4. Elevation & Depth
In this design system, depth is earned through **Tonal Layering**, not shadows.

*   **The Layering Principle:** Depth is achieved by stacking surface-container tiers. Place a `surface_container_lowest` card on a `surface_container_low` section to create a "recessed" or "lifted" effect naturally.
*   **Ambient Shadows:** If a floating element (like a modal) requires a shadow, it must be ultra-diffused. Use a `32px` blur at 8% opacity using the `on_surface` color as a tint. Avoid "dirty" grey shadows at all costs.
*   **The Ghost Border Fallback:** Where accessibility requires a border, use a "Ghost Border": the `outline_variant` token at **15% opacity**. This creates a hint of a boundary without cluttering the visual field.
*   **Logo Integration:** The logo's circular, kinetic arcs should be used as inspiration for background masks. Subtle, large-scale crops of the logo's "swish" can be used as `surface_variant` watermarks behind key content sections to reinforce brand identity without being literal.

## 5. Components

### Buttons
*   **Primary (CTA):** Background `secondary_container` (#F27024), Text `on_secondary` (#561f00). Shape: `md` (0.375rem).
*   **Secondary:** Background `primary_container` (#1B365D), Text `on_primary_container` (#87a0cd).
*   **Tertiary:** No background. Text `primary` (#aec7f7). Use for low-emphasis actions like "Cancel" or "View More."

### Input Fields
*   **Style:** No outer borders. Use `surface_container_highest` as the fill. 
*   **Indicator:** A 2px bottom-accent in `primary` (#aec7f7) appears only on focus. This mimics a "digital dashboard" feel.

### Cards & Lists
*   **The "No-Divider" Mandate:** Never use horizontal lines to separate list items. Use the Spacing Scale (Vertical rhythm) or alternating tonal shifts (e.g., a `surface_container_low` background for every second item).
*   **Interactive Cards:** Cards should have a `none` (0px) border. On hover, the surface should shift from `surface_container_low` to `surface_container_high`.

### Tactical Chips
*   **Selection Chips:** Use `primary_container` with `on_primary_fixed_variant` text. These should feel like "status indicators" on a machine.

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical layouts. Let a headline bleed 20px off the left margin or overlap a background image.
*   **Do** use high-contrast sizing. Make your headlines huge and your labels small.
*   **Do** utilize the `surface_container` tokens to create "wells" of content that feel carved into the UI.

### Don't:
*   **Don't** use pure white (#FFFFFF) for text. Use `on_surface` (#dfe2eb) to reduce eye strain and maintain the urban "dark mode" aesthetic.
*   **Don't** use standard 1px borders. If you feel you need a line, use a background color change instead.
*   **Don't** use rounded corners larger than `xl` (0.75rem). The system must remain "Tactical" and sharp, not "Soft" and bubbly.
*   **Don't** use traditional drop shadows. Use tonal layering to communicate hierarchy.

---
*Document produced for the junior design team. Adhere to these principles to maintain the "Urban Kinetic" identity.*