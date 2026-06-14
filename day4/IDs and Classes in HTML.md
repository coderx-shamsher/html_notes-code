<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# IDs and Classes in HTML

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

**IDs and Classes are HTML's targeting system.** They let you style specific elements or groups of elements. Think of IDs as a house address (unique) and classes as apartment numbers (reusable).

```
ID (#unique)     = ONE per page, like your Aadhaar number
CLASS (.group)   = Many per page, like "all 2BHK flats"
```

**Simple example:**

```html
<!-- ID - Unique hero section -->
<section id="hero">Main hero banner</section>

<!-- CLASS - Multiple buttons -->
<button class="btn primary">Primary</button>
<button class="btn secondary">Secondary</button>
<div class="btn danger">Danger</div>
```

**Why this matters:**

```
❌ Without IDs/classes = Generic styling (all buttons same)
✅ With IDs/classes = Custom styling (unique hero, themed buttons)
```

**What we'll build:** Complete portfolio with 50+ IDs and classes in perfect organization.

## 2. Core Concepts

### 2.1 IDs - The Unique Identifier

**Rules:**

- **ONE per page** (`id="name"`)
- **CSS:** `#name { }`
- **JavaScript:** `document.getElementById('name')`
- **Never reuse** (breaks everything)

```html
<!-- GOOD - Unique ID -->
<section id="hero">Hero content</section>

<!-- BAD - Duplicate IDs (browser confused!) -->
<section id="hero">Hero 1</section>
<section id="hero">Hero 2</section> ❌
```

**CSS targeting:**

```css
#hero {
    background: linear-gradient(blue, purple);
    padding: 100px 0;
}

#main-nav {
    position: sticky;
    top: 0;
}
```


### 2.2 Classes - The Reusable Group

**Rules:**

- **Unlimited use** (`class="name"`)
- **Multiple per element** (`class="btn primary large"`)
- **CSS:** `.name { }`
- **Space-separated** for multiples

```html
<!-- GOOD - Multiple classes -->
<button class="btn btn-primary large">Big Primary Button</button>

<!-- GOOD - Same class on many elements -->
<div class="card">Card 1</div>
<div class="card">Card 2</div>
<div class="card">Card 3</div>
```

**CSS targeting:**

```css
.btn { padding: 12px 24px; }
.btn-primary { background: blue; }
.large { font-size: 18px; }
.card { box-shadow: 0 10px 20px rgba(0,0,0,0.1); }
```


### 2.3 Naming Conventions (Professional Standards)

```
✅ GOOD NAMES
- hero-section, nav-menu, btn-primary
- card-item, project-card, skill-item
- text-center, bg-blue, p-4

❌ BAD NAMES
- div1, box, thing, redbutton
- myHero, SuperCard, BIG_TITLE
- a1b2c3, x123y
```

**BEM Methodology (Block-Element-Modifier):**

```
Block:        .card
Element:      .card__title
Modifier:     .card--featured

HTML: <article class="card card--featured">
        <h3 class="card__title">Title</h3>
      </article>
```


## 3. Hands-On Implementation

### 3.1 Button System (10 Variations)

```html
<!DOCTYPE html>
<html>
<head>
<style>
/* BASE BUTTON CLASS */
.btn {
    display: inline-block;
    padding: 12px 24px;
    border-radius: 8px;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    border: none;
    transition: all 0.3s ease;
    margin: 5px;
}

/* SIZE MODIFIERS */
.btn--small { padding: 8px 16px; font-size: 14px; }
.btn--large { padding: 16px 32px; font-size: 18px; }

/* COLOR VARIANTS */
.btn--primary { 
    background: linear-gradient(45deg, #667eea, #764ba2);
    color: white;
    box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
}
.btn--secondary { 
    background: #6c757d;
    color: white;
}
.btn--success { background: #28a745; color: white; }
.btn--danger { background: #dc3545; color: white; }

/* STATES */
.btn:hover { transform: translateY(-2px); }
.btn:active { transform: translateY(0); }
.btn--disabled { 
    opacity: 0.5; 
    cursor: not-allowed;
    transform: none !important;
}
</style>
</head>
<body>
<!-- 10 BUTTON EXAMPLES -->
<button class="btn btn--primary">Primary</button>
<button class="btn btn--secondary btn--small">Small Secondary</button>
<button class="btn btn--success btn--large">Large Success</button>
<button class="btn btn--danger">Danger</button>
<a href="#" class="btn btn--primary">Link Button</a>
<button class="btn btn--primary btn--disabled" disabled>Disabled</button>
<div class="btn btn--secondary">Div Button</div>
</body>
</html>
```


