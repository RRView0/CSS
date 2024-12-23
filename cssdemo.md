# CSS Interview Questions with Examples

## 1. Basics of CSS

### Question:
What is the difference between inline, internal, and external CSS?

### Example:
```html
<!-- Inline CSS -->
<p style="color: blue;">This is inline CSS</p>

<!-- Internal CSS -->
<style>
  p {
    color: green;
  }
</style>
<p>This is internal CSS</p>

<!-- External CSS -->
<link rel="stylesheet" href="styles.css">
<p>This is external CSS</p>
```

---

## 2. Selectors

### Question:
How does the `>` selector work?

### Example:
```html
<style>
  div > p {
    color: red;
  }
</style>
<div>
  <p>Direct child paragraph</p>
  <div>
    <p>Nested paragraph</p>
  </div>
</div>
```
**Output:** Only the direct child paragraph is red.

---

## 3. Box Model

### Question:
What happens if `margin-top` and `margin-bottom` of two elements overlap?

### Example:
```html
<style>
  div {
    margin: 20px 0;
    background: lightgray;
  }
</style>
<div>Element 1</div>
<div>Element 2</div>
```
**Explanation:** The margin between the two divs will collapse to 20px instead of 40px.

---

## 4. Positioning and Layout

### Question:
How does `z-index` work?

### Example:
```html
<style>
  .box1 {
    position: absolute;
    z-index: 1;
    background: red;
    width: 100px;
    height: 100px;
  }
  .box2 {
    position: absolute;
    z-index: 2;
    background: blue;
    width: 100px;
    height: 100px;
    top: 50px;
    left: 50px;
  }
</style>
<div class="box1"></div>
<div class="box2"></div>
```
**Output:** The blue box will appear on top of the red box.

---

## 5. Responsive Design

### Question:
How do you create a responsive grid layout?

### Example:
```html
<style>
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 10px;
  }
  .box {
    background: lightblue;
    padding: 20px;
    text-align: center;
  }
</style>
<div class="container">
  <div class="box">1</div>
  <div class="box">2</div>
  <div class="box">3</div>
  <div class="box">4</div>
</div>
```
**Output:** Boxes adjust based on the screen size.

---

## 6. Transitions and Animations

### Question:
Write a simple animation to make an element fade in and move upwards.

### Example:
```html
<style>
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  .animated-box {
    animation: fadeInUp 1s ease-in-out;
    background: lightcoral;
    padding: 20px;
    text-align: center;
  }
</style>
<div class="animated-box">Hello, World!</div>
```

---

## 7. Advanced Concepts

### Question:
How can CSS variables help in a large project?

### Example:
```html
<style>
  :root {
    --main-color: #3498db;
    --padding: 10px;
  }
  .box {
    background: var(--main-color);
    padding: var(--padding);
    color: white;
  }
</style>
<div class="box">Using CSS Variables</div>
```

---

## 8. Cross-Browser Compatibility

### Question:
How do you handle vendor prefixes in CSS?

### Example:
```html
<style>
  .box {
    display: -webkit-flex; /* Safari */
    display: -ms-flexbox; /* IE10 */
    display: flex; /* Standard */
    justify-content: center;
  }
</style>
<div class="box">Cross-Browser Flexbox</div>
```

---

## 9. CSS Best Practices

### Question:
What is the BEM naming methodology?

### Example:
```html
<!-- Block -->
<div class="menu">
  <!-- Element -->
  <div class="menu__item">Item 1</div>
  <div class="menu__item">Item 2</div>
  <!-- Modifier -->
  <div class="menu__item menu__item--active">Item 3</div>
</div>
