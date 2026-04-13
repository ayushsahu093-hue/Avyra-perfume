# Design System Strategy: The Olfactory Gallery

### 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Olfactory Gallery."** 

In high-end perfumery, the scent is invisible but occupies space with profound intent. This design system must mirror that experience. We are moving away from the "app-like" density of standard interfaces toward a digital environment that feels like a curated exhibition. By utilizing intentional asymmetry, expansive whitespace, and a sophisticated interplay of earthy tones, we create an atmosphere of quiet luxury. 

The goal is to break the "template" look. We do this by allowing elements to breathe, overlapping imagery with typography to create depth, and using tonal shifts rather than structural lines to guide the eye.

---

### 2. Colors & Tonal Depth
Our palette is rooted in the natural world—soft mosses, sun-bleached linens, and rich earth.

**Primary Palette & Roles:**
*   **Background (`#fdf9f3`):** Our "Gallery Wall." A warm, breathable cream that serves as the canvas for all interactions.
*   **Primary (`#3e5219`):** The "Evergreen Statement." Used for key brand moments and high-priority actions.
*   **Secondary (`#526345`) & Tertiary (`#544b37`):** These provide the "Botanical Depth," used for supporting UI elements and accents that mimic natural shadows and organic materials.

**The "No-Line" Rule:**
Standard 1px solid borders are strictly prohibited for sectioning. To define boundaries, use background color shifts. A section might transition from `surface` (`#fdf9f3`) to `surface-container-low` (`#f7f3ed`) to denote a change in content without the visual clutter of a line.

**Surface Hierarchy & Nesting:**
Treat the UI as physical layers.
*   **Base:** `surface`
*   **Embedded Sections:** `surface-container`
*   **Elevated Cards:** `surface-container-lowest` (`#ffffff`) to create a soft "pop" against the cream background.

**The "Glass & Gradient" Rule:**
For floating menus or high-end navigation, use Glassmorphism. Apply a semi-transparent `surface` color with a `backdrop-blur` of 12px to 20px. For primary CTAs, use a subtle linear gradient from `primary` (`#3e5219`) to `primary-container` (`#556b2f`) at a 135-degree angle to provide a velvet-like texture.

---

### 3. Typography
The typography system relies on a high-contrast pairing between a heritage-inspired serif and a precision-engineered sans-serif.

*   **Display & Headlines (Noto Serif):** These are the "Voices" of the brand. They should be used with generous letter spacing (tracking) in lowercase or dramatic scale in Sentence case. The Serif conveys history, craft, and the artisan nature of perfume.
*   **Body & Labels (Manrope):** The "Technical Specification." Manrope provides a clean, modern counter-balance. It ensures that while the brand feels historic, the shopping experience feels effortless and precise.
*   **The Hierarchy Goal:** Use `display-lg` (3.5rem) for hero statements to command attention, while keeping `body-md` (0.875rem) tucked away with high line-height (1.6) to maintain an editorial, airy feel.

---

### 4. Elevation & Depth
In this design system, depth is felt, not seen. We reject heavy, artificial shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Stack `surface-container` tiers to create hierarchy. A product card using `surface-container-lowest` placed on a `surface-container-low` section creates a natural "lift" that mimics fine paper resting on a stone counter.
*   **Ambient Shadows:** If an element must float (like a modal or a floating action), the shadow must be nearly invisible. Use the `on-surface` color at 4% opacity with a 32px blur and 16px offset. This mimics natural, ambient light.
*   **The "Ghost Border" Fallback:** If a border is required for clarity (e.g., an input field), use the `outline-variant` (`#c5c8b8`) at 20% opacity. Never use 100% opaque borders.
*   **Glassmorphism:** Use semi-transparent layers for elements like navigation bars to allow the "scent" (the background imagery and colors) to bleed through, softening the interface's edges.

---

### 5. Components

**Buttons:**
*   **Primary:** Solid `primary` (`#3e5219`) with `on-primary` text. Use a `md` (0.375rem) corner radius for a sharp, tailored look.
*   **Secondary:** A "Ghost" style. No fill, with a `primary` text color and a 10% opacity `outline` border.
*   **States:** On hover, primary buttons should shift to `primary-container`. No dramatic "lifts"—just a subtle color deepening.

**Input Fields:**
*   Do not use enclosed boxes. Use a `surface-container-high` background with a `sm` (0.125rem) bottom-only "Ghost Border."
*   Labels (`label-md`) should always be visible, floating above the field in `tertiary` color to maintain an archival look.

**Cards:**
*   **Rule:** Forbid divider lines.
*   Use `surface-container-lowest` for the card body. Separation is achieved through 32px or 48px of vertical whitespace.
*   Images within cards should use the `lg` (0.5rem) roundedness scale to feel like "smooth pebbles" or polished glass.

**Fragrance Note Chips:**
*   Small, interactive elements used to filter scents (e.g., "Sandalwood," "Bergamot").
*   Style: `secondary-container` background with `on-secondary-container` text. Use `full` (9999px) rounding to make them feel organic and touchable.

---

### 6. Do's and Don'ts

**Do:**
*   **Do** use asymmetrical layouts. Place a large image on the left and a small, high-contrast headline on the right with significant vertical offset.
*   **Do** prioritize imagery. The perfume bottles and raw ingredients are the stars; the UI is the frame.
*   **Do** use "Optical Spacing." If a section feels crowded, double the white space.

**Don't:**
*   **Don't** use pure black (`#000000`). Always use `on-surface` (`#1c1c18`) for text to keep the look soft and premium.
*   **Don't** use standard "drop shadows." They break the organic, earthy feel of the palette.
*   **Don't** use "loud" animations. Transitions should be slow fades (300ms+) or subtle "slide-and-fade" movements that mimic the lingering of a scent.
*   **Don't** use 1px dividers to separate list items. Use tonal shifts between `surface-container` tiers instead.