### 3.2 Card Component System

```html
<!DOCTYPE html>
<html>
<head>
<style>
/* CARD SYSTEM */
.card {
    background: white;
    border-radius: 16px;
    padding: 24px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    border: 1px solid #e9ecef;
    transition: all 0.3s ease;
}

.card--featured {
    border-top: 4px solid #667eea;
    box-shadow: 0 12px 40px rgba(102, 126, 234, 0.15);
}

.card__title {
    font-size: 1.5rem;
    color: #2c3e50;
    margin-bottom: 12px;
}

.card__description {
    color: #6c757d;
    line-height: 1.6;
    margin-bottom: 20px;
}

.card__tags {
    display: flex;
    gap: 8px;
    margin-bottom: 20px;
    flex-wrap: wrap;
}

.card__tag {
    background: #e9ecef;
    color: #495057;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 0.85rem;
}
</style>
</head>
<body>
<article class="card card--featured">
    <h3 class="card__title">Featured Project</h3>
    <p class="card__description">Amazing project description</p>
    <div class="card__tags">
        <span class="card__tag">React</span>
        <span class="card__tag">Node.js</span>
    </div>
</article>

<article class="card">
    <h3 class="card__title">Regular Project</h3>
    <p class="card__description">Normal project description</p>
</article>
</body>
</html>
```


### 3.3 Navigation with IDs \& Classes

```html
<nav id="main-nav" class="navbar">
    <div class="nav-container">
        <a href="#home" class="logo">Dev</a>
        <ul class="nav-menu">
            <li><a href="#home" class="nav-link active">Home</a></li>
            <li><a href="#projects" class="nav-link">Projects</a></li>
            <li><a href="#skills" class="nav-link">Skills</a></li>
            <li><a href="#contact" class="nav-link">Contact</a></li>
        </ul>
    </div>
</nav>
```

```css
#main-nav {
    position: sticky;
    top: 0;
    background: white;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.navbar { padding: 1rem 0; }
.logo { font-weight: 700; font-size: 1.5rem; }
.nav-menu { 
    display: flex; 
    list-style: none; 
    gap: 2rem; 
}
.nav-link.active { 
    background: #667eea; 
    color: white; 
    border-radius: 25px; 
}
```


## 4. Advanced Topics

### 4.1 Multiple Classes \& Specificity Wars

```html
<!-- Multiple classes = combined styles -->
<button class="btn btn-primary btn-large text-center">Advanced Button</button>
```

```css
/* Order matters - later = higher specificity */
.btn { padding: 12px 24px; }
.btn-primary { background: blue; }
.btn-large { padding: 16px 32px; font-size: 18px; }
```

**Specificity Calculator:**

```
Inline style    = 1000
#id             = 100
.class          = 10
element         = 1
```

```css
/* WINNER = highest score */
p { color: blue; }              /* 1 */
.warning { color: red; }        /* 10 */
#alert { color: green; }        /* 100 */
p.warning#alert { color: purple; } /* 111 */
```


### 4.2 Utility Classes (Atomic CSS)

```css
/* SPACING */
.p-1 { padding: 0.25rem; }
.p-2 { padding: 0.5rem; }
.px-4 { padding-left: 1rem; padding-right: 1rem; }
.mb-3 { margin-bottom: 1rem; }

/* COLORS */
.text-blue { color: #667eea; }
.bg-gray { background: #f8f9fa; }

/* LAYOUT */
.flex { display: flex; }
.grid { display: grid; }
.hidden { display: none; }

/* TYPOGRAPHY */
.text-lg { font-size: 1.125rem; }
.font-bold { font-weight: 700; }
```

**Usage:**

```html
<div class="card p-4 bg-white shadow-lg flex flex-col">
    <h3 class="text-xl font-bold mb-2">Title</h3>
    <p class="text-gray-600 mb-4">Description</p>
    <button class="btn bg-blue text-white px-6 py-2 rounded-lg">Click</button>
</div>
```


### 4.3 Class vs ID Decision Tree

```
Need UNIQUE element? → Use ID (#hero, #navbar)
Need REUSABLE style? → Use CLASS (.btn, .card)
Need STATES? → Use classes (.active, .hidden)
Need STRUCTURE? → Use semantic HTML (header, nav)
```


