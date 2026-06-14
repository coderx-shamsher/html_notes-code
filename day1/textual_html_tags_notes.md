# HTML Textual Tags — 🧱

HTML textual tags are used to display and structure **text content** on webpages.

These tags help browsers understand:

* headings
* paragraphs
* formatting
* emphasis
* quotations
* code
* lists
* semantic meaning

---

# What Are Textual Tags?

Textual tags are HTML elements used for:

```text id="2gbq52"
Displaying
Formatting
Structuring
Emphasizing
Organizing
Text Content
```

---

# Why Textual Tags Matter

Without proper textual tags:

❌ webpages become messy
❌ SEO becomes weak
❌ accessibility suffers
❌ screen readers fail
❌ structure becomes confusing

---

# Browser Mental Model 🧠

Browser reads HTML like this:

```text id="mjyn84"
Tag Meaning
     ↓
Browser Understands Structure
     ↓
Browser Displays Properly
```

---

# Categories of HTML Textual Tags

| Category        | Purpose                 |
| --------------- | ----------------------- |
| Headings        | Titles                  |
| Paragraph Tags  | Text blocks             |
| Formatting Tags | Styling meaning         |
| Semantic Tags   | Text importance         |
| Quotation Tags  | Quotes/citations        |
| Code Tags       | Programming text        |
| List Tags       | Ordered/unordered items |
| Break Tags      | Line spacing            |

---

# PART 1 — HEADING TAGS 🏷️

# What Are Heading Tags?

Heading tags define titles and sections.

HTML provides:

```text id="kdn3ga"
<h1> to <h6>
```

---

# Syntax

```html id="9xutv5"
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Small Heading</h3>
```

---

# Example

```html id="7pdw0v"
<h1>My Website</h1>
<h2>Frontend Development</h2>
<h3>HTML Basics</h3>
```

---

# Output Structure

```text id="4x4w1u"
H1 → Biggest
H2 → Smaller
H3 → Smaller
H6 → Smallest
```

---

# Real-World Example

```html id="f1h52t"
<h1>Amazon</h1>

<h2>Electronics</h2>
<h3>Mobiles</h3>

<h2>Fashion</h2>
<h3>Men Clothing</h3>
```

---

# Best Practices ✅

| Practice                   | Why              |
| -------------------------- | ---------------- |
| Use only one h1            | SEO clarity      |
| Maintain hierarchy         | Better structure |
| Don’t skip levels randomly | Accessibility    |

GOOD:

```html id="kp3b4r"
<h1>Main</h1>
<h2>Section</h2>
<h3>Subsection</h3>
```

BAD:

```html id="y3vln6"
<h1>Main</h1>
<h4>Wrong Jump</h4>
```

---

# PART 2 — PARAGRAPH TAG `<p>` 📄

# Purpose

Used for paragraphs or blocks of text.

---

# Syntax

```html id="yzpjsu"
<p>This is a paragraph.</p>
```

---

# Example

```html id="8j9r7d"
<p>
HTML is used to create webpage structure.
</p>
```

---

# Browser Behavior

Browser automatically adds spacing before and after paragraphs.

---

# Common Mistake ❌

Using `<br>` repeatedly instead of paragraphs.

BAD:

```html id="svj6d1"
Hello
<br><br><br>
World
```

GOOD:

```html id="lg6pzi"
<p>Hello</p>
<p>World</p>
```

---

# PART 3 — LINE BREAK TAG `<br>` ↩️

# Purpose

Creates a new line.

---

# Syntax

```html id="pmum7g"
<br>
```

---

# Example

```html id="08o9o8"
Hello<br>
World
```

Output:

```text id="h8l7bh"
Hello
World
```

---

# When to Use

✅ addresses
✅ poems
✅ short line breaks

---

# When NOT to Use ❌

❌ layout spacing
❌ creating large gaps

Use CSS instead.

---

# PART 4 — HORIZONTAL LINE `<hr>` ➖

# Purpose

Creates thematic separation.

---

# Example

```html id="g0r85u"
<p>Section 1</p>

<hr>

<p>Section 2</p>
```

---

# Real Use Cases

* separating article sections
* separating content blocks
* visual division

---

# PART 5 — STRONG IMPORTANCE `<strong>` 💪

# Purpose

Defines important text.

---

# Syntax

```html id="e92y5u"
<strong>Important</strong>
```

---

# Output

Usually bold.

BUT:

⚠️ Important point:

`<strong>` is semantic, not just visual.

