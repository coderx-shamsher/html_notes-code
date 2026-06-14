<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# Chapter: HTML Standard Attributes – `class`, `id`, `data-*`, and `style`


***

## 1. What Are Standard / Global Attributes?

In HTML, **global attributes** are attributes that can be used on **almost any element**, not just one specific tag.[^3][^6]

The most important ones for beginners are:

- `class`
- `id`
- `style`
- `data-*` (custom data attributes)

They help you **style**, **select**, and **extend** elements in clean, modern HTML.[^7][^3]

***

## 2. The `class` Attribute

### 2.1 What `class` Does

- `class` assigns **one or more class names** to an element.
- Multiple elements can share the same `class`.
- It is used mainly for **CSS styling** and **JavaScript selection**.

Example:

```html
<p class="intro-text">Welcome to my site.</p>
<button class="btn btn-primary">Click me</button>
```

- `intro-text` can be styled with CSS.
- `btn btn-primary` are two classes on the same element (button).[^2][^7]

***

### 2.2 Why `class` Matters

- **Reusable styles:**

```css
.intro-text {
  color: #2c3e50;
  font-size: 18px;
}
```

Every element with `class="intro-text"` gets this style.
- **JavaScript hooks:**

```js
document.querySelectorAll(".btn")
```

Selects all elements with class `btn`.
- Unlike `id`, a `class` name **does not need to be unique**; you can reuse it as much as you want.[^2][^3]

***

### 2.3 Rules and Best Practices

- Separate multiple classes with a **space**:

```html
<div class="card card-hover"></div>
```

- Use **meaningful, readable** names:
    - `btn`, `btn-primary`, `card`, `nav-link`.
- Avoid generic names like `red` or `big`; prefer `error` or `highlight` instead.[^1][^7]

✅ **Try This Yourself:**

```
- Add `class="highlight"` to a `<p>` and then style it in a `<style>` tag or CSS file.  
```


***

### Key Takeaways – Section 2

- `class` = **reusable** label for elements.
- Used for **CSS** and **JavaScript selection**.
- Can be repeated on many elements; use readable, semantic names.[^7][^2]

***

## 3. The `id` Attribute

### 3.1 What `id` Does

- `id` gives an element a **unique identifier** on the page.
- Every `id` must be **unique within the document**.
- Used to:
    - Style a **single** element with CSS.
    - Select or manipulate an element with JavaScript.
    - Create **page anchors** (e.g., `#section1`).[^4][^2]

Example:

```html
<h1 id="main-title">Main Title</h1>
<button id="start-button">Start</button>
```


***

### 3.2 CSS and JavaScript Usage

- **CSS selector with `id`:**

```css
#main-title {
  background-color: lightblue;
  padding: 20px;
}
```

- **JavaScript selection:**

```js
document.getElementById("start-button")
```


Note: `id` values are **case sensitive**; `MainTitle` is different from `maintitle`.[^3][^2]

***

### 3.3 Rules for `id`

- Must be **unique** on the page.
- Must not contain **spaces**; use hyphens or underscores instead:
    - `id="main-title"` ✅
    - `id="main title"` ❌
- Must be **at least one character** long.[^4][^3]

⚠️ Bad practice (duplicate IDs):

```html
<div id="alert">Alert 1</div>
<div id="alert">Alert 2</div>
```

This breaks CSS and JavaScript predictability.

***

### 3.4 When to Use `id` vs `class`

| Case | Use `id` | Use `class` |
| :-- | :-- | :-- |
| One unique element (e.g., main heading, login form) | ✅ | ❌ |
| Multiple similar elements (e.g., buttons, cards, links) | ❌ | ✅ |
| CSS that applies to **only one** element | ✅ | ❌ |
| CSS that applies to **many** elements | ❌ | ✅ |

[^2][^7]

***

### Key Takeaways – Section 3

- `id` = **unique** identifier for one element.
- Used for **specific styling**, **JavaScript selection**, and **page anchors**.
- Must be unique, no spaces, and case‑sensitive.[^4][^2]

***

## 4. Inline `style` Attribute

### 4.1 What `style` Does

- `style` lets you add **inline CSS** directly inside an HTML element.
- Format:

```html
<p style="color: red; font-size: 16px;">Red text</p>
```


Here, `color: red;` and `font-size: 16px;` are CSS declarations written inline.[^6][^1]

***

### 4.2 When To Use `style`

✅ **Acceptable uses:**