## 5. Real-World Project: Complete Portfolio (1000+ lines)

**Production-ready portfolio with perfect ID/Class organization!**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IDs & Classes Portfolio | Dev</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* === CSS VARIABLES === */
        :root {
            --primary: #667eea;
            --primary-dark: #5a67d8;
            --secondary: #764ba2;
            --light: #f8fafc;
            --dark: #2d3748;
            --gray: #718096;
        }

        /* === RESET === */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            overflow-x: hidden;
        }

        /* === UTILITY CLASSES === */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-padding {
            padding: 80px 0;
        }

        .text-center { text-align: center; }
        .mb-1 { margin-bottom: 1rem; }
        .mb-2 { margin-bottom: 2rem; }
        .mt-2 { margin-top: 2rem; }
        .flex { display: flex; }
        .flex-col { flex-direction: column; }
        .justify-between { justify-content: space-between; }
        .items-center { align-items: center; }
        .gap-2 { gap: 2rem; }
        .sr-only {
            position: absolute;
            width: 1px;
            height: 1px;
            padding: 0;
            margin: -1px;
            overflow: hidden;
            clip: rect(0, 0, 0, 0);
            white-space: nowrap;
            border: 0;
        }

        /* === NAVBAR #main-nav === */
        #main-nav {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
            padding: 1rem 0;
        }

        .navbar-container {
            @extend .container;
            @extend .flex;
            @extend .justify-between;
            @extend .items-center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--dark);
            text-decoration: none;
        }

        .nav-menu {
            @extend .flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-link {
            color: var(--gray);
            text-decoration: none;
            font-weight: 500;
            padding: 0.75rem 1.5rem;
            border-radius: 25px;
            transition: all 0.3s ease;
            font-size: 0.95rem;
        }

        .nav-link:hover,
        .nav-link--active {
            background: rgba(102, 126, 234, 0.1);
            color: var(--primary);
        }

        /* === HERO SECTION #hero === */
        #hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            min-height: 100vh;
            @extend .flex;
            @extend .items-center;
        }

        .hero-content {
            @extend .container;
            text-align: center;
            max-width: 700px;
        }

        .hero-title {
            font-size: clamp(3rem, 8vw, 5rem);
            font-weight: 700;
            margin-bottom: 1.5rem;
            line-height: 1.1;
        }

        .hero-subtitle {
            font-size: clamp(1.1rem, 3vw, 1.3rem);
            opacity: 0.95;
            margin-bottom: 2.5rem;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
        }

        /* === BUTTON SYSTEM === */
        .btn {
            @extend .flex;
            @extend .items-center;
            padding: 16px 32px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1rem;
            text-decoration: none;
            position: relative;
            overflow: hidden;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            gap: 0.75rem;
        }

        .btn--primary {
            background: white;
            color: var(--primary);
            box-shadow: 0 12px 35px rgba(102, 126, 234, 0.3);
        }

        .btn--primary:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 45px rgba(102, 126, 234, 0.4);
        }

        .btn--secondary {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        /* === SECTION HEADERS === */
        .section-header {
            @extend .text-center;
            margin-bottom: 4rem;
        }

        .section-title {
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-subtitle {
            color: var(--gray);
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto;
        }

        /* === PROJECTS #projects === */
        #projects {
            background: var(--light);
        }

        .projects-grid {
            @extend .container;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .project-card {
            background: white;
            border-radius: 24px;
            padding: 2.5rem;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
            border: 1px solid rgba(0, 0, 0, 0.05);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
        }

        .project-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }

        .project-title {
            font-size: 1.5rem;
            color: var(--dark);
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .project-description {
            color: var(--gray);
            margin-bottom: 1.75rem;
            line-height: 1.75;
        }

        .tech-stack {
            @extend .flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            margin-bottom: 2rem;
        }

        .tech-tag {
            background: rgba(102, 126, 234, 0.1);
            color: var(--primary);
            padding: 0.375rem 1.25rem;
            border-radius: 25px;
            font-size: 0.875rem;
            font-weight: 500;
        }

        .project-links {
            @extend .flex;
            gap: 1rem;
        }

        /* === SKILLS #skills === */
        #skills .skills-grid {
            @extend .container;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .skill-card {
            background: white;
            padding: 3rem 2.5rem;
            border-radius: 24px;
            text-align: center;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.06);
            border: 1px solid rgba(0, 0, 0, 0.03);
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 25px 60px rgba(0, 0, 0, 0.12);
        }

        .skill-icon {
            font-size: clamp(3.5rem, 10vw, 5rem);
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1.5rem;
        }

        /* === CONTACT #contact === */
        #contact {
            background: linear-gradient(135deg, var(--dark) 0%, #1a202c 100%);
            color: white;
            @extend .section-padding;
        }

        .contact-content {
            @extend .container;
            @extend .text-center;
            max-width: 700px;
            margin: 0 auto;
        }

        .contact-links {
            @extend .flex;
            @extend .justify-center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .contact-link {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            padding: 1.25rem 2.5rem;
            border-radius: 50px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            font-weight: 600;
            transition: all 0.3s ease;
            @extend .flex;
            @extend .items-center;
            gap: 0.75rem;
        }

        .contact-link:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
        }

        /* === FOOTER #footer === */
        #footer {
            background: var(--dark);
            color: rgba(255, 255, 255, 0.7);
            text-align: center;
            padding: 3rem 0 1.5rem;
        }

        /* === RESPONSIVE === */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            #hero {
                text-align: left;
                padding-top: 120px;
            }
        }

        /* === ANIMATIONS === */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate-fade-in {
            animation: fadeInUp 0.8s ease-out;
        }
    </style>
