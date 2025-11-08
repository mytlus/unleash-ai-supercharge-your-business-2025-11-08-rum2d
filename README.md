# Twenty One AI Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your Twenty One AI landing page. Whether you're updating text, fixing links, or adding new pages, this documentation provides step-by-step instructions tailored to your specific HTML structure.

---

## Table of Contents

1. [Understanding Your Landing Page Structure](#understanding-your-landing-page-structure)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Common Customization Tasks](#common-customization-tasks)
7. [Troubleshooting Guide](#troubleshooting-guide)

---

## Understanding Your Landing Page Structure

Before making changes, let's understand how your landing page is organized:

### Page Sections (in order from top to bottom)

| Section | Purpose | HTML ID |
|---------|---------|---------|
| **Header & Navigation** | Logo, menu links, and CTA button | `<header>` |
| **Hero Section** | Main headline and call-to-action | No ID (first section) |
| **Features Section** | Three main features with icons | `id="features"` |
| **Benefits Section** | Three key benefits with metrics | `id="benefits"` |
| **CTA Section** | Call-to-action with background image | No ID |
| **Testimonials Section** | Four customer testimonials | `id="testimonials"` |
| **About Us Section** | Company information and stats | `id="about"` |
| **Footer** | Links, contact info, social media | `<footer>` |

### File Structure You Should Have

```
your-project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy page)
├── terms.html (terms of service page)
├── blog.html (blog page)
└── [other pages as needed]
```

---

## Updating Text Content

Updating text on your landing page is straightforward. Follow these section-by-section instructions:

### 1. Updating Header & Navigation Text

**Location:** Lines 79-100 (Header section)

#### Change the Company Logo Text

Find this code:
```html
<span class="text-2xl font-bold text-gray-900">Twenty One AI</span>
```

**To change the company name:**
1. Open `index.html` in your text editor
2. Find the line above
3. Replace `Twenty One AI` with your company name
4. Save the file

**Example:**
```html
<!-- BEFORE -->
<span class="text-2xl font-bold text-gray-900">Twenty One AI</span>

<!-- AFTER -->
<span class="text-2xl font-bold text-gray-900">Your Company Name</span>
```

#### Update Navigation Menu Links

Find this section (lines 85-91):
```html
<div class="hidden lg:flex items-center gap-8">
    <a href="#features" class="nav-link">Features</a>
    <a href="#benefits" class="nav-link">Benefits</a>
    <a href="#testimonials" class="nav-link">Testimonials</a>
    <a href="#about" class="nav-link">About Us</a>
    <a href="mailto:contact@example.com" class="nav-link">Contact</a>
</div>
```

**To add or change navigation menu items:**
1. Locate the section above
2. Add new menu items by copying an existing line:
   ```html
   <a href="#section-name" class="nav-link">Menu Item Name</a>
   ```
3. Replace `section-name` with the ID of your section
4. Replace `Menu Item Name` with your desired text

**Example - Adding a "Pricing" menu item:**
```html
<a href="#features" class="nav-link">Features</a>
<a href="#benefits" class="nav-link">Benefits</a>
<a href="#pricing" class="nav-link">Pricing</a>  <!-- NEW LINE -->
<a href="#testimonials" class="nav-link">Testimonials</a>
<a href="#about" class="nav-link">About Us</a>
<a href="mailto:contact@example.com" class="nav-link">Contact</a>
```

**Important:** You must also add the same menu item to the mobile menu (lines 102-109) to ensure it appears on smartphones and tablets.

### 2. Updating Hero Section Text

**Location:** Lines 113-145 (Hero section)

#### Change the Main Headline

Find this code:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Unleash AI: Supercharge Your Business
</h1>
```

**To update:**
1. Replace `Unleash AI: Supercharge Your Business` with your headline
2. Keep the HTML tags (`<h1>` and `</h1>`) exactly as they are

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Transform Your Workflow Today
</h1>
```

#### Change the Hero Subtitle/Description

Find this code:
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed max-w-2xl">
    Stop chasing leads, start attracting them. Twenty One AI automates your workflows, frees your team, and propels your business to unparalleled efficiency. Experience the future of business, today.
</p>
```

**To update:**
1. Replace the text between `<p>` and `</p>` tags
2. Keep all the class names exactly the same

**Example:**
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed max-w-2xl">
    Streamline your operations and boost productivity. Our intelligent automation platform helps teams work smarter, not harder.
</p>
```

#### Update Hero Button Text

Find these lines:
```html
<a href="https://www.example.com" class="btn-primary text-center">
    <i class="fas fa-play mr-2"></i>Start Your Journey
</a>
<a href="mailto:contact@example.com" class="btn-secondary text-center">
    <i class="fas fa-envelope mr-2"></i>Contact Us
</a>
```

**To change button text:**
1. Replace `Start Your Journey` and `Contact Us` with your desired text
2. Keep the icons (`<i>` tags) if you want them, or remove them if you prefer just text

**Example:**
```html
<a href="https://www.example.com" class="btn-primary text-center">
    <i class="fas fa-play mr-2"></i>Get Started Free
</a>
<a href="mailto:contact@example.com" class="btn-secondary text-center">
    <i class="fas fa-envelope mr-2"></i>Request Demo
</a>
```

### 3. Updating Features Section

**Location:** Lines 160-230 (Features section)

The features section contains three cards. Here's how to update each one:

#### Update Feature Title

Find this code (appears 3 times, once per feature):
```html
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">Custom AI Workflow Development</h3>
```

**To change:**
1. Replace `Custom AI Workflow Development` with your feature title
2. Keep all the class names the same

#### Update Feature Description

Find this code (appears 3 times):
```html
<p class="text-gray-600 leading-relaxed mb-4">
    Build bespoke AI workflows tailored to your unique business processes...
</p>
```

**To change:**
1. Replace the text between `<p>` and `</p>` tags
2. Keep the class names unchanged

#### Update Feature Bullet Points

Find this code (appears 3 times):
```html
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Drag-and-drop workflow builder</span>
    </li>
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Pre-built integration templates</span>
    </li>
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Real-time workflow monitoring</span>
    </li>
</ul>
```

**To update bullet points:**
1. Replace the text inside each `<span>` tag
2. To add more bullet points, copy an entire `<li>` block and paste it
3. To remove bullet points, delete the entire `<li>` block

**Example - Adding a fourth bullet point:**
```html
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Drag-and-drop workflow builder</span>
    </li>
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Pre-built integration templates</span>
    </li>
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Real-time workflow monitoring</span>
    </li>
    <li class="flex items-center gap-2">
        <i class="fas fa-check text-blue-600"></i>
        <span>Advanced reporting tools</span>
    </li>
</ul>
```

### 4. Updating Benefits Section

**Location:** Lines 245-330 (Benefits section)

Each benefit card has a title, description, and a highlighted stat box. Here's how to update them:

#### Update Benefit Title

Find this code (appears 3 times):
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3 text-center">Significant Cost Reduction</h3>
```

**To change:**
1. Replace `Significant Cost Reduction` with your benefit title
2. Keep all class names the same

#### Update Benefit Description

Find this code (appears 3 times):
```html
<p class="text-gray-600 text-center leading-relaxed mb-4">
    Slash operational expenses by up to 60%...
</p>
```

**To change:**
1. Replace the description text
2. Keep class names unchanged

#### Update the Stat Box

Find this code (appears 3 times):
```html
<div class="bg-green-50 rounded-xl p-4 border border-green-200">
    <p class="text-sm font-semibold text-green-700 text-center">
        <i class="fas fa-check-circle mr-2"></i>Average ROI: 340% in Year 1
    </p>
</div>
```

**To change:**
1. Replace `Average ROI: 340% in Year 1` with your stat
2. Keep the class names and icon the same

### 5. Updating Testimonials Section

**Location:** Lines 410-480 (Testimonials section)

Each testimonial card contains a 5-star rating, quote, and customer info.

#### Update Testimonial Quote

Find this code (appears 4 times):
```html
<p class="text-gray-700 leading-relaxed mb-6 text-lg">
    "Twenty One AI completely transformed how we handle customer inquiries..."
</p>
```

**To change:**
1. Replace the quoted text
2. Keep the quotation marks (" ") at the beginning and end
3. Keep all class names the same

#### Update Customer Name and Title

Find this code (appears 4 times):
```html
<div class="border-t border-gray-200 pt-4">
    <p class="font-bold text-gray-900">Sarah Mitchell</p>
    <p class="text-sm text-gray-600">Director of Customer Success, TechVenture Inc.</p>
</div>
```

**To change:**
1. Replace `Sarah Mitchell` with the customer's name
2. Replace `Director of Customer Success, TechVenture Inc.` with their title and company

### 6. Updating About Us Section

**Location:** Lines 485-545 (About Us section)

#### Update Section Heading

Find this code:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-8 leading-tight">
    About Twenty One AI
</h2>
```

**To change:**
1. Replace `About Twenty One AI` with your heading
2. Keep all class names the same

#### Update About Description

Find this code (appears 2 times):
```html
<p class="text-lg text-gray-700 leading-relaxed">
    Founded in 2020 by a team of AI researchers...
</p>
```

**To change:**
1. Replace the text between `<p>` and `</p>` tags
2. Keep class names unchanged

#### Update Statistics

Find this code:
```html
<div class="grid grid-cols-2 gap-6">
    <div class="bg-gradient-to-br from-blue-50 to-blue-100 rounded-2xl p-6 text-center border border-blue-200">
        <div class="text-4xl font-bold text-blue-600 mb-2">2K+</div>
        <p class="text-gray-700 font-semibold">Happy Customers</p>
    </div>
    <!-- More stat boxes... -->
</div>
```

**To change stats:**
1. Replace `2K+` with your number
2. Replace `Happy Customers` with your label
3. Repeat for each stat box

### 7. Updating Footer

**Location:** Lines 590-650 (Footer section)

#### Update Company Description

Find this code:
```html
<p class="text-gray-400 leading-relaxed">
    Transforming businesses with intelligent AI automation and predictive analytics.
</p>
```

**To change:**
1. Replace the description text
2. Keep class names the same

#### Update Footer Menu Links

Find these sections:
```html
<!-- Product -->
<div>
    <h4 class="text-white font-bold mb-6">Product</h4>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
        <!-- More links... -->
    </ul>
</div>
```

**To update footer menu items:**
1. Find the section you want to modify
2. Update the link text between `<a>` and `</a>` tags
3. Update the `href` attribute if the link destination changes

#### Update Contact Email

Find this code:
```html
<p class="text-gray-400 mb-4">
    <i class="fas fa-envelope mr-2"></i>
    <a href="mailto:contact@example.com" class="hover:text-blue-400 transition-colors duration-300">contact@example.com</a>
</p>
```

**To change:**
1. Replace both instances of `contact@example.com` with your actual email address
2. Keep the `mailto:` prefix before the email address

**Example:**
```html
<a href="mailto:hello@yourcompany.com" class="hover:text-blue-400 transition-colors duration-300">hello@yourcompany.com</a>
```

#### Update Copyright Year

Find this code:
```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">
    &copy; 2025 Twenty One AI. All rights reserved. Powered by Claude (Anthropic).
</p>
```

**To change:**
1. Replace `2025` with the current year
2. Replace `Twenty One AI` with your company name

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first CSS framework that uses class names to style elements. Understanding how to modify these classes is essential for customizing your page's appearance.

### What Are Tailwind Classes?

Tailwind classes control:
- **Colors** (text, backgrounds, borders)
- **Sizes** (padding, margins, width, height)
- **Spacing** (gaps between elements)
- **Responsive design** (how things look on different screen sizes)
- **Effects** (shadows, hover states, transitions)

### Common Tailwind Classes Used in Your Landing Page

#### Text Styling Classes

| Class | What It Does |
|-------|--------------|
| `text-gray-900` | Dark gray text color |
| `text-gray-700` | Medium gray text color |
| `text-gray-600` | Lighter gray text color |
| `text-white` | White text |
| `text-blue-600` | Blue text |
| `font-bold` | Makes text bold |
| `font-semibold` | Makes text semi-bold |
| `text-lg` | Large text size |
| `text-xl` | Extra large text size |

#### Spacing Classes

| Class | What It Does |
|-------|--------------|
| `p-8` | Padding (internal space) of 8 units |
| `px-4` | Padding on left and right of 4 units |
| `py-20` | Padding on top and bottom of 20 units |
| `mb-6` | Margin bottom (space below) of 6 units |
| `gap-4` | Space between flex/grid items of 4 units |

#### Background & Border Classes

| Class | What It Does |
|-------|--------------|
| `bg-white` | White background |
| `bg-blue-50` | Very light blue background |
| `bg-gray-900` | Dark gray background |
| `border` | Adds a border |
| `border-gray-200` | Light gray border |
| `rounded-2xl` | Rounded corners (extra large) |

#### Responsive Classes

| Class Prefix | Applies To |
|--------------|-----------|
| `md:` | Medium screens (tablets) |
| `lg:` | Large screens (desktops) |
| `hidden lg:block` | Hidden on small screens, visible on large |

### How to Change Colors

Your landing page uses a blue color scheme. To change colors:

#### Change Primary Blue to a Different Color

1. **Find all blue color classes** - They typically look like `from-blue-600`, `bg-blue-50`, `text-blue-600`, etc.

2. **Replace with new color** - Tailwind has these color options:
   - `red`, `orange`, `yellow`, `green`, `blue`, `indigo`, `purple`, `pink`

3. **Keep the number** - The number (50, 100, 200, 600, 700, etc.) indicates the shade:
   - `50` = very light
   - `600` = medium
   - `700` = dark

**Example - Change from Blue to Purple:**

Find:
```html
<div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-blue-700 rounded-full flex items-center justify-center">
```

Change to:
```html
<div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-purple-700 rounded-full flex items-center justify-center">
```

### How to Change Button Styles

Your landing page has two button types: primary (filled) and secondary (outlined).

#### Primary Button (Filled Blue Button)

Find this CSS class definition (lines 34-36):
```css
.btn-primary {
    @apply px-8 py-3 rounded-full font-semibold text-white bg-gradient-to-r from-blue-600 to-blue-700 hover:from-blue-700 hover:to-blue-800 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

**To change button appearance:**

| What You Want | Change This | Example |
|---------------|-------------|---------|
| Make button wider | `px-8` | Change to `px-12` |
| Make button taller | `py-3` | Change to `py-4` |
| Change text color | `text-white` | Change to `text-blue-600` |
| Less rounded corners | `rounded-full` | Change to `rounded-lg` |
| Remove hover effect | Delete `hover:scale-105` | Remove the text |

**Example - Make primary button less rounded:**
```css
.btn-primary {
    @apply px-8 py-3 rounded-lg font-semibold text-white bg-gradient-to-r from-blue-600 to-blue-700 hover:from-blue-700 hover:to-blue-800 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

#### Secondary Button (Outlined Button)

Find this CSS class definition (lines 38-40):
```css
.btn-secondary {
    @apply px-8 py-3 rounded-full font-semibold text-blue-600 bg-white border-2 border-blue-600 hover:bg-blue-50 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

**To change:**
- Follow the same approach as the primary button
- `text-blue-600` = text color
- `border-blue-600` = border color
- `bg-white` = background color

### How to Change Spacing

Spacing classes control padding (internal space) and margins (external space).

#### Change Section Padding

Find this code (appears multiple times):
```html
<section class="py-20 md:py-28 lg:py-32">
```

This means:
- `py-20` = padding top and bottom on small screens
- `md:py-28` = padding top and bottom on medium screens
- `lg:py-32` = padding top and bottom on large screens

**To increase spacing:**
```html
<!-- BEFORE -->
<section class="py-20 md:py-28 lg:py-32">

<!-- AFTER - More space -->
<section class="py-24 md:py-32 lg:py-40">
```

**To decrease spacing:**
```html
<!-- BEFORE -->
<section class="py-20 md:py-28 lg:py-32">

<!-- AFTER - Less space -->
<section class="py-12 md:py-16 lg:py-20">
```

#### Change Gap Between Cards

Find this code (in Features section):
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

The `gap-8` controls space between feature cards.

**To change:**
- `gap-4` = small gap
- `gap-8` = medium gap (current)
- `gap-12` = large gap

### How to Change Responsive Breakpoints

Your page automatically adjusts for different screen sizes using `md:` and `lg:` prefixes.

#### Example - Change how many columns appear on tablets

Find:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

This means:
- `grid-cols-1` = 1 column on small screens (phones)
- `md:grid-cols-2` = 2 columns on medium screens (tablets)
- `lg:grid-cols-3` = 3 columns on large screens (desktops)

**To show 3 columns on tablets instead of 2:**
```html
<div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-3 gap-8">
```

### How to Change Card Hover Effects

Find this CSS class (line 42):
```css
.card-hover {
    @apply transition-all duration-300 hover:scale-105 hover:shadow-xl cursor-pointer;
}
```

This controls what happens when you hover over cards.

**To remove hover effect:**
```css
.card-hover {
    @apply transition-all duration-300 cursor-pointer;
}
```

**To make hover effect more dramatic:**
```css
.card-hover {
    @apply transition-all duration-300 hover:scale-110 hover:shadow-2xl cursor-pointer;
}
```

### Tailwind Color Reference

For your landing page, here are all available colors:

**Neutral Colors:**
- `gray-50`, `gray-100`, `gray-200`, `gray-300`, `gray-400`, `gray-500`, `gray-600`, `gray-700`, `gray-800`, `gray-900`

**Primary Colors:**
- `blue`, `indigo`, `purple`, `pink`

**Secondary Colors:**
- `red`, `orange`, `yellow`, `green`, `teal`, `cyan`

**Example - Change from gray text to blue text:**
```html
<!-- BEFORE -->
<p class="text-gray-600">Description text</p>

<!-- AFTER -->
<p class="text-blue-600">Description text</p>
```

---

## Fixing and Managing Links

Links are crucial for navigation and user engagement. Let's learn how to fix and update them.

### Understanding Link Types in Your Landing Page

Your page has three types of links:

1. **Internal Navigation Links** - Link to sections within the same page
2. **External Links** - Link to other websites
3. **Email Links** - Open the user's email client

### Identifying All Current Links

Here's a complete list of all links in your landing page:

#### Navigation Links (Header)

| Link Text | Current href | Type | Location |
|-----------|-------------|------|----------|
| Features | `#features` | Internal | Header nav |
| Benefits | `#benefits` | Internal | Header nav |
| Testimonials | `#testimonials` | Internal | Header nav |
| About Us | `#about` | Internal | Header nav |
| Contact | `mailto:contact@example.com` | Email | Header nav |
| Get Started | `https://www.example.com` | External | Header nav |

#### Mobile Navigation Links

Same as above, but repeated in mobile menu (lines 102-109)

#### Hero Section Links

| Link Text | Current href | Type | Location |
|-----------|-------------|------|----------|
| Start Your Journey | `https://www.example.com` | External | Hero section |
| Contact Us | `mailto:contact@example.com` | Email | Hero section |

#### CTA Section Links

| Link Text | Current href | Type | Location |
|-----------|-------------|------|----------|
| Start Free Trial | `https://www.example.com` | External | CTA section |
| Schedule Demo | `mailto:contact@example.com` | Email | CTA section |

#### Footer Links

| Link Text | Current href | Type | Location |
|-----------|-------------|------|----------|
| Features | `#features` | Internal | Footer |
| Benefits | `#benefits` | Internal | Footer |
| Testimonials | `#testimonials` | Internal | Footer |
| About | `#about` | Internal | Footer |
| Privacy Policy | `privacy.html` | Page Link | Footer |
| Terms of Service | `terms.html` | Page Link | Footer |
| Blog | `blog.html` | Page Link | Footer |
| Contact | `mailto:contact@example.com` | Email | Footer |
| Twitter | `#` | External | Footer |
| LinkedIn | `#` | External | Footer |
| GitHub | `#` | External | Footer |
| Privacy (footer bottom) | `privacy.html` | Page Link | Footer |
| Terms (footer bottom) | `terms.html` | Page Link | Footer |
| Blog (footer bottom) | `blog.html` | Page Link | Footer |

### How to Fix Placeholder Links

Your landing page currently has placeholder links that need to be updated:

#### 1. Update the Main CTA Link (Sign Up/Get Started)

**Location:** Lines 131, 150, 359, 366

Find:
```html
<a href="https://www.example.com" class="btn-primary text-center">
```

**What to replace:**
- `https://www.example.com` = Your actual signup/application URL

**Example:**
```html
<!-- BEFORE -->
<a href="https://www.example.com" class="btn-primary text-center">

<!-- AFTER -->
<a href="https://yourcompany.com/signup" class="btn-primary text-center">
```

#### 2. Update Contact Email Link

**Location:** Lines 95, 133, 152, 364, 368, 629

Find:
```html
<a href="mailto:contact@example.com" class="nav-link">Contact</a>
```

**What to replace:**
- `contact@example.com` = Your actual email address

**Example:**
```html
<!-- BEFORE -->
<a href="mailto:contact@example.com" class="nav-link">Contact</a>

<!-- AFTER -->
<a href="mailto:hello@yourcompany.com" class="nav-link">Contact</a>
```

#### 3. Update Social Media Links

**Location:** Lines 631-641

Find:
```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-twitter text-white"></i>
</a>
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-linkedin text-white"></i>
</a>
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
    <i class="fab fa-github text-white"></i>
</a>
```

**What to replace:**
- `href="#"` = Your actual social media URLs

**Example:**
```html
<!-- BEFORE -->
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full...">
    <i class="fab fa-twitter text-white"></i>
</a>

<!-- AFTER -->
<a href="https://twitter.com/yourcompany" class="w-10 h-10 bg-gray-800 rounded-full...">
    <i class="fab fa-twitter text-white"></i>
</a>
```

### How to Add New Links

#### Add a New Navigation Menu Item

**Step 1:** Add to desktop navigation menu (lines 85-91)

Find:
```html
<div class="hidden lg:flex items-center gap-8">
    <a href="#features" class="nav-link">Features</a>
    <a href="#benefits" class="nav-link">Benefits</a>
    <a href="#testimonials" class="nav-link">Testimonials</a>
    <a href="#about" class="nav-link">About Us</a>
    <a href="mailto:contact@example.com" class="nav-link">Contact</a>
</div>
```

**Add your new link:**
```html
<div class="hidden lg:flex items-center gap-8">
    <a href="#features" class="nav-link">Features</a>
    <a href="#benefits" class="nav-link">Benefits</a>
    <a href="#testimonials" class="nav-link">Testimonials</a>
    <a href="#about" class="nav-link">About Us</a>
    <a href="#pricing" class="nav-link">Pricing</a>  <!-- NEW -->
    <a href="mailto:contact@example.com" class="nav-link">Contact</a>
</div>
```

**Step 2:** Add to mobile navigation menu (lines 102-109)

Find:
```html
<div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white shadow-lg border-t border-gray-200">
    <div class="max-w-7xl mx-auto px-4 py-4 flex flex-col gap-4">
        <a href="#features" class="nav-link block py-2">Features</a>
        <a href="#benefits" class="nav-link block py-2">Benefits</a>
        <a href="#testimonials" class="nav-link block py-2">Testimonials</a>
        <a href="#about" class="nav-link block py-2">About Us</a>
        <a href="mailto:contact@example.com" class="nav-link block py-2">Contact</a>
        <a href="https://www.example.com" class="btn-primary block text-center">Get Started</a>
    </div>
</div>
```

**Add your new link:**
```html
<div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white shadow-lg border-t border-gray-200">
    <div class="max-w-7xl mx-auto px-4 py-4 flex flex-col gap-4">
        <a href="#features" class="nav-link block py-2">Features</a>
        <a href="#benefits" class="nav-link block py-2">Benefits</a>
        <a href="#testimonials" class="nav-link block py-2">Testimonials</a>
        <a href="#about" class="nav-link block py-2">About Us</a>
        <a href="#pricing" class="nav-link block py-2">Pricing</a>  <!-- NEW -->
        <a href="mailto:contact@example.com" class="nav-link block py-2">Contact</a>
        <a href="https://www.example.com" class="btn-primary block text-center">Get Started</a>
    </div>
</div>
```

### Link Format Reference

#### Internal Navigation Links (Within Same Page)

Format: `href="#section-id"`

```html
<a href="#features">Go to Features</a>
```

**Note:** The section you're linking to must have a matching `id`:
```html
<section id="features">
    <!-- Content here -->
</section>
```

#### External Website Links

Format: `href="https://www.example.com"`

```html
<a href="https://www.yourcompany.com">Visit Our Site</a>
```

**Important:** Always include `https://` at the beginning!

#### Email Links

Format: `href="mailto:email@example.com"`

```html
<a href="mailto:hello@yourcompany.com">Contact Us</a>
```

#### Page Links (Within Your Website)

Format: `href="page-name.html"`

```html
<a href="privacy.html">Privacy Policy</a>
```

---

## Linking Privacy and Terms Pages

Your landing page references `privacy.html`, `terms.html`, and `blog.html` in the footer, but these pages don't exist yet. Let's create them and ensure they're properly linked.

### Step 1: Create the Privacy Policy Page

**1. Create a new file:**
- In your project folder, create a new file named `privacy.html`
- Save it in the same folder as `index.html`

**2. Add this basic template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Twenty One AI">
    <title>Privacy Policy | Twenty One AI</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header & Navigation -->
    <header>
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-blue-700 rounded-full flex items-center justify-center">
                    <i class="fas fa-rocket text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold text-gray-900">Twenty One AI</span>
            </div>
            
            <div class="hidden lg:flex items-center gap-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Back to Home</a>
            </div>
            
            <a href="index.html" class="lg:hidden text-gray-900 hover:text-blue-600 transition-colors duration-300">
                <i class="fas fa-arrow-left text-2xl"></i>
            </a>
        </nav>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-20 md:py-28 lg:py-32">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-8">
                <p>
                    <strong>Last Updated:</strong> January 2025
                </p>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p>
                        Twenty One AI ("Company," "we," "us," or "our") operates the website. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
                    </p>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information Collection and Use</h2>
                    <p>
                        We collect several different types of information for various purposes to provide and improve our Service to you.
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Personal Data: Email address, name, phone number</li>
                        <li>Usage Data: Browser type, IP address, pages visited</li>
                        <li>Cookies and tracking technologies</li>
                    </ul>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Data</h2>
                    <p>
                        Twenty One AI uses the collected data for various purposes:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>To provide and maintain our Service</li>
                        <li>To notify you about changes to our Service</li>
                        <li>To allow you to participate in interactive features</li>
                        <li>To provide customer support</li>
                        <li>To gather analysis or valuable information for improving our Service</li>
                        <li>To monitor the usage of our Service</li>
                    </ul>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Security of Data</h2>
                    <p>
                        The security of your data is important to us, but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                    </p>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Contact Us</h2>
                    <p>
                        If you have any questions about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:contact@example.com" class="text-blue-600 hover:text-blue-700">contact@example.com</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 text-sm mb-4">
                    &copy; 2025 Twenty One AI. All rights reserved.
                </p>
                <div class="flex gap-6 justify-center text-sm">
                    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
                    <a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**1. Create a new file:**
- In your project folder, create a new file named `terms.html`
- Save it in the same folder as `index.html`

**2. Add this basic template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Twenty One AI">
    <title>Terms of Service | Twenty One AI</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header & Navigation -->
    <header>
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-blue-700 rounded-full flex items-center justify-center">
                    <i class="fas fa-rocket text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold text-gray-900">Twenty One AI</span>
            </div>
            
            <div class="hidden lg:flex items-center gap-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Back to Home</a>
            </div>
            
            <a href="index.html" class="lg:hidden text-gray-900 hover:text-blue-600 transition-colors duration-300">
                <i class="fas fa-arrow-left text-2xl"></i>
            </a>
        </nav>
    </header>

    <!-- Terms of Service Content -->
    <section class="py-20 md:py-28 lg:py-32">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-8">
                <p>
                    <strong>Last Updated:</strong> January 2025
                </p>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on Twenty One AI's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on Twenty One AI's website are provided on an 'as is' basis. Twenty One AI makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p>
                        In no event shall Twenty One AI or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Twenty One AI's website.
                    </p>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on Twenty One AI's website could include technical, typographical, or photographic errors. Twenty One AI does not warrant that any of the materials on its website are accurate, complete, or current. Twenty One AI may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>
                
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Contact Us</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:contact@example.com" class="text-blue-600 hover:text-blue-700">contact@example.com</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 text-sm mb-4">
                    &copy; 2025 Twenty One AI. All rights reserved.
                </p>
                <div class="flex gap-6 justify-center text-sm">
                    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
                    <a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Create the Blog Page (Optional)

**1. Create a new file:**
- In your project folder, create a new file named `blog.html`

**2. Add this basic template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - Twenty One AI">
    <title>Blog | Twenty One AI</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header & Navigation -->
    <header>
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-blue-700 rounded-full flex items-center justify-center">
                    <i class="fas fa-rocket text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold text-gray-900">Twenty One AI</span>
            </div>
            
            <div class="hidden lg:flex items-center gap-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Back to Home</a>
            </div>
            
            <a href="index.html" class="lg:hidden text-gray-900 hover:text-blue-600 transition-colors duration-300">
                <i class="fas fa-arrow-left text-2xl"></i>
            </a>
        </nav>
    </header>

    <!-- Blog Content -->
    <section class="py-20 md:py-28 lg:py-32">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Blog</h1>
            <p class="text-lg text-gray-600 mb-12">Stay updated with the latest insights and news from Twenty One AI.</p>
            
            <div class="space-y-12">
                <!-- Blog Post 1 -->
                <article class="border-b border-gray-200 pb-12">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">Getting Started with AI Automation</h2>
                    <p class="text-gray-600 mb-4">Published on January 15, 2025</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Learn how to implement AI automation in your business. In this comprehensive guide, we'll walk you through the basics of workflow automation and how it can transform your operations.
                    </p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </article>
                
                <!-- Blog Post 2 -->
                <article class="border-b border-gray-200 pb-12">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">The Future of Predictive Analytics</h2>
                    <p class="text-gray-600 mb-4">Published on January 10, 2025</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Explore the latest trends in predictive analytics and how machine learning is revolutionizing decision-making across industries.
                    </p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </article>
                
                <!-- Blog Post 3 -->
                <article>
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">Case Study: How Company X Increased Efficiency by 300%</h2>
                    <p class="text-gray-600 mb-4">Published on January 5, 2025</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Discover how one of our clients leveraged our platform to dramatically improve their operational efficiency and reduce costs.
                    </p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </article>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 text-sm mb-4">
                    &copy; 2025 Twenty One AI. All rights reserved.
                </p>
                <div class="flex gap-6 justify-center text-sm">
                    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
                    <a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 4: Verify Footer Links in index.html

Your `index.html` already has the correct links to these pages. Let's verify they're correct:

**Location 1:** Lines 619-626 (Footer Product Links)
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a></li>
```

**Location 2:** Lines 640-644 (Footer Bottom Links)
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
```

✅ **These links are already correct!** Your footer will automatically link to the new pages once you create them.

### Step 5: File Structure After Setup

After completing all steps, your project folder should look like this:

```
your-project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy page) ✓ NEW
├── terms.html (terms of service page) ✓ NEW
└── blog.html (blog page) ✓ NEW
```

### Step 6: Test All Links

**To verify everything works:**

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - should open `privacy.html`
4. Click on "Terms of Service" - should open `terms.html`
5. Click on "Blog" - should open `blog.html`
6. On each policy page, click "Back to Home" to return to `index.html`

---

## Common Customization Tasks

### Task 1: Change the Color Scheme from Blue to Green

**Step 1:** Update primary button styles

Find (line 34):
```css
.btn-primary {
    @apply px-8 py-3 rounded-full font-semibold text-white bg-gradient-to-r from-blue-600 to-blue-700 hover:from-blue-700 hover:to-blue-800 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

Change to:
```css
.btn-primary {
    @apply px-8 py-3 rounded-full font-semibold text-white bg-gradient-to-r from-green-600 to-green-700 hover:from-green-700 hover:to-green-800 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

**Step 2:** Update secondary button styles

Find (line 38):
```css
.btn-secondary {
    @apply px-8 py-3 rounded-full font-semibold text-blue-600 bg-white border-2 border-blue-600 hover:bg-blue-50 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

Change to:
```css
.btn-secondary {
    @apply px-8 py-3 rounded-full font-semibold text-green-600 bg-white border-2 border-green-600 hover:bg-green-50 transform transition-all duration-300 hover:scale-105 hover:shadow-lg cursor-pointer;
}
```

**Step 3:** Update gradient backgrounds

Find (line 24):
```css
.gradient-blue {
    background: linear-gradient(135deg, #0066ff 0%, #0052cc 100%);
}
```

Change to:
```css
.gradient-blue {
    background: linear-gradient(135deg, #059669 0%, #047857 100%);
}
```

**Step 4:** Update all `blue-600` and `blue-700` classes throughout the HTML

Use Find & Replace:
- Find: `blue-600`
- Replace with: `green-600`

Then:
- Find: `blue-700`
- Replace with: `green-700`

And:
- Find: `blue-50`
- Replace with: `green-50`

**Step 5:** Update logo background

Find (line 80):
```html
<div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-blue-700 rounded-full flex items-center justify-center">
```

Change to:
```html
<div class="w-10 h-10 bg-gradient-to-r from-green-600 to-green-700 rounded-full flex items-center justify-center">
```

### Task 2: Add a New Feature Card

**Location:** Features section (lines 160-230)

**Step 1:** Find an existing feature card

```html
<div class="feature-card">
    <div class="w-16 h-16 bg-gradient-to-br from-blue-100 to-blue-50 rounded-2xl flex items-center justify-center mb-6">
        <svg class="w-8 h-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
        </svg>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">Custom AI Workflow Development</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Build bespoke AI workflows...
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-center gap-2">
            <i class="fas fa-check text-blue-600"></i>
            <span>Drag-and-drop workflow builder</span>
        </li>
        <!-- More list items -->
    </ul>
</div>
```

**Step 2:** Copy the entire feature card

**Step 3:** Paste it after the third feature card (after line 227)

**Step 4:** Update the content:
- Change the SVG icon
- Update the title
- Update the description
- Update the bullet points

**Example - New Feature Card:**

```html
<div class="feature-card">
    <div class="w-16 h-16 bg-gradient-to-br from-blue-100 to-blue-50 rounded-2xl flex items-center justify-center mb-6">
        <svg class="w-8 h-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4" />
        </svg>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">Advanced Team Collaboration</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Enable seamless collaboration with real-time updates and integrated communication tools. Keep your entire team synchronized and productive with our unified workspace.
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-center gap-2">
            <i class="fas fa-check text-blue-600"></i>
            <span>Real-time collaboration features</span>
        </li>
        <li class="flex items-center gap-2">
            <i class="fas fa-check text-blue-600"></i>
            <span>Integrated messaging and comments</span>
        </li>
        <li class="flex items-center gap-2">
            <i class="fas fa-check text-blue-600"></i>
            <span>Team permission management</span>
        </li>
    </ul>
</div>
```

**Step 5:** Update the grid to show 4 columns instead of 3

Find (line 161):
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

Change to:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

### Task 3: Change the Hero Section Background Image

**Location:** Lines 304-306 (CTA Section)

Find:
```html
<div class="absolute inset-0 bg-cover bg-center bg-no-repeat" style="background-image: url('https://images.unsplash.com/photo-1552664730-d307ca884978?w=1200&h=600&fit=crop'); opacity: 0.1;"></div>
```

**To change the image:**

1. Find a new image URL on:
   - Unsplash (https://unsplash.com)
   - Pexels (https://pexels.com)
   - Pixabay (https://pixabay.com)

2. Copy the image URL

3. Replace the URL in the code:

```html
<div class="absolute inset-0 bg-cover bg-center bg-no-repeat" style="background-image: url('YOUR_NEW_IMAGE_URL'); opacity: 0.1;"></div>
```

**Example:**
```html
<div class="absolute inset-0 bg-cover bg-center bg-no-repeat" style="background-image: url('https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=1200&h=600&fit=crop'); opacity: 0.1;"></div>
```

### Task 4: Add a New Section to the Page

**Step 1:** Choose where to add the section

Decide if you want to add it:
- After the hero section
- Between features and benefits
- Before testimonials
- After about us

**Step 2:** Create the section HTML

```html
<section id="new-section" class="py-20 md:py-28 lg:py-32 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16 md:mb-20">
            <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 leading-tight">
                Your New Section Title
            </h2>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                Your section description goes here.
            </p>
        </div>
        
        <!-- Your content here -->
    </div>
</section>
```

**Step 3:** Add to navigation menu

Update the header navigation (lines 85-91) to include a link to your new section:

```html
<a href="#new-section" class="nav-link">New Section</a>
```

Also add to mobile menu (lines 102-109):

```html
<a href="#new-section" class="nav-link block py-2">New Section</a>
```

### Task 5: Customize Font Sizes

**To make all text larger:**

Find the `@import` line (line 20):
```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
```

You can change the font family by replacing `Inter` with another Google Font:
- `Roboto`
- `Poppins`
- `Playfair Display`
- `Montserrat`

**Example - Change to Poppins:**
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap');
```

Then update the font-family:
```css
* {
    font-family: 'Poppins', sans-serif;
}
```

---

## Troubleshooting Guide

### Problem 1: Links Not Working

**Symptom:** Clicking a link does nothing or shows an error

**Solution:**

1. **For internal links (starting with `#`):**
   - Make sure the section has a matching `id`
   - Example: `<a href="#features">` needs `<section id="features">`
   - Check for typos in the `href` and `id`

2. **For external links:**
   - Make sure the URL starts with `https://` or `http://`
   - Test the URL in a browser to ensure it's valid
   - Example: `<a href="https://www.example.com">` ✓

3. **For email links:**
   - Make sure it starts with `mailto:`
   - Example: `<a href="mailto:hello@example.com">` ✓

4. **For page links:**
   - Make sure the filename matches exactly (case-sensitive)
   - File should be in the same folder as `index.html`
   - Example: `<a href="privacy.html">` ✓

### Problem 2: Text Not Updating

**Symptom:** Changed text in the HTML but it's not showing on the website

**Solutions:**

1. **Hard refresh your browser:**
   - Windows: Press `Ctrl + Shift + R`
   - Mac: Press `Cmd + Shift + R`

2. **Clear browser cache:**
   - Chrome: Settings → Privacy → Clear browsing data
   - Firefox: Preferences → Privacy → Clear Data

3. **Make sure you saved the file:**
   - Press `Ctrl + S` (Windows) or `Cmd + S` (Mac)

4. **Check for typos:**
   - Missing closing tags `</p>`, `</div>`, etc.
   - Mismatched quotes or brackets

### Problem 3: Styling Not Applying

**Symptom:** Changed Tailwind classes but styling doesn't change

**Solutions:**

1. **Make sure you're using valid Tailwind classes:**
   - Check the Tailwind documentation
   - Common mistake: `text-size-lg` (wrong) vs `text-lg` (correct)

2. **Verify class syntax:**
   - Classes should be in the `class=""` attribute
   - Multiple classes separated by spaces: `class="text-lg font-bold text-blue-600"`

3. **Check for conflicting classes:**
   - If you have `text-gray-900` and `text-white`, the last one wins
   - Remove duplicate or conflicting classes

4. **Hard refresh browser** (same as Problem 2)

### Problem 4: Mobile Menu Not Working

**Symptom:** Mobile menu button doesn't open/close

**Solutions:**

1. **Check JavaScript is enabled:**
   - Browser settings should have JavaScript enabled
   - Most browsers enable it by default

2. **Verify the mobile menu HTML:**
   - Make sure the mobile menu `<div>` has `class="mobile-menu hidden"`
   - Make sure the button has `class="mobile-menu-button"`

3. **Check for JavaScript errors:**
   - Open browser developer tools (F12)
   - Check the Console tab for red error messages
   - Fix any errors shown

### Problem 5: Colors Not Changing

**Symptom:** Changed color classes but colors don't update

**Solutions:**

1. **Use valid Tailwind color names:**
   - Valid: `text-blue-600`, `bg-green-50`, `border-red-200`
   - Invalid: `text-blue`, `bg-green`, `text-darkblue`

2. **Remember the color scale:**
   - `50` = lightest
   - `100`, `200`, `300` = light shades
   - `400`, `500` = medium shades
   - `600`, `700`, `800` = dark shades
   - `900` = darkest

3. **Replace all instances:**
   - If changing from blue to green, replace ALL instances
   - Use Find & Replace to ensure you catch them all

### Problem 6: Page Layout Broken on Mobile

**Symptom:** Page looks wrong on phones or tablets

**Solutions:**

1. **Check responsive classes:**
   - `md:` applies to tablets and larger
   - `lg:` applies to desktops and larger
   - Make sure you have mobile-first classes

2. **Test on actual devices:**
   - Use browser developer tools (F12)
   - Click the mobile device icon to simulate different screen sizes

3. **Check grid and flex layouts:**
   - `grid-cols-1` = 1 column on mobile
   - `md:grid-cols-2` = 2 columns on tablets
   - `lg:grid-cols-3` = 3 columns on desktops

### Problem 7: Images Not Showing

**Symptom:** Image URLs show broken image icon

**Solutions:**

1. **Check URL format:**
   - External URLs: Must start with `https://`
   - Local files: Must be in the same folder and use correct filename

2. **Verify the URL:**
   - Copy the URL into your browser
   - If it doesn't load in browser, the URL is wrong

3. **Check file paths:**
   - If using local images, create an `images` folder
   - Reference it like: `<img src="images/photo.jpg">`

### Problem 8: Buttons Not Clickable

**Symptom:** Buttons look right but don't respond to clicks

**Solutions:**

1. **Check the `href` attribute:**
   - Buttons must have `href="#"` or a valid URL
   - Example: `<a href="https://example.com" class="btn-primary">Click Me</a>`

2. **Verify it's an `<a>` tag:**
   - Use `<a>` for links
   - Use `<button>` for forms
   - Use `<div>` with JavaScript for custom functionality

3. **Check for JavaScript errors:**
   - Open developer tools (F12)
   - Check the Console tab
   - Fix any errors shown

### Problem 9: Footer Links Lead to 404 Error

**Symptom:** Privacy, Terms, or Blog links show "page not found"

**Solution:**

1. **Make sure you created the files:**
   - `privacy.html` ✓
   - `terms.html` ✓
   - `blog.html` ✓

2. **Verify file names match exactly:**
   - Check for typos
   - Check capitalization (usually lowercase)
   - Ensure `.html` extension

3. **Verify files are in correct folder:**
   - All HTML files should be in the same folder
   - Example structure:
     ```
     project-folder/
     ├── index.html
     ├── privacy.html
     ├── terms.html
     └── blog.html
     ```

### Problem 10: Page Loads Slowly

**Symptom:** Website takes a long time to load

**Solutions:**

1. **Compress images:**
   - Use tools like TinyPNG or ImageOptim
   - Replace large images with smaller versions

2. **Remove unused CSS:**
   - Only load Tailwind CSS if needed
   - Minimize custom CSS

3. **Optimize external resources:**
   - Use CDN versions of libraries
   - Load non-critical scripts asynchronously

4. **Check browser cache:**
   - Hard refresh (Ctrl+Shift+R)
   - Clear browser cache

---

## Best Practices for Maintenance

### Regular Maintenance Checklist

- [ ] **Weekly:** Check that all links are working
- [ ] **Monthly:** Update testimonials and case studies
- [ ] **Quarterly:** Review and update statistics
- [ ] **Yearly:** Refresh design and content
- [ ] **Always:** Test on mobile devices before publishing

### Version Control Tips

1. **Keep backups:**
   - Save copies of original files
   - Use version control (Git) if possible

2. **Comment your changes:**
   - Add HTML comments explaining modifications
   - Example: `<!-- Updated hero section on Jan 15, 2025 -->`

3. **Test before publishing:**
   - Test all links
   - Test on multiple browsers
   - Test on mobile devices

### Accessibility Improvements

1. **Add alt text to images:**
   ```html
   <img src="image.jpg" alt="Description of image">
   ```

2. **Use proper heading hierarchy:**
   - Use `<h1>` for main title
   - Use `<h2>` for section titles
   - Don't skip heading levels

3. **Ensure color contrast:**
   - Text should be readable on background
   - Use tools like WebAIM Color Contrast Checker

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing your Twenty One AI landing page. Remember:

- **Start small:** Make one change at a time
- **Test frequently:** Check your work as you go
- **Keep backups:** Always have a copy of the original
- **Ask for help:** When stuck, consult documentation or forums

For additional help:
- **Tailwind CSS Docs:** https://tailwindcss.com/docs
- **HTML Reference:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **Font Awesome Icons:** https://fontawesome.com/icons

Happy customizing! 🚀