# 📘 HTML Cheatsheet for Beginners

> A beginner-friendly guide to the most commonly used HTML elements and concepts.

---

## 🏁 Basic Structure
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
  </body>
</html>
```

---

## 🧱 Text Elements
```html
<h1> to <h6>                     # Headings
<p>Paragraph</p>
<strong>Bold</strong>
<em>Italic</em>
<br>                             # Line break
<hr>                             # Horizontal line
<pre>Preformatted text</pre>
<code>Inline code</code>
<blockquote>Quoted text</blockquote>
```

### 🔧 Common Attributes
These can be used on most HTML elements:
```html
class="classname"     # For styling with CSS
id="uniqueId"         # For targeting with CSS/JS
style="color: red;"   # Inline styling
title="Tooltip text"  # Shows on hover
hidden                # Hides the element
```

---

## 🔗 Links and Images
```html
<!-- Link Attributes -->
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Visit Site</a>  <!-- Opens in new tab safely -->

<!-- Image Attributes -->
<img src="image.jpg" alt="Description" width="200" height="150" title="Hover text">
```

---

## 📦 Lists
```html
<!-- Unordered List -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>

<!-- Ordered List -->
<ol>
  <li>First</li>
  <li>Second</li>
</ol>

<!-- Description List -->
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
</dl>
```

---

## 📁 Tables
```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ali</td>
      <td>25</td>
    </tr>
  </tbody>
</table>
```

---

## 📤 Forms
```html
<form action="/submit" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Enter your name" required maxlength="50">

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4" cols="50"></textarea>

  <label for="gender">Gender:</label>
  <select id="gender" name="gender">
    <option value="male">Male</option>
    <option value="female">Female</option>
    <option value="other">Other</option>
  </select>

  <input type="submit" value="Submit">
</form>
```

### 🏷️ Common Input Attributes
```html
placeholder="text"    # Shows hint text inside the input
required              # Makes input mandatory
maxlength="number"    # Sets maximum number of characters
value="default"       # Sets default value
disabled              # Makes input uneditable
readonly              # Cannot edit but value is visible
checked               # For checkboxes and radio buttons
selected              # For preselecting options in <select>
```

---

## 🧩 Input Types
```html
<input type="text">
<input type="email">
<input type="password">
<input type="checkbox">
<input type="radio">
<input type="date">
<input type="file">
<input type="number">
<input type="range">
<input type="search">
<input type="tel">
<input type="url">
```

---

## 🎨 Semantic Tags
```html
<header>
<nav>
<main>
<section>
<article>
<aside>
<footer>
<figure>
<figcaption>
<details>
<summary>
```

---

## ⚙️ Other Useful Tags
```html
<div>         # Generic container
<span>        # Inline container
<iframe>      # Embed another page
<video>       # Embed video
<audio>       # Embed audio
<canvas>      # For drawing graphics
<progress>    # Progress bar
<meter>       # Gauge indicator
<noscript>    # Fallback for no JS
<template>    # Hidden template content
```

---

## 📌 Best Practices
- Always use semantic tags for clarity.
- Add `alt` to images for accessibility.
- Use lowercase for tag names.
- Nest elements properly.
- Validate your HTML code.
- Use `label` with form inputs for accessibility.
- Avoid inline styles; use CSS instead.

---

> 🧠 Tip: Start small. Build simple pages first, then explore forms, multimedia, and advanced layouts.
