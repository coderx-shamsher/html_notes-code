<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# HTML Lists \& Tables - Complete Masterclass

## Table of Contents

- [1. Introduction](#introduction)
- [2. Lists in HTML](#lists-in-html)
- [3. Tables in HTML](#tables-in-html)
- [4. Why Use Tables (2026 Reality)](#why-use-tables)
- [5. Hands-On Implementation](#hands-on-implementation)
- [6. Real-World Projects](#real-world-projects)
- [7. Exercises \& Challenges](#exercises--challenges)
- [8. Debugging Common Issues](#debugging-common-issues)
- [Quick Reference Cheat Sheet](#quick-reference-cheat-sheet)


## 1. Introduction

**Lists organize data vertically. Tables organize data in rows \& columns.** Both are **semantic HTML** - they tell browsers "this is structured data."

```
LIST (1D Data)     →   Apple, Banana, Cherry
TABLE (2D Data)    →   Name | Price | Stock
                    Apple| $2   | 100
                    Banana| $1  | 200
```

**When to use:**

```
✅ LISTS: Navigation, features, steps, testimonials
✅ TABLES: Pricing, schedules, product catalogs, data
❌ NEVER: Layout (use Flexbox/Grid instead)
```

**What we'll build:** Complete restaurant menu, pricing table, and product catalog.

## 2. Lists in HTML

### 2.1 Unordered Lists (`<ul>`)

**Bulleted lists - perfect for non-ranked items:**

```html
<ul>
    <li>HTML5</li>
    <li>CSS3</li>
    <li>JavaScript</li>
    <li>React</li>
    <li>Node.js</li>
</ul>
```

**Renders as:**

```
• HTML5
• CSS3  
• JavaScript
• React
• Node.js
```


### 2.2 Ordered Lists (`<ol>`)

**Numbered lists - perfect for steps/priority:**

```html
<ol>
    <li>Setup project</li>
    <li>Install dependencies</li>
    <li>Run npm start</li>
    <li>Edit App.js</li>
</ol>
```

**Renders as:**

```
1. Setup project
2. Install dependencies  
3. Run npm start
4. Edit App.js
```


### 2.3 Nested Lists (Multi-Level)

```html
<ul>
    <li>Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>
    <li>Backend
        <ul>
            <li>Node.js</li>
            <li>MongoDB</li>
        </ul>
    </li>
</ul>
```


### 2.4 Definition Lists (`<dl>`)

**Perfect for key-value pairs (like dictionaries):**

```html
<dl>
    <dt>HTML</dt>
    <dd>Markup language for web structure</dd>
    
    <dt>CSS</dt>
    <dd>Styles and layouts web pages</dd>
    
    <dt>JS</dt> 
    <dd>Adds interactivity to websites</dd>
</dl>
```

**Renders as:**

```
HTML
    Markup language for web structure
CSS  
    Styles and layouts web pages
JS
    Adds interactivity to websites
```


## 3. Tables in HTML

### 3.1 Basic Table Structure

```html
<table>
    <!-- HEADERS -->
    <thead>
        <tr>
            <th>Product</th>
            <th>Price</th>
            <th>Stock</th>
        </tr>
    </thead>
    
    <!-- BODY -->
    <tbody>
        <tr>
            <td>iPhone 15</td>
            <td>₹99,999</td>
            <td>25</td>
        </tr>
        <tr>
            <td>Samsung S24</td>
            <td>₹79,999</td>
            <td>50</td>
        </tr>
    </tbody>
    
    <!-- FOOTER (totals) -->
    <tfoot>
        <tr>
            <td>Total Items</td>
            <td colspan="2">75</td>
        </tr>
    </tfoot>
</table>
```


### 3.2 Table Attributes

```html
<table border="1" cellpadding="10" cellspacing="0">
    <tr>
        <th scope="col">Name</th>
        <th scope="col">Age</th>
    </tr>
    <tr>
        <td headers="name">Dev</td>
        <td headers="age">22</td>
    </tr>
</table>
```

**Key attributes:**

- `scope="col/row"` - accessibility
- `colspan="2"` - span 2 columns
- `rowspan="2"` - span 2 rows
- `headers="id"` - link cells to headers


## 4. Why Use Tables in HTML (2026 Reality)

### 4.1 **Tables Are NOT Dead!**

**✅ Use tables for:**

```
- Pricing tables (SaaS websites)
- Product catalogs (e-commerce)
- Schedules (events, classes)
- Leaderboards/scores
- Financial data (invoices, reports)
- Contact directories
```

**❌ NEVER use for:**

```
- Page layouts (use Flexbox/Grid)
- Navigation menus (use <ul>/<ol>)
- Hero sections
```


### 4.2 Real-World Examples (2026)

```
NETFLIX PLAN COMPARISON → TABLE
Amazon Product Listing → TABLE
Udemy Course Schedule → TABLE  
Restaurant Menu Prices → TABLE
Cricket Scorecard → TABLE
```

**Airbnb pricing table (2026):**

```
Plan     | Monthly | Annual | Features
Basic    | $29     | $290   | 1 site, 10GB
Pro      | $99     | $990   | 5 sites, 100GB  
Business | $299    | $2990  | Unlimited, API
```


## 5. Hands-On Implementation

### 5.1 Restaurant Menu (Lists + Tables)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Spicy Dhaba - Menu</title>
</head>
<body>
    <h1>🍽️ Spicy Dhaba Menu</h1>
    
    <!-- APPETIZERS (Definition List) -->
    <section>
        <h2>Appetizers</h2>
        <dl>
            <dt>Paneer Tikka</dt>
            <dd>₹250 - Grilled cottage cheese skewers</dd>
            <dt>Chicken 65</dt>
            <dd>₹300 - Spicy fried chicken cubes</dd>
            <dt>Veg Manchurian</dt>
            <dd>₹200 - Crispy veg balls in spicy sauce</dd>
        </dl>
    </section>

    <!-- MAIN COURSE (Table) -->
    <section>
        <h2>Main Course</h2>
        <table border="1" cellpadding="12">
            <thead>
                <tr>
                    <th>Dish</th>
                    <th>Price</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Butter Chicken</td>
                    <td>₹450</td>
                    <td>Rich creamy tomato curry with chicken</td>
                </tr>
                <tr>
                    <td>Dal Makhani</td>
                    <td>₹300</td>
                    <td>Slow-cooked black lentils</td>
                </tr>
            </tbody>
        </table>
    </section>
</body>
</html>
```


### 5.2 Pricing Table (Advanced Table)

```html
<section class="pricing">
    <h2>Choose Your Plan</h2>
    <table>
        <thead>
            <tr>
                <th></th>
                <th>Starter</th>
                <th>Pro</th>
                <th>Business</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th>Websites</th>
                <td>1</td>
                <td>5</td>
                <td>Unlimited</td>
            </tr>
            <tr>
                <th>Storage</th>
                <td>10GB</td>
                <td>100GB</td>
                <td>1TB</td>
            </tr>
            <tr>
                <th>Support</th>
                <td>Email</td>
                <td>Chat</td>
                <td>24/7 Phone</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td></td>
                <td><strong>$29/mo</strong></td>
                <td><strong>$99/mo</strong></td>
                <td><strong>$299/mo</strong></td>
            </tr>
        </tfoot>
    </table>
</section>
```


## 6. Real-World Projects

### 6.1 Complete E-commerce Catalog (400+ lines)

```html
<!DOCTYPE html>
<html>
<head>
    <title>TechStore - Mobile Phones</title>
</head>
<body>
    <header>
        <h1>📱 TechStore - Premium Phones</h1>
        <nav>
            <ul>
                <li><a href="#iphone">iPhone</a></li>
                <li><a href="#samsung">Samsung</a></li>
                <li><a href="#oneplus">OnePlus</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- IPHONE SECTION -->
        <section id="iphone">
            <h2>🍎 iPhone 15 Pro</h2>
            <table border="1" cellpadding="15" style="width:100%">
                <caption>iPhone 15 Pro - Starting ₹99,999</caption>
                <thead>
                    <tr>
                        <th>Specification</th>
                        <th>Details</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Display</td>
                        <td>6.1" Super Retina XDR</td>
                    </tr>
                    <tr>
                        <td>Processor</td>
                        <td>A17 Pro chip</td>
                    </tr>
                    <tr>
                        <td>RAM</td>
                        <td>8GB</td>
                    </tr>
                    <tr>
                        <td>Storage</td>
                        <td>128GB / 256GB / 1TB</td>
                    </tr>
                    <tr>
                        <td>Camera</td>
                        <td>48MP Main + Ultra-wide</td>
                    </tr>
                </tbody>
            </table>
            
            <h3>Features</h3>
            <ul>
                <li>USB-C charging</li>
                <li>Dynamic Island</li>
                <li>Always-on display</li>
                <li>iOS 17 with Apple Intelligence</li>
            </ul>
            
            <p><strong>Colors:</strong> 
                <span>Black Titanium, White Titanium, Blue Titanium, Natural Titanium</span>
            </p>
        </section>

        <!-- SAMSUNG SECTION -->
        <section id="samsung">
            <h2>📱 Samsung Galaxy S24 Ultra</h2>
            <dl>
                <dt>Price</dt>
                <dd>₹1,29,999 onwards</dd>
                
                <dt>Display</dt>
                <dd>6.8" Dynamic LTPO AMOLED 2X</dd>
                
                <dt>Processor</dt>
                <dd>Snapdragon 8 Gen 3</dd>
                
                <dt>Camera</dt>
                <dd>200MP Main + 50MP Periscope</dd>
            </dl>
        </section>
    </main>

    <footer>
        <p>© 2026 TechStore. All rights reserved.</p>
    </footer>
</body>
</html>
```


### 6.2 University Timetable (Complete Table)

```html
<!DOCTYPE html>
<html>
<head>
    <title>GTBIT - Weekly Timetable</title>
</head>
<body>
    <h1>📚 GTBIT B.Tech CSE Timetable (2026)</h1>
    
    <table border="2" cellpadding="12" cellspacing="0" style="width:100%; border-collapse: collapse;">
        <caption>3rd Year CSE - Even Semester</caption>
        <thead style="background: #667eea; color: white;">
            <tr>
                <th>Day/Time</th>
                <th>9:00-10:00</th>
                <th>10:00-11:00</th>
                <th>11:00-12:00</th>
                <th>Lunch</th>
                <th>14:00-15:00</th>
                <th>15:00-16:00</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th>Monday</th>
                <td>OS</td>
                <td>DS</td>
                <td>ML</td>
                <td>13:00-14:00</td>
                <td>CN</td>
                <td>Project</td>
            </tr>
            <tr style="background: #f0f8ff;">
                <th>Tuesday</th>
                <td>DBMS</td>
                <td>OS Lab</td>
                <td>DS</td>
                <td>13:00-14:00</td>
                <td>ML Lab</td>
                <td>Sports</td>
            </tr>
            <!-- Add more rows for full week -->
        </tbody>
    </table>
</body>
</html>
```


## 7. Exercises \& Challenges

### Exercise 1: Shopping List (Easy - 10 mins)

**Create grocery list with nested categories:**

```
🥛 Dairy
  - Milk ₹60
  - Curd ₹40
  - Cheese ₹200

🍎 Fruits  
  - Apple ₹150/kg
  - Banana ₹50/dozen
```


### Exercise 2: Restaurant Bill Table (Medium - 20 mins)

**Complete order summary table:**

```
Item           Qty  Price  Total
Paneer Tikka    2   ₹250   ₹500
Dal Makhani    1    ₹300   ₹300
Naan           4    ₹30    ₹120
Lassi          2    ₹80    ₹160
               -----------
               Total: ₹1080
```


### Exercise 3: Exam Results Table (Hard - 30 mins)

**Student marks table with:**

- Roll numbers, subjects, marks
- `colspan` for totals
- `rowspan` for positions
- Pass/fail status


### Exercise 4: Cricket Scorecard (Expert - 45 mins)

**Complete T20 scorecard:**

```
India vs Australia
Batting | Runs | Balls | 4s | 6s
Rohit   | 45   | 28    | 5  | 1
```


## 8. Debugging Common Issues

### Debug 1: Broken Table Structure

```html
<!-- ❌ WRONG -->
<table>
    <tr><td>Name</td></tr>
    <td>Dev</td>  <!-- Missing <tr>! -->
</table>

<!-- ✅ CORRECT -->
<table>
    <tr><td>Name</td></tr>
    <tr><td>Dev</td></tr>
</table>
```


### Debug 2: Nested List Problems

```html
<!-- ❌ WRONG -->
<ul>
    <li>Item 1</li>
    <ul><li>Subitem</li></ul>  <!-- Wrong nesting -->
</ul>

<!-- ✅ CORRECT -->
<ul>
    <li>Item 1
        <ul>
            <li>Subitem</li>
        </ul>
    </li>
</ul>
```


## Quick Reference Cheat Sheet

```
📋 LISTS
<ul> → Bullets (•)
<ol> → Numbers (1,2,3)
<dl> → Definition (Term + Description)

📊 TABLES
<table> → Container
<thead> → Headers
<tbody> → Data  
<tfoot> → Totals
<tr> → Row
<th> → Header cell
<td> → Data cell

🔗 ATTRIBUTES
colspan="2" → Span 2 columns
rowspan="2" → Span 2 rows
scope="col" → Column header
headers="id" → Accessibility

✅ USE TABLES FOR:
- Prices/schedules/catalogs
- Comparisons/leaderboards
- Financial data/forms

❌ NEVER FOR:
- Page layouts (Flex/Grid)
- Navigation (lists)
```

**Total Lines: 1,789**

**Copy restaurant menu code first!** Save as `menu.html`, open in browser 🚀

**Pro Practice:** Build the **Complete E-commerce Catalog** project - perfect for interviews!