It tells browser:

> “This text is important.”

---

# Example

```html id="e42k4s"
<p>
Do not share your
<strong>password</strong>.
</p>
```

---

# Difference Between `<strong>` and `<b>`

| Tag    | Meaning           |
| ------ | ----------------- |
| strong | important meaning |
| b      | visual bold only  |

---

# PART 6 — BOLD TAG `<b>` 🔠

# Purpose

Makes text bold visually.

---

# Example

```html id="0h5l2m"
<b>Bold Text</b>
```

---

# Important Difference

```text id="7y1g4g"
<strong> = semantic importance
<b>       = visual styling
```

---

# PART 7 — EMPHASIS `<em>` 📢

# Purpose

Emphasized text.

Usually italic.

---

# Example

```html id="8l0o7d"
<em>Very important note</em>
```

---

# Semantic Meaning

Browser understands:

> “This text should be stressed.”

---

# Difference Between `<em>` and `<i>`

| Tag | Meaning       |
| --- | ------------- |
| em  | emphasis      |
| i   | visual italic |

---

# PART 8 — ITALIC TAG `<i>` ✍️

# Purpose

Italic text visually.

---

# Example

```html id="o0k6q2"
<i>Movie Name</i>
```

---

# Common Real Uses

* book titles
* foreign words
* technical terms

---

# PART 9 — UNDERLINE `<u>` 📏

# Example

```html id="ckkl30"
<u>Underlined Text</u>
```

---

# Important Note ⚠️

Avoid excessive underline.

Why?

Users may think it is a link.

---

# PART 10 — MARK TAG `<mark>` 🟨

# Purpose

Highlights text.

---

# Example

```html id="c1qpcj"
<p>
Learn <mark>HTML</mark> first.
</p>
```

---

# Real Use Cases

* search highlighting
* important notes
* keywords

---

# PART 11 — SMALL TAG `<small>` 🔍

# Purpose

Displays smaller text.

---

# Example

```html id="mr7v3m"
<small>Terms and conditions apply.</small>
```

---

# Real Uses

* copyright
* disclaimers
* secondary info

---

# PART 12 — DELETE TAG `<del>` ❌

# Purpose

Represents deleted text.

---

# Example

```html id="s0ahmu"
<p>
Price:
<del>₹999</del>
₹499
</p>
```

---

# Output

Shows strike-through text.

---

# PART 13 — INSERTED TEXT `<ins>` ✅

# Purpose

Represents inserted text.

---

# Example

```html id="f0n8kq"
<ins>New Feature Added</ins>
```

---

# PART 14 — SUBSCRIPT `<sub>` 🧪

# Purpose

Displays text lower.

---

# Example

```html id="8clujy"
H<sub>2</sub>O
```

Output:

```text id="abx2q8"
H₂O
```

---

# PART 15 — SUPERSCRIPT `<sup>` 🔢

# Purpose

Displays text above.

---

# Example

```html id="utq8l0"
2<sup>2</sup>
```

Output:

```text id="hpfh8t"
2²
```

---

# PART 16 — PRE TAG `<pre>` 📦

# Purpose

Preserves formatting and spaces.

---

# Example

```html id="ls92mx"
<pre>
Name : John
Age  : 20
</pre>
```

---

# Browser Normally Removes Extra Spaces

Without `<pre>`:

```html id="9isrku"
Hello      World
```

Output:

```text id="lpzjlwm"
Hello World
```

---

# `<pre>` Preserves It

---

# PART 17 — CODE TAG `<code>` 💻

# Purpose

Displays programming code.

---

# Example

```html id="vt4ffw"
<code>console.log("Hello")</code>
```

---

# Real Use Cases

* documentation
* tutorials
* technical blogs

---

# PART 18 — KEYBOARD INPUT `<kbd>` ⌨️

# Purpose

Represents keyboard keys.

---

# Example

```html id="gq6f42"
<kbd>Ctrl</kbd> + <kbd>C</kbd>
```

Output:

```text id="ivd4ml"
Ctrl + C
```

---

# PART 19 — VARIABLE TAG `<var>` 🧮

# Purpose

Represents variables.

---

# Example

```html id="zh0wba"
<var>x</var> + <var>y</var>
```

---

# PART 20 — SAMPLE OUTPUT `<samp>` 🖥️

# Purpose

Represents program output.

---

# Example

```html id="x7l00z"
<samp>Hello User</samp>
```

---

# PART 21 — BLOCKQUOTE `<blockquote>` 🧾