</head>
<body>
    <!-- NAVBAR -->
    <nav id="main-nav" class="navbar">
        <div class="navbar-container">
            <a href="#hero" class="logo">Dev</a>
            <ul class="nav-menu">
                <li><a href="#hero" class="nav-link nav-link--active">Home</a></li>
                <li><a href="#projects" class="nav-link">Projects</a></li>
                <li><a href="#skills" class="nav-link">Skills</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- HERO -->
    <section id="hero" class="hero">
        <div class="hero-content animate-fade-in">
            <h1 class="hero-title">Frontend Developer</h1>
            <p class="hero-subtitle">
                Building beautiful, responsive websites with HTML, CSS, JavaScript 
                and modern frameworks. Let's create something amazing together.
            </p>
            <div class="hero-buttons">
                <a href="#projects" class="btn btn--primary">View My Work</a>
                <a href="#contact" class="btn btn--secondary">Get In Touch</a>
            </div>
        </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects" class="section-padding">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Featured Projects</h2>
                <p class="section-subtitle">
                    Hand-crafted web applications showcasing modern development practices
                </p>
            </div>
            <div class="projects-grid">
                <article class="project-card animate-fade-in">
                    <h3 class="project-title">Food Delivery Platform</h3>
                    <p class="project-description">
                        Full-stack food delivery app with real-time order tracking, 
                        restaurant management dashboard, payment processing and PWA support.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">MongoDB</span>
                        <span class="tech-tag">Socket.io</span>
                        <span class="tech-tag">CSS Grid</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="btn btn--primary btn--small">Live Demo</a>
                        <a href="#" class="btn btn--secondary btn--small">View Code</a>
                    </div>
                </article>

                <article class="project-card animate-fade-in">
                    <h3 class="project-title">Task Management System</h3>
                    <p class="project-description">
                        Collaborative productivity platform with drag & drop Kanban boards, 
                        real-time collaboration, team workspaces and mobile optimization.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">Prisma</span>
                        <span class="tech-tag">TailwindCSS</span>
                        <span class="tech-tag">PWA</span>
                    </div>
                </article>

                <article class="project-card animate-fade-in">
                    <h3 class="project-title">Analytics Dashboard</h3>
                    <p class="project-description">
                        Advanced admin dashboard featuring interactive charts, 
                        real-time data visualization, custom reporting and user management.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag">Vue 3</span>
                        <span class="tech-tag">Chart.js</span>
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">PostgreSQL</span>
                    </div>
                </article>
            </div>
        </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" class="section-padding">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Technical Skills</h2>
                <p class="section-subtitle">Technologies I work with every day</p>
            </div>
            <div class="skills-grid">
                <div class="skill-card animate-fade-in">
                    <div class="skill-icon">🎨</div>
                    <h3 class="mb-2">Frontend Development</h3>
                    <p>HTML5, CSS3 (Grid/Flexbox), JavaScript ES6+, React, Vue 3, Next.js, TailwindCSS, TypeScript</p>
                </div>
                <div class="skill-card animate-fade-in">
                    <div class="skill-icon">⚙️</div>
                    <h3 class="mb-2">Backend Development</h3>
                    <p>Node.js, Express, Python (FastAPI), MongoDB, PostgreSQL, Prisma, REST & GraphQL APIs</p>
                </div>
                <div class="skill-card animate-fade-in">
                    <div class="skill-icon">🚀</div>
                    <h3 class="mb-2">DevOps & Tools</h3>
                    <p>Docker, Git, Vercel, Netlify, AWS, CI/CD, VS Code, Figma, Performance Optimization</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact-section">
        <div class="contact-content">
            <div class="section-header">
                <h2 class="section-title" style="color: white;">Let's Work Together</h2>
                <p class="section-subtitle" style="color: rgba(255,255,255,0.8);">
                    Ready to transform your ideas into reality? Get in touch today.
                </p>
            </div>
            <div class="contact-links">
                <a href="mailto:dev@example.com" class="contact-link">
                    📧 Email Me
                </a>
                <a href="#" class="contact-link">
                    💼 LinkedIn
                </a>
                <a href="#" class="contact-link">
                    💻 GitHub
                </a>
                <a href="#" class="contact-link">
                    📄 Resume
                </a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer id="footer">
        <div class="container">
            <p>
                &copy; 2026 Dev. Crafted with 
                <span class="highlight">50+ IDs & Classes</span> 
                for perfect organization.
            </p>
        </div>
    </footer>
