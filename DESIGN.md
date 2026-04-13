```markdown
# Design System Document: STIM Canada Industrial Excellence

## 1. Overview & Creative North Star

### The Creative North Star: "The Precision Engineer"
This design system is built to reflect the high-stakes world of Tier-1 electronics manufacturing. It moves beyond the generic "industrial" aesthetic by adopting a high-end editorial approach—combining the clinical precision of medical technology (ISO 13485) with the robust reliability of advanced PCBA production.

The system breaks away from standard "templated" layouts through **intentional white space** and **asymmetric balance**. We avoid heavy containers in favor of breathing room and sophisticated tonal shifts. By layering surfaces rather than drawing borders, the UI feels like a high-tech cleanroom: open, organized, and meticulously calibrated.

---

## 2. Colors

The palette is anchored by a sophisticated teal and supported by a range of technical greys.

### Primary Spectrum
- **Primary (`#006a63`)**: The core brand color, used for high-signal actions and key brand identifiers.
- **Primary Container (`#35bdb2`)**: Used for hero backgrounds or secondary CTA surfaces to inject vibrant energy.

### Tonal Surface Strategy
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning content. Boundaries are defined exclusively through background shifts. For instance, a technical data section using `surface-container-low` (`#f3f4f5`) should sit directly on a `surface` (`#f8f9fa`) background.
- **Surface Hierarchy:** 
    - `surface-container-lowest` (#ffffff): Use for cards or primary content blocks to make them "pop" against the background.
    - `surface` (#f8f9fa): The standard page canvas.
- **The "Glass & Gradient" Rule:** For floating navigation elements or high-tech overlays, use Glassmorphism. Apply `surface` at 80% opacity with a `20px` backdrop-blur.
- **Signature Textures:** Use subtle linear gradients for CTAs, transitioning from `primary` (#006a63) to `primary-container` (#35bdb2) at a 135-degree angle to create a sense of depth and "tech-glow."

---

## 3. Typography

The typography pairs **Manrope** (Display/Headlines) with **Inter** (Body/Labels) to balance industrial strength with modern readability.

### Scale & Hierarchy
- **Display Large (Manrope, 3.5rem):** Reserved for hero value propositions (e.g., "Precision Manufacturing for Life-Critical Electronics").
- **Headline Medium (Manrope, 1.75rem):** Used for service categories like "PCBA Assembly" or "Box-Build Integration."
- **Title Medium (Inter, 1.125rem, Semi-Bold):** Used for secondary headers and card titles.
- **Body Medium (Inter, 0.875rem):** The workhorse for technical descriptions and service details.

**Identity Note:** Headlines should use a "tight" letter-spacing (-0.02em) to feel authoritative and engineered, while body text uses standard tracking for maximum legibility in technical contexts.

---

## 4. Elevation & Depth

We eschew traditional "drop shadows" in favor of **Tonal Layering** and **Ambient Light**.

- **The Layering Principle:** Depth is achieved by stacking containers. A `surface-container-lowest` card placed on a `surface-container-low` background creates a natural elevation that mimics a physical component placed on a workbench.
- **Ambient Shadows:** When a floating element (like a modal or dropdown) is required, use a tinted shadow: `rgba(0, 71, 66, 0.08)` with a `32px` blur and `8px` Y-offset. This pulls the brand teal into the shadow, making it feel integrated into the environment.
- **The "Ghost Border" Fallback:** For input fields or essential separations, use the `outline-variant` (#bbc9c7) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons (The "Actuator" Style)
- **Primary:** Gradient fill (`primary` to `primary-container`), white text, `0.25rem` (4px) corner radius.
- **Secondary:** Transparent background with a "Ghost Border" (20% opacity `primary`). Text in `primary`.
- **States:** On hover, primary buttons should increase in saturation; secondary buttons should gain a subtle `surface-container-high` background tint.

### Circular Icon Indicators
Inspired by the "Value Added Service" section, icons must be housed in circular containers. Use a `surface-container-highest` circle with a `primary` icon. This mimics the appearance of high-end industrial buttons or indicators.

### Service Cards
- **Construction:** No borders. Background: `surface-container-lowest`. 
- **Header:** Title-Medium (Inter).
- **Body:** Body-Medium (Inter).
- **Separator:** A 24px horizontal line in `primary` (#006a63) at 2px thickness to separate the headline from the text—used sparingly as a "surgical strike" of color.

### Technical Specification Chips
Used for certifications like "ISO 9001" and "ISO 13485."
- **Style:** `secondary-container` background with `on-secondary-container` text. Small `0.125rem` radius to feel precise and "stamped."

### Input Fields
- **Style:** Use a "bottom-line-only" approach for a cleaner, more editorial look, or a full container with `surface-container-low` and a 15% opacity Ghost Border.

---

## 6. Do's and Don'ts

### Do:
- **Use High-Contrast Imagery:** Use photos of green PCBs, stainless steel housings, and clinical medical environments. Crop images aggressively to create interesting angles.
- **Embrace White Space:** If a section feels crowded, double the padding. The "Precision" brand personality requires room to breathe.
- **Highlight Certifications:** Treat ISO certifications as "Badges of Honor"—place them prominently in the footer and hero sections using the high-contrast Teal accent.

### Don't:
- **No 100% Black:** Never use `#000000`. Use `on-surface` (#191c1d) for text to maintain a sophisticated, soft-touch industrial feel.
- **No Rounded Corners > 8px:** This is an industrial system. Large, bubbly radii (like 24px or 32px) undermine the "Reliable & Professional" personality. Stick to `0.25rem` (4px) or `0.5rem` (8px).
- **No Heavy Dividers:** Never use a full-width, high-contrast line to separate sections. Use a background color change from `surface` to `surface-container-low` instead.

---

## Contact & Brand Info
- **Entity:** STIM Canada
- **Contact:** (416) 636 4584 | sales@stimcanada.com
- **Services:** PCBA, Box-Build, NPI/Prototyping, Supply Chain Solutions.
- **Quality Mandate:** ISO 9001 & ISO 13485 Certified.```