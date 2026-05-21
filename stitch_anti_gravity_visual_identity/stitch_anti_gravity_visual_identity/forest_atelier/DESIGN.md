# Design System Specification: The Botanical Archivist

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Botanical Archivist."** This vision moves away from the sterile, "tech-first" aesthetic and toward a high-end editorial experience that feels curated, organic, and authoritative. 

We are building a digital conservatory. To achieve this, we reject the rigid, "boxed-in" layout of standard SaaS templates. Instead, we embrace **intentional asymmetry**, large-scale editorial typography, and a "depth-first" layering strategy. Elements should feel like specimens placed carefully on a dark velvet surface—overlapping, breathing, and connected by light rather than lines.

---

## 2. Colors: Tonal Depth & Organic Accents
Our palette is a study in shadows and light. We utilize high-contrast accents against a monochromatic foundation of deep, mossy greens to guide the eye.

### The Foundation (Primary Palette)
*   **Midnight Moss (#0a0f0a):** Used exclusively for page-level backgrounds (`surface_container_lowest`). This is our canvas.
*   **Forest Depth (#142114):** Used for large structural sections.
*   **Deep Canopy (#1e3a1e):** Used for elevated surfaces like cards and modals.
*   **Jungle Green (#2d5c2d):** Reserved for subtle structural cues and low-contrast borders.

### The Radiance (Accent Palette)
*   **Marigold Gold (#d4a843):** Our primary CTA and pricing token. It represents value and sunlight.
*   **Sunlight (#e8c068):** Used for micro-interactions, highlights, and active states.
*   **Daisy White (#f5f0e8):** Primary typography. A warm off-white to prevent harsh ocular fatigue.
*   **Leaf Mist (#a8c5a0):** Muted secondary text and decorative botanical elements.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Boundary definition must be achieved through background shifts. A `Forest Depth` section sitting on a `Midnight Moss` background provides enough contrast to be felt without the "cheapness" of a structural line.

### Glassmorphism & Signature Textures
To provide a "signature" feel, we employ glass layers for navigation and floating elements:
*   **Dark Navbar:** `rgba(45, 92, 45, 0.4)` with a `backdrop-filter: blur(12px)`.
*   **Hover States:** Use `rgba(168, 197, 160, 0.1)` (Leaf Mist) to create a soft "organic glow" behind elements.
*   **CTA Soul:** Never use a flat #d4a843. Apply a subtle linear gradient from `Marigold Gold` to `Sunlight` at 135 degrees to simulate a metallic, premium finish.

---

## 3. Typography: The Editorial Voice
We use a high-contrast pairings to evoke the feeling of a premium botanical journal.

*   **Display & Headlines (Noto Serif):** Use these for brand moments and storytelling. The serif adds historical weight. *Implementation: Use tight letter-spacing (-0.02em) for Display-LG to create a custom, "font-locked" look.*
*   **UI & Body (Manrope):** A modern, geometric sans-serif that ensures legibility in dense data environments.
*   **Hierarchy as Identity:** Use `Display-LG` (3.5rem) and `Body-SM` (0.75rem) in close proximity to create "Scale Shock"—a hallmark of high-end design that signals confidence.

---

## 4. Elevation & Depth: Tonal Layering
In this system, depth is not a shadow; it is a change in pigment.

*   **The Layering Principle:** 
    1.  Base: `Midnight Moss (#0a0f0a)`
    2.  Section: `Forest Depth (#142114)`
    3.  Object (Card/Menu): `Deep Canopy (#1e3a1e)`
*   **Ambient Shadows:** If an object must float (e.g., a dropdown), use a shadow color of `rgba(0, 5, 0, 0.6)` with a 40px blur. This mimics the way shadows fall in a dense forest—dark and diffused, not grey.
*   **The Ghost Border:** For accessibility on inputs, use `Jungle Green (#2d5c2d)` at 20% opacity. This creates a "suggestion" of a container without breaking the organic flow.

---

## 5. Components: Refined Interaction

### Buttons
*   **Primary:** Gradient of `Marigold Gold` to `Sunlight`. No border. Text color: `Midnight Moss (#0a0f0a)` for maximum legibility.
*   **Secondary:** Ghost style. `Daisy White` text with a `Jungle Green` 1px border at 40% opacity.
*   **Tertiary:** `Leaf Mist` text, no background, underline on hover only.

### Cards
*   **Style:** No borders. Use `Deep Canopy` fill. 
*   **Interaction:** On hover, shift background to `rgba(168, 197, 160, 0.1)` and increase the "leafiness" by introducing a subtle `Leaf Mist` inner glow.

### Input Fields
*   **Style:** `Midnight Moss` fill with a `Jungle Green` bottom border only (2px). 
*   **Focus State:** The bottom border transforms into `Marigold Gold`. Helper text should always be `Leaf Mist`.

### Selection Chips
*   **Unselected:** `Forest Depth` background, `Leaf Mist` text.
*   **Selected:** `Marigold Gold` background, `Midnight Moss` text. Pill-shaped (Rounded: full).

---

## 6. Do’s and Don'ts

### Do:
*   **Do** use generous white space. If you think there is enough space, add 16px more.
*   **Do** overlap images with text. Let a serif headline bleed into the edge of a botanical photograph.
*   **Do** use `Leaf Mist` for all "metadata" (dates, categories, tags).
*   **Do** use the `0.25rem` (sm) roundedness for most UI, but `full` for chips and buttons to soften the interface.

### Don't:
*   **Don't** use pure black (#000000) or pure white (#ffffff). It breaks the botanical immersion.
*   **Don't** use standard "Drop Shadows" (Offset X/Y). Keep shadows centered and diffused.
*   **Don't** use divider lines between list items. Use 24px of vertical space or a 5% shift in background color instead.
*   **Don't** use bright "Alert Blue" or "Success Green." Map all feedback states to our palette (e.g., use `Sunlight` for warnings).

---

## 7. Signature Layout Patterns: The "Asymmetric Specimen"
When designing hero sections, do not center-align everything. Place the `Display-LG` headline on the left, and push the primary CTA to the far right or offset it vertically. This breaks the "website template" feel and makes the screen feel like a thoughtfully composed page in an archive.