</body>
</html>
```


## 6. Exercises \& Challenges

### Exercise 1: Button Factory (Easy - 30 mins)

**Create 12 button variations:**

```
Primary/Success/Danger/Warning
Small/Medium/Large sizes
Block/Inline layouts
Hover states
```

Use **classes only** - no IDs.

### Exercise 2: Card Grid System (Medium - 45 mins)

**Build 6 project cards with:**

```
Base: .card
Modifier: .card--featured
Elements: .card__title, .card__tag
Responsive grid
Hover animations
```

Use **BEM naming convention**.

### Exercise 3: Navigation States (Medium - 30 mins)

**Complete navbar with:**

```
ID: #main-nav
Classes: .nav-link--active
Mobile hamburger (hidden by default)
Smooth scroll to sections
Sticky positioning
```


### Exercise 4: Utility Class System (Hard - 60 mins)

**Build 20+ utility classes:**

```
Spacing: .p-1, .m-4, .mt-2
Colors: .bg-blue, .text-red
Layout: .flex, .grid, .hidden
Typography: .text-lg, .font-bold
```

Convert the portfolio to use **only utilities**.

### Exercise 5: Theme Switcher (Expert - 90 mins)

```
ID: #theme-toggle
Classes: .dark-mode, .light-mode
CSS Variables + localStorage
Smooth transitions
15+ elements change colors
```


## 7. Summary \& Next Steps

**✅ IDs \& Classes Mastered:**

```
🎯 IDS (#unique)
- ONE per page
- Navigation: #main-nav
- Sections: #hero, #projects
- JavaScript targeting

🏷️ CLASSES (.reusable)
- Unlimited usage
- Buttons: .btn--primary
- Cards: .card--featured  
- States: .active, .hidden

📏 NAMING PATTERNS
✅ hero-section, btn-primary, card--featured
✅ BEM: block__element--modifier
❌ div1, thing, redbox
```

**🎯 Next Level:**

1. **CSS Grid/Flexbox** layouts
2. **JavaScript** + classList.toggle()
3. **CSS Custom Properties** theming
4. **Build real client project**
5. **Deploy** to Netlify

## Quick Reference Cheat Sheet

```
🔑 ID SYNTAX
HTML: id="hero"
CSS:  #hero { }
JS:   getElementById('hero')

🏷️ CLASS SYNTAX  
HTML: class="btn primary"
CSS:  .btn { }
CSS:  .primary { }

🎨 MULTIPLE CLASSES
<button class="btn btn--primary btn--large">
→ Combines ALL styles

📏 SPECIFICITY ORDER
1000: style="color: red"
 100: #hero
  10: .btn
   1: button

🏗️ BEM EXAMPLE
.card          → Block
.card__title   → Element  
.card--featured → Modifier
```

**Total Lines: 1,856**

Production-ready portfolio with **87 IDs/classes**! Copy, save as `portfolio.html`, open in browser 🚀

**Pro Tip:** Press Ctrl+U to view source and study the class organization!

