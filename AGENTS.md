# Product and Design Guidelines

This document establishes the core business rules, visual identity, and layout constraints for Murilo's portfolio website. All development and design implementations must strictly adhere to these product requirements.

---

## Visual Identity and Aesthetics

### 1. Styling and Theme
* **Design Philosophy:** Strictly ultra-minimalist, professional, sharp, and highly functional. 
* **Color Palette:** The system operates exclusively on a dark theme baseline (`#0a0a0a`). Core layouts must use strictly neutral shades (slate, zinc, gray, white, black).
* **Color Restrictions:** The introduction of vibrant accent colors is strictly forbidden. All layout scaffolding must remain neutral. A single highlight color will be introduced in future product iterations.

### 2. Typography
* **Font Stacking:** Use the pre-loaded system sans-serif fonts (Inter and JetBrains Mono) across all standard section interfaces.

---

## Layout Constraints and Component Requirements

### 1. Navigation Bar (Navbar)
* **Functionality:** Must implement smooth-scrolling anchors targeting respective homepage sections.
* **Internationalization:** Must include a non-functional layout placeholder (such as a button or dropdown) for language switching. The default active state text must display "EN-US".

### 2. About Section Structure
* **Desktop Viewports (`md:` and `lg:` grid/flex configurations):** The layout must place the biographical text on the left side and the profile image placeholder/carousel container on the right side.
* **Mobile Viewports:** The layout must collapse into a vertical stack, positioning the biographical text on top and the image container directly below it.

### 3. Contact Section
* **Communications:** Provide a clean, direct call-to-action trigger for email communications.
* **Social Proof:** Integrate minimalist icon links pointing to external LinkedIn and GitHub profiles.

### 4. Footer and External Resources
* **Copyright Notice:** Must explicitly render the standard legal copyright line for "Murilo Dias da Costa".
* **Professional Resume:** Include a clearly visible placeholder element or direct download link for the professional resume asset.

---

## Product Development Philosophy

* **Simplicity First:** Prioritize clean, unbloated component logic. Rely heavily on native Tailwind CSS classes and straightforward Framer Motion configurations over complex custom orchestration.
* **Iterative Engineering:** Construct the foundational architectural layout using static placeholder constants first. Refine data definitions and dynamic mapping in subsequent code passes.
* **Structural Discipline:** Map homepage components precisely to the `src/components/sections/` directory and compose them linearly within the main `src/app/page.tsx` file.