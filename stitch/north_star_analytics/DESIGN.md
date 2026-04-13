# Design System Strategy: Academic Professionalism

## 1. Overview & Creative North Star
The North Star for this design system is **"The Digital Atelier."** 

We are moving away from the "template" look of student organizations and toward a high-end, editorial experience that mirrors a modern consultancy or a data-driven research lab. The goal is to balance the heritage of UMD with the forward-looking nature of Management Information Systems and Business Analytics. 

To achieve this, the system breaks the traditional rigid grid through **Intentional Asymmetry** and **Tonal Depth**. Instead of boxing content into restrictive containers, we use sweeping white space, overlapping typography, and a "layered surface" philosophy. This creates a sense of movement and innovation—reflecting a club that is "connected" and "supportive" rather than static and institutional.

---

## 2. Colors: Tonal Architecture
The palette transitions from the authoritative "Academic Professionalism" of deep blues and slates to the energetic "UMD Heritage" accents of Maroon and Gold.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning or containment. Traditional borders feel "boxed in" and dated. 
- **Boundaries** must be defined solely through background color shifts. For example, a `surface-container-low` section sitting on a `surface` background creates a clear but sophisticated division.
- **Surface Hierarchy:** Use the hierarchy of `surface-container-lowest` to `surface-container-highest` to create a "nested" physical depth. Treat the UI like stacked sheets of fine paper or frosted glass.

### Signature Textures & Accents
- **The Glass Rule:** Use `surface-variant` with a `backdrop-blur` (12px–20px) for floating navigation or overlay elements. This prevents the UI from feeling "pasted on" and allows the brand colors to bleed through softly.
- **The Soul Gradient:** Main CTAs and Hero backgrounds should leverage subtle gradients (e.g., `primary` to `primary-container`). Avoid flat maroon; it lacks the "innovative" depth required for a modern MISBA experience.

---

## 3. Typography: The Editorial Edge
We use a high-contrast scale to create an "Editorial" feel. By pairing the technical precision of **Inter** with the geometric character of **Manrope**, we signal both "Knowledgeable" and "Innovative."

*   **Display (Manrope):** Used for "Big Ideas" and hero headers. `display-lg` (3.5rem) should be used with tight letter-spacing (-0.02em) to feel authoritative.
*   **Headlines (Manrope):** Designed for impact. Use `headline-lg` for section headers, often paired with an asymmetrical layout (e.g., left-aligned header with right-aligned body text).
*   **Body & Labels (Inter):** The workhorse. `body-lg` (1rem) provides high readability for "Student-Friendly" content. Labels are set in `label-md` to maintain clarity in data-dense analytics components.

The hierarchy is designed to guide the eye through "The Digital Atelier," leading with a bold statement and supporting it with clean, breathable data.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows and borders are replaced by **Ambient Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking" surface tiers. Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a soft, natural lift without visual noise.
*   **Ambient Shadows:** When a float is necessary (e.g., a modal or a primary button), use an extra-diffused shadow. 
    *   *Spec:* `0px 12px 32px rgba(13, 28, 46, 0.06)`. Note the use of a tinted `on-surface` color rather than pure black.
*   **The Ghost Border Fallback:** If a boundary is strictly required for accessibility, use the `outline-variant` token at **20% opacity**. Never 100%.

---

## 5. Components: The MISBA Toolkit

### Primary CTA Buttons
- **Style:** High-contrast `primary` container with `on-primary` text.
- **Geometry:** `rounded-full` for a "Connected" and "Friendly" feel.
- **Interaction:** On hover, transition from `primary` to `primary-container` with a subtle `surface-tint` glow.

### Signature Member Cards
- **Construction:** Use `surface-container-lowest` with `rounded-xl` (1.5rem) corners.
- **Rule:** **No Dividers.** Separate the member’s name from their MISBA role using vertical white space (1rem) and a font weight shift (Semi-bold to Regular).
- **The Accent:** A subtle 4px vertical bar of `secondary` (Gold) on the left side of the card provides the UMD nod without overpowering the professional slate tones.

### Analytical Chips
- **Style:** Use `tertiary-container` for the background and `on-tertiary-container` for text.
- **Context:** Perfect for tagging skills (e.g., "Python," "Data Viz") on board member profiles or event listings.

### Input Fields
- **Style:** "Floating Label" style using `surface-container-high`. 
- **States:** The "Active" state should utilize a 2px `secondary` (Gold) bottom-only "Underglow" rather than a full-box stroke.

---

## 6. Do's and Don'ts

### Do
- **Do** use `surface-dim` for dark mode backgrounds to maintain "Academic Professionalism" without the harshness of pure black.
- **Do** embrace asymmetrical white space. Let a hero image bleed off the edge of the screen to create an "Innovative" feel.
- **Do** use `secondary_container` (Gold) sparingly—as a "light" to guide the user's eye to primary actions or notifications.

### Don't
- **Don't** use 1px solid lines to separate board members in a list. Use `1.5rem` of vertical white space or a subtle background shift.
- **Don't** use "Drop Shadows" that are dark or tight. If it looks like a "button from 2010," it is too heavy.
- **Don't** crowd the interface. If a screen feels "busy," increase the padding using the `xl` (1.5rem) rounding scale as a spacing guide.

---

## 7. Token Summary Reference

| Role | Token / Value | Application |
| :--- | :--- | :--- |
| **Primary Brand** | `#811331` (Maroon) | Key accents, Hero headers, Primary CTAs |
| **Secondary Brand** | `#FFCC33` (Gold) | Interaction cues, small "Supportive" accents |
| **Professional Base**| `#0c2c50` (Deep Blue) | Tertiary containers, Professional headers |
| **Surface Base** | `#f8f9ff` (Slate White)| Main background for "Modern & Clean" look |
| **Corner Radius** | `1rem` (lg) | Standard for cards and feature blocks |
| **Typography (H1)** | Manrope / 2.75rem | "Innovation" and "Knowledge" headlines |
| **Typography (Body)**| Inter / 1rem | "Supportive" and "Readable" student content |