- Quick prototyping or learning.
- One‑off styles that are truly unique and unlikely to repeat.

❌ **Avoid in production code:**

- Writing long CSS rules inline.
- Repeating the same style on many elements.

Better pattern:

```html
<p class="error-message">Something went wrong.</p>
```

```css
.error-message {
  color: red;
  font-weight: bold;
}
```

This keeps **HTML** clean and **CSS** reusable.[^1][^6]

***

### 4.3 Try This Yourself

✅ **Exercise:**
Temporarily experiment with `style`:

```html
<h1 style="text-align: center; color: purple;">Centered Purple Title</h1>
<p style="background: #f0f0f0; padding: 10px;">
  This has inline background and padding.
</p>
```

Then refactor it later by moving styles into a CSS class.

***

### Key Takeaways – Section 4

- `style` = **inline CSS** for one element.
- Useful for **fast testing**, not for large, reusable styles.
- Prefer **external or internal CSS classes** for maintainable code.[^6][^1]

***

## 5. Custom Data Attributes: `data-*`

### 5.1 What `data-*` Is

`data-*` attributes let you store **custom data private to the page or application**.

- `*` means you can choose your own name:
    - `data-user-id`
    - `data-price`
    - `data-category`

Example:

```html
<div class="product" 
     data-user-id="5678" 
     data-price="299" 
     data-category="electronics">
  Smartphone
</div>
```

These attributes do **not affect rendering** but are perfect for **JavaScript**.[^9][^7]

***

### 5.2 Why `data-*` Matters

- Store **extra info** that is not visible on the screen.
- Used heavily in **single‑page apps (SPA)**, CMS blocks, and components.
- Popular alternatives to using `id` or `class` for **non‑CSS data**.[^9][^7]

Example in JavaScript:

```js
const product = document.querySelector(".product");
const userId = product.dataset.userId;   // "5678"
const price  = product.dataset.price;    // "299"
```

Note: `data-user-id` becomes `dataset.userId` in JavaScript (camelCase).[^9]

***

### 5.3 Rules for `data-*`

- Name must start with `data-`.
- Use lowercase letters and hyphens:

```html
data-product-name
data-is-active
```

- No spaces or special characters (besides `-` and letters/numbers).[^7][^9]

***

### 5.4 Try This Yourself

✅ **Exercise:**
Create a “product card” and add `data-*` attributes:

```html
<div class="card" 
     data-product-id="42" 
     data-stock="10" 
     data-discount="true">
  <h3>Widget X</h3>
  <p>Only 10 left in stock.</p>
</div>
```

Then open the browser’s DevTools and inspect the element to see the `data-` fields.

***

### Key Takeaways – Section 5

- `data-*` = custom data for JavaScript, not for styling.
- Use for storing extra info like IDs, prices, flags, etc.
- Access them in JS via `element.dataset.*`.[^7][^9]

***

## 6. Quick Reference Table: Standard Attributes

| Attribute | Scope | Main Use |
| :-- | :-- | :-- |
| `class` | Global | Reusable CSS class; group multiple elements. [^2][^7] |
| `id` | Global | Unique identifier; one per element; CSS + JS + anchors. [^2][^4] |
| `style` | Presentational | Inline CSS on one element (use sparingly). [^1][^6] |
| `data-*` | Global | Store custom application data (for JavaScript). [^7][^9] |


***

These four attributes (`class`, `id`, `style`, and `data-*`) are **core tools** you’ll use in almost every modern HTML project:

- `class` for **grouping and styling**.
- `id` for **one‑off identification**.
- `style` for **rare inline styles**.
- `data-*` for **custom data** tied to elements.[^3][^9]
<span style="display:none">[^5][^8]</span>

<div align="center">⁂</div>

[^1]: https://www.almabetter.com/bytes/tutorials/html/global-attributes-in-html

[^2]: https://www.w3schools.com/html/html_id.asp

[^3]: https://web.dev/learn/html/attributes

[^4]: https://www.w3.org/TR/2011/WD-html5-20110525/elements.html

[^5]: https://www.linkedin.com/posts/kedari-anegondi-ab250319b_html-webdevelopment-frontenddeveloper-activity-7410634478504710144-eLtl

[^6]: https://tutorial.techaltum.com/attribute.html

[^7]: https://www.codewithharry.com/tutorial/html-attributes

[^8]: http://www.w3schools.com/htmL/html_attributes.asp

[^9]: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes

