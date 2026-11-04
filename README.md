# 🎨 Cat Painting — Pure CSS Art & Geometry

> *A creative exploration of modern CSS layout techniques, shape manipulation, and layering logic.*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

---

## 📌 Project Overview

**Cat Painting** is an interactive pure-CSS artwork built without external images, SVG graphics, or JavaScript rendering engine frameworks. Designed as part of the freeCodeCamp Responsive Web Design curriculum, this project focuses on pushing CSS positioning mechanics to their absolute limit.

By treating the browser DOM as a canvas, every facial contour, ear shape, eye highlight, and whisker line is generated strictly using styled HTML `div` elements, precise border clipping, CSS transforms, and relative/absolute stacking context management.

---

## ⚙️ Key Technical Features & Concepts

### 1. Advanced Border Geometry
Standard DOM elements are rectangular, but CSS borders interact at 45-degree angles when adjacent sides meet. By setting specific borders to `transparent` and giving fixed pixel widths to others, complex triangles and curved slopes were formed:
* **Cat Ears:** Formed using transparent left/right borders and a solid bottom border.
* **Cat Nose:** Built with inverted solid/transparent border tricks and rounded corners.

### 2. Stacking Context & `z-index` Management
Layering visual components requires a strict understanding of the CSS Stacking Context:
* **Parent Coordinates:** `.cat-head` establishes `position: relative` to act as the coordinate system for child elements.
* **Child Overlays:** Inner ears, eyes, and mouth lines leverage `position: absolute` with tailored `z-index` levels to prevent unwanted overlap artifacts.

### 3. CSS Ellipses & Multi-Corner Radius
By utilizing the slash syntax (`/`) inside `border-radius`, custom elliptical curves were achieved for the mouth and inner ear components:
```css
border-radius: 190%/190px 150px 0 0;
