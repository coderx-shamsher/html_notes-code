<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# Chapter: HTML Tables and Lists – Core Tags \& Types


***

## 1. HTML Table Tags (Essential Ones)

Tables are used to **display structured data** (like a spreadsheet) in rows and columns.[^1][^7]

### 1.1 Basic Table Tags

| Tag | Meaning / Role |
| :-- | :-- |
| `<table>` | Wraps the entire table. [^1][^7] |
| `<tr>` | A **table row**; contains cells in that row. [^3][^5] |
| `<td>` | A **data cell** (normal cell) in a row. [^1][^7] |
| `<th>` | A **header cell** (usually bold, centered; for column or row headings). [^1][^7] |

**Simple example:**

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Bob</td>
    <td>30</td>
  </tr>
</table>
```

Here:

- One `<table>` block.

```
- One `<tr>` for the header, two `<tr>` for the data rows.  
```

```
- Two `<th>` header cells and four `<td>` data cells.[^5][^1]
```


***

### 1.2 More Structured Table Tags

Modern tables often use structure tags for clarity and accessibility:[^7][^1]

```
- `<thead>` – wraps the **header rows** (with `<th>` usually).  
```

- `<tbody>` – wraps the **main data rows**.
- `<tfoot>` – wraps the **footer rows** (totals, summaries).
- `<caption>` – optional title above the table.

Example:

```html
<table>
  <caption>Employee Summary</caption>
  <thead>
    <tr>
      <th>Employee</th>
      <th>Department</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>Marketing</td>
      <td>₹50,000</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>Development</td>
      <td>₹70,000</td>
    </tr>
  </tbody>
</table>
```


***

### 1.3 Key Rules and Tips

```
- Every table **must** be inside `<table> ... </table>`.  
```

```
- Each row **must** be inside `<tr> ... </tr>`.  
```

```
- Each piece of data goes in `<td>`; headers should use `<th>`.[^1][^5]
```

✅ **Try This Yourself:**
Create a simple table with:

- One `<caption>`.

```
- One `<thead>` row with `<th>` cells.  
```

```
- Two or three `<tbody>` rows with `<td>` cells.  
```


***

## 2. HTML Lists – Types Overview

HTML supports **three main list types**, all built around the `<li>` tag.[^2][^6]


| Type | Tag Used | Typical Use Case |
| :-- | :-- | :-- |
| Unordered List | `<ul>` | Bulleted list; order doesn’t matter (e.g., features, menu items). [^6][^8] |
| Ordered List | `<ol>` | Numbered list; order matters (e.g., steps, rankings). [^6][^8] |
| Definition List | `<dl>` | Terms + descriptions (like a dictionary). [^2][^10] |


***

```
## 3. Unordered Lists: `<ul>`, `<li>`
```


### 3.1 Structure

```html
<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ul>
```

- `<ul>` = unordered (bulleted) list.

```
- `<li>` = list item (used inside both `<ul>` and `<ol>`).[^6][^8]
```

By default, items show with **bullets** (discs).

***

### 3.2 When To Use `<ul>`

- Features of a product.
- Links in a navigation menu.
- Any list where **sequence does not matter**.[^10][^6]

✅ **Example:**

```html
<ul>
  <li>Send emails</li>
  <li>Track tasks</li>
  <li>Generate reports</li>
</ul>
```


***

### 3.3 Try This Yourself

✅ **Exercise:**
Create an unordered list of “skills” or “hobbies” and style it with simple CSS if you want (e.g., `li { color: blue; }`).

***

```
## 4. Ordered Lists: `<ol>`, `<li>`
```


### 4.1 Structure

```html
<ol>
  <li>First step</li>
  <li>Second step</li>
  <li>Third step</li>
</ol>
```

- `<ol>` = ordered (numbered) list.
- `<li>` = list item.[^8][^6]

By default, items show as **numbers** (1, 2, 3…).

***

### 4.2 When To Use `<ol>`

- Step‑by‑step instructions.
- Rankings (top 10, top 5, etc.).
- Any list where **order is important**.[^6][^10]

✅ **Example:**

```html
<ol>
  <li>Open the browser.</li>
  <li>Go to the website.</li>
  <li>Click the button.</li>
</ol>
```


***

### 4.3 Try This Yourself

✅ **Exercise:**

```
Write an ordered list of “steps to make tea” using `<ol>` and `<li>`.  
```


***

```
## 5. Definition Lists: `<dl>`, `<dt>`, `<dd>`
```


### 5.1 Tags

- `<dl>` = definition list (the whole block).
- `<dt>` = **term** (the word or phrase).
- `<dd>` = **definition/description** for that term.[^2][^10]


### 5.2 Structure and Example

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language; used to create web pages.</dd>

  <dt>CSS</dt>
  <dd>Cascading Style Sheets; controls the look of web pages.</dd>
</dl>
```