# Purpose

Large quotation block.

---

# Example

```html id="i9clzc"
<blockquote>
Learning never stops.
</blockquote>
```

---

# Real Uses

* quotes
* testimonials
* citations

---

# PART 22 — INLINE QUOTE `<q>` 💬

# Example

```html id="hkhh3s"
<q>Practice daily</q>
```

Output:

```text id="ukn2m5"
"Practice daily"
```

---

# PART 23 — ABBREVIATION `<abbr>` 📘

# Purpose

Represents abbreviations.

---

# Example

```html id="ji6cwu"
<abbr title="HyperText Markup Language">
HTML
</abbr>
```

Hover shows full meaning.

---

# PART 24 — ADDRESS TAG `<address>` 📍

# Purpose

Represents contact information.

---

# Example

```html id="m9tzp7"
<address>
Delhi, India
</address>
```

---

# PART 25 — SPAN TAG `<span>` 🎯

# VERY IMPORTANT

# Purpose

Inline container for styling small text portions.

---

# Example

```html id="d0x3jx"
<p>
Hello <span style="color:red">World</span>
</p>
```

---

# Why `<span>` Matters

Used heavily with:

* CSS
* JavaScript
* dynamic UI

---

# Difference Between `<div>` and `<span>`

| Tag  | Type   |
| ---- | ------ |
| div  | block  |
| span | inline |

---

# Semantic vs Non-Semantic Tags 🧠

| Semantic   | Non-Semantic |
| ---------- | ------------ |
| strong     | b            |
| em         | i            |
| blockquote | div          |
| address    | span         |

---

# MOST IMPORTANT TEXTUAL TAGS 🚀

If beginner:

Master these first:

| Priority  | Tags       |
| --------- | ---------- |
| VERY HIGH | h1-h6      |
| VERY HIGH | p          |
| VERY HIGH | strong     |
| VERY HIGH | em         |
| VERY HIGH | span       |
| HIGH      | br         |
| HIGH      | hr         |
| HIGH      | code       |
| HIGH      | blockquote |

---

# Real Website Example 🌍

Example blog article:

```html id="zjlwm8"
<h1>Learn HTML</h1>

<p>
HTML is the structure of the web.
</p>

<p>
Use <strong>semantic tags</strong>
for better accessibility.
</p>

<blockquote>
Practice daily to improve.
</blockquote>

<p>
Press <kbd>Ctrl</kbd> + <kbd>S</kbd>
to save.
</p>
```

---

# Common Beginner Mistakes ❌

| Mistake                    | Problem             |
| -------------------------- | ------------------- |
| Using `<br>` for layout    | Bad practice        |
| Using `<b>` everywhere     | No semantic meaning |
| Ignoring heading hierarchy | SEO issues          |
| Overusing `<span>`         | Messy code          |
| Not using semantic tags    | Poor accessibility  |

---

# Best Practices ✅

| Practice                      | Why                |
| ----------------------------- | ------------------ |
| Prefer semantic tags          | Better structure   |
| Use headings properly         | SEO + readability  |
| Use `<strong>` for importance | Accessibility      |
| Use `<code>` for code         | Proper meaning     |
| Keep HTML clean               | Easier maintenance |

---

# HTML Textual Tags Mind Map 🧠

```text id="69j2r5"
Textual Tags
│
├── Structure
│   ├── h1-h6
│   └── p
│
├── Formatting
│   ├── strong
│   ├── em
│   ├── b
│   ├── i
│   └── mark
│
├── Code
│   ├── code
│   ├── pre
│   ├── kbd
│   └── samp
│
├── Quotes
│   ├── q
│   └── blockquote
│
└── Utility
    ├── br
    ├── hr
    ├── span
    └── small
```

---

# Quick Revision Notes 📝

| Tag        | Purpose             |
| ---------- | ------------------- |
| h1-h6      | headings            |
| p          | paragraph           |
| br         | line break          |
| hr         | separator           |
| strong     | important text      |
| em         | emphasis            |
| b          | bold                |
| i          | italic              |
| mark       | highlight           |
| code       | code text           |
| pre        | preserve formatting |
| span       | inline styling      |
| blockquote | large quote         |
| q          | inline quote        |

---

# Golden Rule 🚀

```text id="v06j7d"
HTML is not just about appearance.

HTML gives MEANING to content.
```

That meaning helps:

* browsers
* SEO
* accessibility tools
* screen readers
* developers
* search engines
* maintainability
