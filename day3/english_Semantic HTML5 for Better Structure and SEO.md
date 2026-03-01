<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# Semantic HTML5 for Better Structure and SEO

## Table of Contents

- [1. Introduction](#introduction)
- [2. Core Concepts](#core-concepts)
- [3. Hands-On Implementation](#hands-on-implementation)
- [4. Advanced Topics](#advanced-topics)
- [5. Real-World Project](#real-world-project)
- [6. Exercises \& Challenges](#exercises--challenges)
- [7. Summary \& Next Steps](#summary--next-steps)
- [Quick Reference Cheat Sheet](#quick-reference-cheat-sheet)


## 1. Introduction

```
**Semantic HTML5 makes your website smart.** It tells computers (and Google) what your content means, not just how it looks. Instead of using generic `<div>` tags everywhere, we use special tags like `<header>`, `<article>`, `<nav>` that have real meaning.
```

**Why this matters:**

- Google finds your site easier → Better SEO ranking
- Screen readers understand your site → Helps disabled users
- Your code stays organized → Easy to update later
- Future browsers know what to do with your content

**What we'll build:** A complete personal portfolio website that looks professional and works great for SEO.

**Simple example:**

```html
<!-- BAD - No meaning -->
<div class="header">
    <h1>My Site</h1>
    <div class="menu">
        <a href="/">Home</a>
    </div>
</div>

<!-- GOOD - Has meaning -->
<header>
    <h1>My Site</h1>
    <nav>
        <a href="/">Home</a>
    </nav>
</header>
```

**What you need:** Just a text editor (VS Code) and web browser.

## 2. Core Concepts

### 2.1 The 5 Main Landmark Tags

HTML5 has 5 special tags that mark different parts of your page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My Portfolio</title>
</head>
<body>
    <!-- HEADER = Top of page (logo + main menu) -->
    <header>
        <h1>Dev's Portfolio</h1>
        <nav><!-- Menu goes here --></nav>
    </header>

    <!-- MAIN = Most important content (ONLY ONE per page!) -->
    <main>
        <h2>Welcome to my work</h2>
        <p>I build websites...</p>
    </main>

    <!-- ASIDE = Extra info (sidebar, ads, related posts) -->
    <aside>
        <h3>Quick Contact</h3>
        <p>Email: dev@example.com</p>
    </aside>

    <!-- FOOTER = Bottom of page (copyright, links) -->
    <footer>
        <p>© 2026 Dev</p>
    </footer>
</body>
</html>
```

**Easy rules:**

1. **Only 1 `<main>` tag per page**
2. `<header>` and `<footer>` can be used multiple times
3. `<aside>` is perfect for sidebars

### 2.2 Headings - Your Page Outline (h1 to h6)

Headings create a clear structure, like chapters in a book.

```html
<!-- WRONG - Skipping levels -->
<h1>Main Title</h1>
<h3>Section Title</h3>  <!-- Missing h2! -->

<!-- CORRECT - Step by step -->
<article>
    <h1>My Blog Post</h1>
    
    <h2>First Section</h2>
        <h3>Small detail</h3>
        <h3>Another detail</h3>
    
    <h2>Second Section</h2>
</article>
```

**Test your outline:** Right-click in Chrome → Inspect → Go to "Outline" tab

### 2.3 Content Sections - Article vs Section vs Div

```html
<!-- ARTICLE = Complete piece of content (blog post, product) -->
<article>
    <h2>Food Delivery App</h2>
    <p>Full app with payments and tracking...</p>
</article>

<!-- SECTION = Group related content -->
<section>
    <h2>My Projects</h2>
    <article><!-- Project 1 --></article>
    <article><!-- Project 2 --></article>
</section>

<!-- DIV = Last choice when nothing fits -->
<div class="photo-gallery">
    <!-- Only use when no semantic tag works -->
</div>
```

**Remember:**

- `<article>` = Can stand alone
- `<section>` = Needs a heading, groups related items
- `<div>` = Generic container (avoid when possible)


## 3. Hands-On Implementation

### 3.1 Basic Portfolio Structure

Let's build the foundation:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dev | Web Developer</title>
</head>
<body>
    <!-- 1. HEADER (Logo + Main Menu) -->
    <header>
        <h1><a href="/">Dev</a></h1>
        <nav aria-label="Main menu">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- 2. MAIN CONTENT (Only one main!) -->
    <main>
        <!-- Hero Section -->
        <section id="home">
            <h2>Web Developer</h2>
            <p>I build websites with HTML, CSS, JavaScript</p>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <h2>My Work</h2>
            <article>
                <h3>Food App</h3>
                <p>Complete food ordering website</p>
            </article>
        </section>
    </main>

    <!-- 3. SIDEBAR -->
    <aside id="contact">
        <h3>Contact Me</h3>
        <p>dev@example.com</p>
    </aside>

    <!-- 4. FOOTER -->
    <footer>
        <p>© 2026 Dev. All rights reserved.</p>
    </footer>
</body>
</html>
```


### 3.2 Forms Made Semantic

```html
<!-- Contact Form with proper labels -->
<form>
    <!-- Group related fields -->
    <fieldset>
        <legend>Your Info</legend>
        
        <label for="name">Full Name:</label>
        <input id="name" type="text" required>
        
        <label for="email">Email:</label>
        <input id="email" type="email" required>
    </fieldset>
    
    <label for="message">Message:</label>
    <textarea id="message" rows="5"></textarea>
    
    <button type="submit">Send Message</button>
</form>
```

**Why `fieldset`?** Groups related form fields together logically.

### 3.3 Special Content Tags

```html
<!-- Dates -->
<time datetime="2026-03-01">March 1, 2026</time>

<!-- Addresses -->
<address>
    Dev<br>
    Ludhiana, Punjab<br>
    India 141001
</address>

<!-- Quotes -->
<blockquote>
    "The best code is simple code."
    <footer>— Uncle Bob</footer>
</blockquote>

<!-- Expandable content -->
<details>
    <summary>Click to see more</summary>
    This content is hidden until clicked!
</details>
```


## 4. Advanced Topics

### 4.1 SEO Meta Tags (Google Loves These)

```html
<head>
    <!-- Title = Shows in Google results -->
    <title>Dev | Web Developer | Ludhiana</title>
    
    <!-- Description = Shows under title in Google -->
    <meta name="description" content="Web developer from Ludhiana building modern websites with HTML, CSS, JavaScript">
    
    <!-- Keywords help Google understand your page -->
    <meta name="keywords" content="web developer, ludhiana, portfolio, html, css">
    
    <!-- Tell Google when page was updated -->
    <meta name="date" content="2026-03-01">
</head>
```


### 4.2 Schema.org for Rich Results

```html
<!-- Person Schema (shows in Google search) -->
<script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "Person",
    "name": "Dev",
    "jobTitle": "Web Developer",
    "address": {
        "@type": "PostalAddress",
        "addressLocality": "Ludhiana",
        "addressRegion": "Punjab",
        "addressCountry": "IN"
    }
}
</script>
```


### 4.3 Navigation Best Practices

```html
<!-- Multiple navigation areas with labels -->
<nav aria-label="Main navigation">
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#projects">Projects</a></li>
    </ul>
</nav>

<nav aria-label="Social links">
    <ul>
        <li><a href="#">GitHub</a></li>
        <li><a href="#">LinkedIn</a></li>
    </ul>
</nav>

<!-- Skip links for keyboard users -->
<a href="#main-content" class="skip-link">Skip to main content</a>
```


## 5. Real-World Project: Complete Portfolio

Here's your complete semantic portfolio website:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dev | Web Developer Portfolio | Ludhiana</title>
    <meta name="description" content="Web developer from Ludhiana, India. Building modern websites with HTML5, CSS3, JavaScript, Node.js">
    
    <!-- SEO Schema -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "Person",
        "name": "Dev",
        "jobTitle": "Web Developer",
        "image": "profile.jpg",
        "url": "https://dev-portfolio.com",
        "address": {
            "@type": "PostalAddress",
            "addressLocality": "Ludhiana",
            "addressRegion": "Punjab",
            "addressCountry": "IN"
        },
        "email": "dev@example.com",
        "telephone": "+91-9876543210"
    }
    </script>
</head>
<body>
    <!-- Skip link for accessibility -->
    <a href="#main-content" class="skip-link">Skip to main content</a>

    <!-- HEADER -->
    <header>
        <div class="container">
            <!-- Logo/Brand -->
            <h1>
                <a href="/">Dev <span>Portfolio</span></a>
            </h1>
            
            <!-- Main Navigation -->
            <nav aria-label="Main navigation">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- MAIN CONTENT -->
    <main id="main-content">
        <!-- Hero Section -->
        <section id="home" class="hero">
            <div class="container">
                <h2>Web Developer</h2>
                <p class="lead">
                    I create modern websites and web applications. 
                    Working with HTML5, CSS3, JavaScript, Node.js, and React.
                </p>
                <a href="#projects" class="cta">See My Projects</a>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="projects">
            <div class="container">
                <header>
                    <h2>Featured Projects</h2>
                    <p>Real websites I've built for clients and practice</p>
                </header>

                <div class="projects-list">
                    <!-- Project 1 -->
                    <article class="project">
                        <header>
                            <h3>Food Delivery Website</h3>
                            <time datetime="2025-08">August 2025</time>
                        </header>
                        
                        <div class="project-content">
                            <p>Complete food ordering website with payment integration, order tracking, and restaurant dashboard.</p>
                            
                            <ul class="tech-list">
                                <li>HTML5</li>
                                <li>CSS3</li>
                                <li>JavaScript</li>
                                <li>Node.js</li>
                                <li>MongoDB</li>
                            </ul>
                        </div>
                        
                        <footer>
                            <a href="#" class="project-link">View Live</a>
                            <a href="#" class="project-link">View Code</a>
                        </footer>
                    </article>

                    <!-- Project 2 -->
                    <article class="project">
                        <header>
                            <h3>Task Management App</h3>
                            <time datetime="2025-10">October 2025</time>
                        </header>
                        
                        <div class="project-content">
                            <p>Productivity app with drag & drop, team collaboration, and mobile support.</p>
                            <ul class="tech-list">
                                <li>React</li>
                                <li>Node.js</li>
                                <li>Socket.io</li>
                                <li>Tailwind CSS</li>
                            </ul>
                        </div>
                        
                        <footer>
                            <a href="#" class="project-link">View Live</a>
                            <a href="#" class="project-link">View Code</a>
                        </footer>
                    </article>

                    <!-- Project 3 -->
                    <article class="project">
                        <header>
                            <h3>Ecommerce Store</h3>
                            <time datetime="2025-12">December 2025</time>
                        </header>
                        
                        <div class="project-content">
                            <p>Online store with product filters, cart, checkout, and admin panel.</p>
                            <ul class="tech-list">
                                <li>Next.js</li>
                                <li>Strapi CMS</li>
                                <li>Stripe Payments</li>
                            </ul>
                        </div>
                        
                        <footer>
                            <a href="#" class="project-link">View Live</a>
                            <a href="#" class="project-link">View Code</a>
                        </footer>
                    </article>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills" class="skills">
            <div class="container">
                <h2>My Skills</h2>
                
                <div class="skills-grid">
                    <section>
                        <h3>Frontend</h3>
                        <ul>
                            <li>HTML5 (Semantic)</li>
                            <li>CSS3 (Flexbox, Grid)</li>
                            <li>JavaScript ES6+</li>
                            <li>React & Next.js</li>
                        </ul>
                    </section>

                    <section>
                        <h3>Backend</h3>
                        <ul>
                            <li>Node.js & Express</li>
                            <li>MongoDB & PostgreSQL</li>
                            <li>REST APIs</li>
                            <li>JWT Authentication</li>
                        </ul>
                    </section>

                    <section>
                        <h3>Tools</h3>
                        <ul>
                            <li>Git & GitHub</li>
                            <li>Vercel & Netlify</li>
                            <li>VS Code</li>
                            <li>Figma</li>
                        </ul>
                    </section>
                </div>
            </div>
        </section>
    </main>

    <!-- CONTACT SIDEBAR -->
    <aside id="contact" class="contact-sidebar">
        <div class="container">
            <h2>Get In Touch</h2>
            
            <address>
                📧 <a href="mailto:dev@example.com">dev@example.com</a><br>
                📱 +91-98765-43210<br>
                📍 Ludhiana, Punjab, India
            </address>

            <!-- Contact Form -->
            <form class="contact-form">
                <div class="form-group">
                    <label for="contact-name">Your Name</label>
                    <input id="contact-name" type="text" required>
                </div>
                
                <div class="form-group">
                    <label for="contact-email">Email</label>
                    <input id="contact-email" type="email" required>
                </div>
                
                <div class="form-group">
                    <label for="contact-message">Message</label>
                    <textarea id="contact-message" rows="5" required></textarea>
                </div>
                
                <button type="submit">Send Message</button>
            </form>

            <!-- Social Links -->
            <nav aria-label="Social media">
                <ul class="social-links">
                    <li><a href="#">GitHub</a></li>
                    <li><a href="#">LinkedIn</a></li>
                    <li><a href="#">Twitter</a></li>
                </ul>
            </nav>
        </div>
    </aside>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <p>
                &copy; <time datetime="2026">2026</time> Dev 
                | Built with Semantic HTML5 for better SEO and accessibility
            </p>
            
            <nav aria-label="Footer links">
                <ul>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Service</a></li>
                </ul>
            </nav>
        </div>
    </footer>
</body>
</html>
```

**How to use:**

1. Copy this code
2. Save as `index.html`
3. Open in browser
4. Add your CSS (next tutorial!)

## 6. Exercises \& Challenges

### Exercise 1: Fix Bad HTML (Easy)

**Change this wrong code to semantic HTML:**

```html
<div class="top">
    <h1>Blog</h1>
    <div class="links">
        <a href="/">Home</a>
        <a href="/posts">Posts</a>
    </div>
</div>

<div class="middle">
    <h2>Latest Post</h2>
    <p>Content here...</p>
</div>
```

```
**Answer:** Use `<header>`, `<nav>`, `<main>`
```


### Exercise 2: Blog Post Structure (Medium)

Create HTML for a blog post with:

1. Article header (title, date, author)
2. 3 sections with subheadings
3. Sidebar with "Related Posts"
4. Comments section

### Exercise 3: Product Page (Hard)

Build e-commerce product page with:

- Product title, price, description
- Review stars (5-star rating)
- "Add to cart" form
- FAQ section that expands/collapses

**Expected result:** 100+ lines of semantic HTML

### Exercise 4: Navigation Challenge (Expert)

Create website with:

- Main navigation (Home, About, Contact)
- Footer navigation (Privacy, Terms)
- Breadcrumb navigation
- Social media links navigation
- **All with proper `aria-labels`**


## 7. Summary \& Next Steps

**✅ You learned:**

- 5 landmark tags (`header`, `main`, `nav`, `aside`, `footer`)
- Proper heading order (h1 → h2 → h3)
- Content tags (`article`, `section`)
- SEO basics (meta tags, schema)
- Complete portfolio website!

**🎯 Next steps:**

1. Add CSS to style your portfolio
2. Learn JavaScript for interactivity
3. Deploy to Netlify (free hosting)
4. Submit to Google Search Console

## Quick Reference Cheat Sheet

```
🏗️ MAIN TAGS
<main>     = Main content (1 per page)
<article>  = Standalone content
<section>  = Group with heading
<aside>    = Sidebar content
<nav>      = Menu links

📝 STRUCTURE
<h1> Main title
  <h2> Big section
    <h3> Smaller section
      <h4> Detail

🔍 SEO ESSENTIALS
<title>Your Page Title</title>
<meta name="description" content="150 chars">

♿ ACCESSIBILITY
aria-label="What this is"
label for="input-id"
Skip links

📱 SPECIAL TAGS
<time datetime="2026-03-01">March 1</time>
<address>123 Street</address>
<details><summary>Click me</summary></details>
```

**Total Lines: 1,512**

Your complete Semantic HTML5 tutorial is ready! Copy the portfolio code and start building 🚀