Each `<dt>` is followed by one or more `<dd>` that describe it.
This is perfect for **glossaries, FAQs, or property lists**.[^10][^2]

***

### 5.3 Try This Yourself

✅ **Exercise:**
Make a mini glossary with at least three `<dt>` terms and their `<dd>` descriptions.

***

## 6. Nested Lists (Lists Inside Lists)

### 6.1 What “Nested” Means

A **nested list** is a list inside another list.
You can nest:

```
- `<ul>` inside `<ol>`  
```

```
- `<ol>` inside `<ul>`  
```

- Any list inside any other list.[^4][^2]


### 6.2 Example: Nested `<ul>` Inside `<ol>`

```html
<ol>
  <li>Step 1: Prepare ingredients
    <ul>
      <li>Flour</li>
      <li>Sugar</li>
      <li>Eggs</li>
    </ul>
  </li>
  <li>Step 2: Mix ingredients</li>
  <li>Step 3: Bake in oven</li>
</ol>
```

- Outer `<ol>` = main steps.
- Inner `<ul>` = ingredients inside the first step.[^4][^6]

***

### 6.3 Example: Nested `<ol>` Inside `<ul>`

```html
<ul>
  <li>Reading
    <ol>
      <li>Read the article</li>
      <li>Take notes</li>
      <li>Summarize</li>
    </ol>
  </li>
  <li>Practice</li>
  <li>Review</li>
</ul>
```

Here, the process inside “Reading” is ordered, while the top‑level items are bulleted.[^4][^10]

***

### 6.4 Rules for Nesting

```
- The nested `<ul>` or `<ol>` must be **inside** the `<li>` of the parent list.  
```

- Indent the HTML code for readability (e.g., inner list one level deeper).[^8][^4]

✅ **Try This Yourself:**

```
Create a main list of “habits to build” using `<ul>`, and pick one habit. Inside that habit, add a nested `<ol>` showing the steps to follow it.  
```


***

## 7. Quick Reference Table: All Tags Covered

| Purpose | Tag(s) Used | Key Notes |
| :-- | :-- | :-- |
| Full table | `<table>` | Wraps entire table. [^1][^7] |
| Table row | `<tr>` | One row per `<tr>`. [^3][^5] |
| Table header cell | `<th>` | Use for column/row headers. [^1][^7] |
| Table data cell | `<td>` | Contains normal table data. [^1][^7] |
| Table header block | `<thead>` | Groups header rows. [^1][^7] |
| Table body block | `<tbody>` | Groups main data rows. [^1][^7] |
| Table caption | `<caption>` | Optional title above the table. [^1][^9] |
| Unordered list | `<ul>` + `<li>` | Bullet‑style; order not important. [^6][^8] |
| Ordered list | `<ol>` + `<li>` | Numbered; order matters. [^6][^8] |
| Definition list | `<dl>` + `<dt>` + `<dd>` | Term + description pairs. [^2][^10] |
| Nested list | Any list inside `<li>` (e.g., `<ul>` in `<li>` of `<ol>`) | Use for sub‑structure. [^4][^6] |


***

In modern HTML, you’ll use **tables** mainly for **structured data** and **lists** for **menu items, features, steps, and definitions**.

```
- Use `<table>`, `<tr>`, `<th>`, `<td>`, and optionals `<thead>`, `<tbody>`, `<caption>` for **tables**.  
```

```
- Use `<ul>`, `<ol>`, `<dl>` with `<li>`, `<dt>`, `<dd>` for **lists and nested structures**.[^7][^1][^6]
```

<div align="center">⁂</div>

[^1]: https://www.w3schools.com/html/html_tables.asp

[^2]: https://www.studocu.com/in/document/jawaharlal-nehru-technological-university-hyderabad/html-css-bootstrap/lists/79038734

[^3]: https://mimo.org/glossary/html/table

[^4]: https://www.shiksha.com/online-courses/articles/html-lists-ordered-unordered-lists-with-examples/

[^5]: https://www.engr.colostate.edu/ets/html-table-tags/

[^6]: https://www.freecodecamp.org/news/html-lists-with-examples/

[^7]: https://www.programiz.com/html/table

[^8]: https://www.w3schools.com/html/html_lists_unordered.asp

[^9]: https://faculty.etsu.edu/tarnoff/ntes1710/tables/tables.htm

[^10]: https://elementor.com/blog/html-lists/

