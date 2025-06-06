# Frontend Mentor – QR Code Component Solution

This repository contains my solution to the [QR Code Component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). The goal was to build a pixel-perfect, responsive component that displays a styled QR code card—matching the exact colors, typography, and spacing from the official design.

---

## Table of Contents

- [Overview](#overview)  
  - [Screenshot](#screenshot)  
  - [Links](#links)  
- [My Process](#my-process)  
  - [Built With](#built-with)  
  - [What I Learned](#what-i-learned)  
  - [Continued Development](#continued-development)  
  - [Useful Resources](#useful-resources)  
- [Author](#author)  
- [Acknowledgments](#acknowledgments)  

---

## Overview

### Screenshot

![QR Code Component Preview](./screenshot.png)

> The screenshot above shows the final QR code card centered on a light‐blue background, with the correct HSL color values, “Outfit” typography, and responsive sizing.  

### Links

- **Solution URL:** [https://github.com/syariefazman/qr-code-component](https://github.com/syariefazman/qr-code-component)  
- **Live Site URL:** [https://syariefazman.github.io/qr-code-component/](https://syariefazman.github.io/qr-code-component/)  

---

## My Process

### Built With

- **Semantic HTML5** markup (proper use of `<header>`, `<main>`, `<footer>` semantics).  
- **CSS3**  
  - CSS custom properties for color variables (`--color-slate-300`, `--color-slate-500`, `--color-slate-900`, etc.).  
  - Flexbox for vertical and horizontal centering.  
  - Mobile‐first responsive layout (fluid width + `max-width` cap).  
- **Google Fonts – [Outfit](https://fonts.google.com/specimen/Outfit)** (weights 400 & 700).  
- **No JavaScript**—the component is purely HTML & CSS.

### What I Learned

- **Pixel‐Perfect Replication:** I practiced translating a Figma/PNG design layout into exact HSL-based CSS variables and correct `border-radius`, `box-shadow`, and `line-height` values.  
- **Responsive, Mobile-First Workflow:** By using `width: 90%; max-width: 320px;` on the card container, I ensured that on very narrow viewports the card still shrinks gracefully (down to ~320px or below), and on larger screens it remains centered and visually balanced.  
- **CSS Custom Properties:** Defining color variables at the top of `:root` made it trivial to reference and maintain the exact “Slate 300” (hsl(212, 45%, 89%)), “Slate 500” (hsl(216, 15%, 48%)), and “Slate 900” (hsl(218, 44%, 22%)) values throughout the stylesheet.  
- **Flexbox Centering:** Using `display: flex; flex-direction: column; align-items: center; justify-content: center;` on `<body>` guaranteed that the card and its attribution stack vertically and stay perfectly centered both horizontally and vertically.  

```css
:root {
  --color-white: hsl(0, 0%, 100%);
  --color-slate-300: hsl(212, 45%, 89%);
  --color-slate-500: hsl(216, 15%, 48%);
  --color-slate-900: hsl(218, 44%, 22%);
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: var(--color-slate-300);
  font-family: 'Outfit', sans-serif;
  min-height: 100vh;
  margin: 0;
}
