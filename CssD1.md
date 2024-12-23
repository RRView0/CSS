# CSS Interview Questions with Examples

## Key Concepts of CSS

### 1. Basics of CSS
- **CSS Syntax**: Selectors, Properties, and Values.
- **Types of CSS**: Inline, Internal, and External.
- **CSS Comments**: `/* This is a comment */`.

---

### 2. Selectors
- **Universal Selector**: `* { margin: 0; }`
- **Type Selector**: `p { color: blue; }`
- **Class Selector**: `.class-name { font-size: 14px; }`
- **ID Selector**: `#id-name { text-align: center; }`
- **Attribute Selector**: `input[type="text"] { background: lightgray; }`
- **Combinators**:
  - Descendant Selector: `div p`
  - Child Selector: `div > p`
  - Adjacent Sibling Selector: `h1 + p`
  - General Sibling Selector: `h1 ~ p`

---

### 3. Box Model
- Components: `margin`, `border`, `padding`, `content`.
- `box-sizing`: 
  - `content-box`: Default.
  - `border-box`: Includes padding and border in width/height.

---

### 4. Positioning and Layout
- **Position Property**:
  - `static` (default), `relative`, `absolute`, `fixed`, `sticky`.
- **Float and Clear**:
  - Float: `float: left;`
  - Clear: `clear: both;`
- **Flexbox**:
  - Parent: `display: flex;`
  - Properties: `justify-content`, `align-items`, `flex-direction`.
- **Grid**:
  - Parent: `display: grid;`
  - Properties: `grid-template-columns`, `grid-template-rows`.

---

### 5. Responsive Design
- Media Queries: 
  ```css
  @media (max-width: 600px) {
    body {
      font-size: 14px;
    }
  }
  ```
- Fluid Layouts: `width: 100%;`
- Responsive Units: `em`, `rem`, `%`, `vw`, `vh`.

---

### 6. Typography
- Font Properties: `font-family`, `font-size`, `font-weight`, `line-height`.
- Text Properties: `text-align`, `text-decoration`, `text-transform`.

---

### 7. Transitions and Animations
- **Transitions**:
  ```css
  button {
    transition: background 0.3s ease;
  }
  button:hover {
    background: blue;
  }
  ```
- **Keyframes Animations**:
  ```css
  @keyframes example {
    0% { transform: translateX(0); }
    100% { transform: translateX(100px); }
  }
  ```

---

### 8. Colors and Backgrounds
- Color Models: Hex (`#ffffff`), RGB (`rgb(255,255,255)`), HSL (`hsl(0, 0%, 100%)`).
- Background Properties: `background-color`, `background-image`, `background-size`, `background-repeat`.

---

### 9. Advanced Concepts
- **CSS Variables**:
  ```css
  :root {
    --primary-color: #3498db;
  }
  ```
- **Pseudo-Classes**: `:hover`, `:nth-child()`, `:focus`.
- **Pseudo-Elements**: `::before`, `::after`.
- **Custom Properties**: Dynamic theming with variables.

---

### 10. Cross-Browser Compatibility
- Vendor Prefixes: `-webkit-`, `-moz-`, `-ms-`.
- Tools: Autoprefixer, Can I Use.

---

### 11. CSS Preprocessors
- Popular Tools: SASS, LESS.
- Features: Nesting, Variables, Mixins.

---

### 12. Accessibility
- Focus Indicators: `:focus`.
- High Contrast Mode: Use relative units for font sizes.

---

### 13. CSS Best Practices
- BEM (Block Element Modifier): `.block__element--modifier`.
- Avoid Overly Specific Selectors.
- Use Reset or Normalize CSS.

---

### 14. Debugging Tools
- Browser DevTools: Inspect and test CSS.
- Validators: [W3C CSS Validator](https://jigsaw.w3.org/css-validator/).

---

## Examples

### 1. Inline, Internal, and External CSS
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

### 2. Box Model Margin Collapse
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

### 3. Responsive Grid Layout
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

### 4. Keyframes Animation Example
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
