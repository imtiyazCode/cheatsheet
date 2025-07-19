# 🎨 CSS Cheatsheet

> A comprehensive CSS guide covering selectors, units, typography, transitions, animations, transforms (2D & 3D), variables, filters, clip-paths, and modern layouts.

---

## 📄 Basic Syntax
```css
selector {
  property: value;
}
```

---

## 🎯 CSS Selectors
- `*` – Universal selector
- `element` – All elements of that type (`p`, `h1`)
- `.class` – Class selector
- `#id` – ID selector
- `element.class` – Type + class
- `parent child` – Descendant selector
- `parent > child` – Direct child
- `element + sibling` – Adjacent sibling
- `[attr=value]` – Attribute selector
- `element:hover`, `:focus`, `:active`
- `element:first-child`, `:last-child`, `:nth-child(n)`
- `element::before`, `::after` – Pseudo-elements

---

## 📏 Units
- Absolute: `px`, `cm`, `mm`, `in`
- Relative: `%`, `em`, `rem`
- Viewport: `vh`, `vw`
- Fractional: `fr` (Grid)
- Time: `s`, `ms`

---

## 🖋️ Font Properties
```css
font-family: Arial, sans-serif;
font-size: 16px;
font-style: italic;
font-weight: bold;
line-height: 1.5;
letter-spacing: 2px;
```

---

## 📝 Text Properties
```css
text-align: left | center | right | justify;
text-transform: uppercase | lowercase | capitalize;
text-decoration: underline | none | line-through;
text-shadow: 1px 1px 2px gray;
white-space: nowrap | normal;
word-break: break-word;
```

---

## 🔗 List Styling
```css
list-style-type: disc | circle | square | none;
list-style-position: inside | outside;
list-style-image: url('bullet.png');
```

---

## 📌 Position
```css
position: static | relative | absolute | fixed | sticky;
top, right, bottom, left: values;
z-index: 100;
```

---

## 🖼️ Background Properties
```css
background-color: #f0f0f0;
background-image: url('image.jpg');
background-size: cover | contain;
background-position: center | top right;
background-repeat: no-repeat | repeat-x | repeat-y;
background-clip: border-box | padding-box | content-box;
background-attachment: fixed | scroll;
```

---

## 📦 Box Model & Properties
```css
width, height: values;
max-width, min-height: values;
padding, margin: values;
border: 2px solid #333;
border-radius: 8px;
box-sizing: border-box;
box-shadow: 2px 2px 10px rgba(0,0,0,0.2);
```

---

## ⚡ Transitions
```css
transition-property: none | all | color | background | transform;
transition-duration: 0.3s | 500ms;
transition-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n);
transition-delay: 0s | 200ms;
transition: property duration timing-function delay;
```

---

## 🎬 Animations
```css
animation-name: slideIn | none;
animation-duration: 1s;
animation-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n);
animation-delay: 0s;
animation-iteration-count: 1 | infinite | number;
animation-direction: normal | alternate;
animation-fill-mode: none | forwards | backwards | both;
animation-play-state: running | paused;

@keyframes slideIn {
  from { transform: translateX(-100%); }
  to { transform: translateX(0); }
}

.element {
  animation: slideIn 1s ease-in-out 0s infinite alternate;
}
```

**Shorthand:**
```css
animation: name duration timing-function delay iteration-count direction;
```

---

## 🔄 2D Transforms
```css
transform: translate(x, y);      /* Move element */
transform: rotate(angle);        /* Rotate element */
transform: scale(x, y);          /* Scale element */
transform: skew(x-angle, y-angle); /* Skew element */
transform: skewX(angle);         /* Skew along X-axis */
transform: skewY(angle);         /* Skew along Y-axis */
```

## 🔄 3D Transforms
```css
transform: translate3d(x, y, z); /* Move element in 3D */
transform: rotateX(angle);       /* Rotate around X-axis */
transform: rotateY(angle);       /* Rotate around Y-axis */
transform: rotateZ(angle);       /* Rotate around Z-axis */
transform: scale3d(x, y, z);     /* Scale in 3D */
transform: perspective(value);   /* Perspective view */
```

---

## 🎛️ CSS Variables (Custom Properties)
```css
:root {
  --main-color: #3498db;
  --padding: 10px;
}

.box {
  color: var(--main-color);
  padding: var(--padding);
}

/* Fallback value */
color: var(--secondary-color, #333);
```

---

## 🌫️ Filter & Backdrop Filter
```css
filter: blur(5px) | brightness(1.2) | contrast(150%) | grayscale(100%) | sepia(80%) | hue-rotate(90deg);
backdrop-filter: blur(10px) | brightness(1.1) | saturate(120%);
```

---

## ✂️ Clip-Path Examples
```css
clip-path: circle(50%);
clip-path: ellipse(60% 40%);
clip-path: inset(10px 20px 30px 40px);
clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
```

---

## 📐 Flexbox
```css
.container {
  display: flex;
  flex-direction: row | column;
  justify-content: center | space-between | space-around | flex-start | flex-end;
  align-items: center | flex-start | flex-end | stretch;
  flex-wrap: nowrap | wrap;
  gap: 10px;
}
```

---

## 🕸️ Grid
```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto;
  gap: 10px;
  justify-items: center;
  align-items: start;
}
```

---

## 🎨 Colors
- Named: `red`, `blue`
- Hex: `#ff0000`
- RGB: `rgb(255,0,0)`
- RGBA: `rgba(255,0,0,0.5)`
- HSL: `hsl(0, 100%, 50%)`

---

## 📱 Media Queries
```css
@media (max-width: 768px) {
  body { background-color: lightblue; }
}
```

---

## ⚙️ Misc Properties
```css
cursor: pointer;
opacity: 0.8;
overflow: hidden | auto | scroll;
object-fit: cover | contain;
clip-path: circle(50%);
```

---

## 📌 Best Practices
- Use classes for reusable styles.
- Use external `.css` files.
- Prefer `rem` and `em` over `px` for responsiveness.
- Use Flexbox and Grid for modern layouts.
- Utilize CSS variables for consistency.

---

## 📚 Resources
- [MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [CSS Tricks](https://css-tricks.com/)
- [Can I Use](https://caniuse.com/)
- [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/)
- [Flexbox Guide - CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Grid Guide - CSS Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)

---

> **Tip:** Use browser dev tools for live CSS editing.
