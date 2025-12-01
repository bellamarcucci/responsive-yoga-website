# Responsive Yoga Website

This repository contains a responsive, multi-section landing page for a yoga website.  
The project focuses on modern front-end development practices using **semantic HTML5** and **CSS3**, including responsive design, dark mode, animations, and a component-based layout inspired by a professional UI design.

---

## Design Credits

This project is based on an original UI design created by **Young Kim**.

**Designer:** Young Kim 
**Figma Profile:** https://www.figma.com/@youngkim5  

All visual inspiration, layout composition, spacing, and overall aesthetic were derived from Young Kim’s design.  
This implementation is for **educational purposes only**.

---

## Development Team

This project was designed and developed by:

- **Isabella Marcucci**
- **Santiago Suárez Jaramillo**

---

## Technologies Used

The project was built using:

- **HTML5**
  - Semantic structure for sections such as `header`, `main`, hero content, navigation, and feature sections.

- **CSS3**
  - **CSS Custom Properties (Variables)**  
    - The global design system is managed through variables defined in `:root`, such as:
      - `--bg-color`
      - `--text-color`
      - `--title-color`
      - `--border-color`
      - `--gradient-color`
  - **Typography & Fonts**
    - Global font family: `"Poppins", sans-serif`
    - Headings using `"Lora", serif` for a more elegant, editorial look.

    - **Layout & Positioning**
        - Flexbox for layout alignment in navigation, hero section, list sections, and health section (`display: flex`, `justify-content`, `align-items`, `gap`).
        - Positioning with `absolute`, `relative`, and `fixed` to control overlapping elements, floating badges, icons, and decorative shapes.
        - Controlled stacking using `z-index` for layered content (menu, dark-mode toggle, hero images, decorative graphics).

    - **Responsive Design**
        - **Media Queries** for devices with `max-width: 768px`:
        - Reflow of the hero section into a column layout.
        - Mobile navigation with a slide-in menu using a hamburger icon and checkbox toggle.
        - Resized headings, images, and spacing for small screens.

    - **Dark Mode Toggle**
        - Implemented with a hidden checkbox (`.theme-toggle`) combined with the sibling selector:
        ```css
            .theme-toggle:checked ~ .full-page-content {
                --bg-color: #14092A;
                --text-color: #A094B8;
                --title-color: #D1C0F1;
                --border-color: #14092A;
            }
            ```
        - Theme switcher (`.theme-switch`) swaps sun and moon icons using conditional display rules with `.icon-sun` and `.icon-moon`.

    - **Transitions & Animations**
        - Smooth transitions for background and text colors:
        ```css
        * {
            transition: background-color 0.5s ease, color 0.5s ease;
        }
        ```
        - `@keyframes starSpin` for rotating decorative star elements.
        - `@keyframes tiltDrop` for playful motion on gradient tags on hover.

    - **Buttons & Gradients**
        - Reusable gradient styles defined with `--gradient-color` and applied to:
        - Primary CTA buttons (`.title-btn`, `.health-btn`)
        - Gradient text using `background-clip: text` and `color: transparent`.

    - **Overflow & Page Behavior**
        - `html, body { overflow-x: hidden; }` to prevent unintended horizontal scroll on wide positioned elements.

- **License & Usage**

    This project is intended for educational and portfolio use only.
    The original UI design belongs to Young Kim and may not be used for commercial purposes without the designer’s permission.


---