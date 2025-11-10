# Pogiso's Tours Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Updating Text and Content](#updating-text-and-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Color Scheme Customization](#color-scheme-customization)
8. [Troubleshooting Guide](#troubleshooting-guide)

---

## Overview

This README provides step-by-step guidance for maintaining and customizing the Pogiso's Tours executive shuttle landing page. The page uses:

- **HTML5** for structure
- **Tailwind CSS** for styling (via CDN)
- **Font Awesome** for icons
- **Google Fonts** for typography (Space Grotesk and Inter)

The landing page is built as a single-page application with multiple sections that showcase services, benefits, testimonials, FAQs, and contact information.

---

## Project Structure

```
Your Project Folder/
├── index.html                 (Main landing page)
├── privacy.html              (Privacy Policy page - needs to be created)
├── terms.html                (Terms of Service page - needs to be created)
└── blog.html                 (Blog page - needs to be created)
```

### Key Sections in index.html:

| Section | Purpose | Location in Code |
|---------|---------|-----------------|
| Header/Navigation | Main menu and branding | Lines 56-107 |
| Hero Section | Main headline and CTA | Lines 109-166 |
| Features Section | Service highlights | Lines 168-221 |
| Benefits Section | Why choose us | Lines 223-288 |
| CTA Section | Call-to-action with background | Lines 290-312 |
| Testimonials Section | Client reviews | Lines 314-397 |
| About Us Section | Company information | Lines 399-451 |
| FAQ Section | Questions and answers | Lines 453-545 |
| Contact CTA Section | Contact information | Lines 547-564 |
| Contact Form Section | Web form | Lines 566-664 |
| Footer | Links and company info | Lines 666-727 |

---

## Updating Text and Content

### 1. Updating the Header/Navigation

**Location:** Lines 56-107

The header contains your company logo, navigation links, and booking button.

#### Change the Company Name

**Current code:**
```html
<div class="flex items-center gap-2">
    <i class="fas fa-shuttle-van text-3xl" style="color: #FF5A5F;"></i>
    <span class="text-2xl font-bold" style="color: #FF5A5F;">Pogiso's Tours</span>
</div>
```

**To change it:**
1. Open `index.html` in your text editor
2. Find the line: `<span class="text-2xl font-bold" style="color: #FF5A5F;">Pogiso's Tours</span>`
3. Replace `Pogiso's Tours` with your company name
4. Save the file

**Example:**
```html
<span class="text-2xl font-bold" style="color: #FF5A5F;">Your Company Name</span>
```

#### Update Navigation Menu Links

**Current code (Desktop Menu):**
```html
<div class="hidden md:flex items-center gap-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
</div>
```

**To add or change menu items:**
1. Find the navigation section (around line 71-77 for desktop)
2. To add a new menu item, add this line:
   ```html
   <a href="#section-id" class="text-gray-300 hover:text-white transition-colors duration-300">Menu Item Name</a>
   ```
3. Replace `section-id` with the ID of the section you want to link to
4. Replace `Menu Item Name` with the text you want to display

**Important:** Update the mobile menu (lines 95-102) with the same changes.

### 2. Updating the Hero Section

**Location:** Lines 109-166

This is the main headline area with the large title.

#### Change the Main Headline

**Current code:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold leading-tight mb-6 tracking-tight">
    <span style="color: #FF5A5F;">Executive Shuttle</span> & <span style="color: #FFD166;">VIP Transport</span>
</h1>
```

**To change it:**
1. Find this section around line 123
2. Replace the text between the `<span>` tags with your own headline
3. The `<span style="color: #FF5A5F;">` makes text red
4. The `<span style="color: #FFD166;">` makes text yellow

**Example:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold leading-tight mb-6 tracking-tight">
    <span style="color: #FF5A5F;">Premium</span> & <span style="color: #FFD166;">Reliable Transport</span>
</h1>
```

#### Change the Subheadline

**Current code:**
```html
<p class="text-xl sm:text-2xl text-gray-300 mb-4 font-light">
    For Business & Leisure
</p>
```

**To change it:**
1. Find line 130
2. Replace `For Business & Leisure` with your text

#### Change the Secondary Headline

**Current code:**
```html
<h2 class="text-3xl sm:text-4xl font-bold mb-12 text-gray-100">
    <i class="fas fa-arrow-right" style="color: #FF5A5F;"></i> Corporate Transfers. Elite Tours. Arrive in Style. <i class="fas fa-arrow-left" style="color: #FF5A5F;"></i>
</h2>
```

**To change it:**
1. Find line 134
2. Replace the text between the arrows with your message
3. Keep the `<i class="fas fa-arrow-right">` and `<i class="fas fa-arrow-left">` tags for the arrows

### 3. Updating the Features Section

**Location:** Lines 168-221

This section has three feature cards with icons and descriptions.

#### Change Feature Title

**Current code (Feature 1):**
```html
<h3 class="text-2xl font-bold mb-4">24/7 Service Availability</h3>
```

**To change it:**
1. Find the feature you want to update (around lines 189, 201, 213)
2. Replace the text in the `<h3>` tag
3. Keep the `class="text-2xl font-bold mb-4"` as is

#### Change Feature Description

**Current code:**
```html
<p class="text-gray-300 font-light leading-relaxed">
    Round-the-clock transportation services designed to accommodate your schedule...
</p>
```

**To change it:**
1. Find the paragraph (`<p>` tag) under each feature title
2. Replace the text while keeping all the class attributes
3. Do not delete the `class="text-gray-300 font-light leading-relaxed"` part

#### Change Feature Icon

**Current code:**
```html
<i class="fas fa-clock text-3xl" style="color: #FF5A5F;"></i>
```

**To change the icon:**
1. Visit [Font Awesome Icons](https://fontawesome.com/icons) to find icon names
2. Replace `fa-clock` with your chosen icon name (e.g., `fa-star`, `fa-heart`, `fa-check`)
3. Keep `fas` and the color style

**Example:**
```html
<i class="fas fa-star text-3xl" style="color: #FF5A5F;"></i>
```

### 4. Updating the Benefits Section

**Location:** Lines 223-288

Similar structure to Features but in a 2-column layout.

**Follow the same process as Features:**
- Update titles in `<h3>` tags
- Update descriptions in `<p>` tags
- Change icons using Font Awesome names

### 5. Updating the Testimonials Section

**Location:** Lines 314-397

#### Change Testimonial Text

**Current code:**
```html
<p class="text-gray-300 font-light mb-6 leading-relaxed">
    "Pogiso's Tours transformed our executive travel program..."
</p>
```

**To change it:**
1. Find the testimonial paragraph
2. Replace the text inside the quotes
3. Keep the opening and closing quote marks

#### Change Testimonial Author

**Current code:**
```html
<p class="font-bold">Sarah Johnson</p>
<p class="text-sm text-gray-400">CEO, TechVision Solutions</p>
```

**To change it:**
1. Replace `Sarah Johnson` with the person's name
2. Replace `CEO, TechVision Solutions` with their title and company

### 6. Updating the About Us Section

**Location:** Lines 399-451

#### Change Company Story

**Current code:**
```html
<p class="text-lg text-gray-300 font-light leading-relaxed mb-6">
    Founded in 2010, Pogiso's Tours began with a simple vision...
</p>
```

**To change it:**
1. Find the paragraph in the first box
2. Replace the entire text with your company story
3. Keep all the class attributes

#### Change Company Mission

The second paragraph (starting with "Our mission is...") can be updated the same way.

#### Update Statistics

**Current code:**
```html
<div class="text-center">
    <div class="text-4xl font-bold" style="color: #FF5A5F;">500+</div>
    <p class="text-gray-300 font-light mt-2">Corporate Clients</p>
</div>
```

**To change it:**
1. Replace `500+` with your number
2. Replace `Corporate Clients` with your metric

### 7. Updating the FAQ Section

**Location:** Lines 453-545

#### Change FAQ Question

**Current code:**
```html
<h3 class="text-lg font-bold">How far in advance should I book a vehicle?</h3>
```

**To change it:**
1. Find the question in the `<h3>` tag
2. Replace with your question
3. Keep the class attributes

#### Change FAQ Answer

**Current code:**
```html
<p>For regular bookings, we recommend booking at least 24 hours in advance...</p>
```

**To change it:**
1. Find the answer in the `<p>` tag inside the `.faq-answer` div
2. Replace with your answer
3. Keep all formatting

#### Add New FAQ Item

To add a new FAQ question and answer:

1. Find the last FAQ item (around line 535)
2. Copy the entire FAQ item block:
```html
<div class="faq-item bg-gray-900 rounded-lg px-8 py-6 border border-gray-700">
    <div class="faq-question">
        <h3 class="text-lg font-bold">Your Question Here</h3>
        <i class="fas fa-chevron-down faq-icon"></i>
    </div>
    <div class="faq-answer hidden">
        <p>Your answer here</p>
    </div>
</div>
```

3. Paste it before the closing `</div>` of the FAQ section
4. Update the question and answer text
5. Do NOT change the class names or structure

### 8. Updating the Footer

**Location:** Lines 666-727

#### Change Footer Company Description

**Current code:**
```html
<p class="text-gray-400 font-light leading-relaxed">
    Premium executive transportation and VIP services for business and leisure travel.
</p>
```

**To change it:**
1. Find this paragraph in the first column
2. Replace with your company description

#### Update Footer Service Links

**Current code:**
```html
<li><a href="#features" class="hover:text-white transition-colors duration-300">Corporate Transfers</a></li>
```

**To change it:**
1. Find the Services column (around line 689)
2. Replace the link text with your services
3. Keep the `href="#features"` pointing to correct sections

#### Update Footer Company Links

**Current code:**
```html
<li><a href="#about" class="hover:text-white transition-colors duration-300">About Us</a></li>
```

**To change it:**
1. Find the Company column (around line 698)
2. Update link text as needed
3. Ensure href attributes point to correct sections

#### Update Copyright Year

**Current code:**
```html
<p>&copy; 2025 Pogiso's Tours. All rights reserved.</p>
```

**To change it:**
1. Find this line (around line 724)
2. Update the year to current year
3. Replace `Pogiso's Tours` with your company name

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS, you add pre-made classes to HTML elements.

### Understanding Tailwind Classes in This Project

#### Common Spacing Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `p-8` | Padding (space inside) | `<div class="p-8">` |
| `m-6` | Margin (space outside) | `<div class="m-6">` |
| `mb-4` | Margin bottom | `<h3 class="mb-4">` |
| `px-4` | Padding left and right | `<section class="px-4">` |
| `py-16` | Padding top and bottom | `<section class="py-16">` |
| `gap-8` | Space between items in a grid/flex | `<div class="gap-8">` |

#### Common Text Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-2xl` | Font size (very large) | `<h1 class="text-2xl">` |
| `font-bold` | Make text bold | `<h1 class="font-bold">` |
| `text-gray-300` | Text color (light gray) | `<p class="text-gray-300">` |
| `text-white` | Text color (white) | `<p class="text-white">` |
| `font-light` | Make text thin/light | `<p class="font-light">` |
| `leading-relaxed` | Line height (space between lines) | `<p class="leading-relaxed">` |

#### Common Layout Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `flex` | Display as flexbox | `<div class="flex">` |
| `grid` | Display as grid | `<div class="grid">` |
| `grid-cols-3` | 3 columns in grid | `<div class="grid grid-cols-3">` |
| `md:grid-cols-2` | 2 columns on medium screens | `<div class="md:grid-cols-2">` |
| `items-center` | Align items vertically | `<div class="items-center">` |
| `justify-center` | Align items horizontally | `<div class="justify-center">` |

#### Responsive Design Classes

Tailwind uses prefixes for different screen sizes:

| Prefix | Screen Size | When It Applies |
|--------|-------------|-----------------|
| None | Mobile | Default (small screens) |
| `sm:` | Small | 640px and up |
| `md:` | Medium | 768px and up |
| `lg:` | Large | 1024px and up |
| `xl:` | Extra Large | 1280px and up |

**Example:**
```html
<div class="text-2xl md:text-4xl lg:text-5xl">
    <!-- Mobile: 2xl size -->
    <!-- Tablet and up: 4xl size -->
    <!-- Desktop and up: 5xl size -->
</div>
```

### Common Modifications

#### Change Section Padding

**Current code:**
```html
<section class="py-16 md:py-24 px-4 sm:px-6 lg:px-8">
```

**What it means:**
- `py-16` = Padding top and bottom on mobile (16 units)
- `md:py-24` = Padding top and bottom on tablets (24 units)
- `px-4` = Padding left and right on mobile (4 units)
- `lg:px-8` = Padding left and right on desktop (8 units)

**To increase padding:**
- Change `py-16` to `py-20` or `py-24`
- Change `md:py-24` to `md:py-32`

#### Change Text Size

**Current code:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl">
```

**What it means:**
- `text-5xl` = Extra large on mobile
- `sm:text-6xl` = Even larger on small screens
- `lg:text-7xl` = Largest on desktop

**To make text smaller:**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl">
```

**Text size scale:** `text-sm` < `text-base` < `text-lg` < `text-xl` < `text-2xl` < `text-3xl` < `text-4xl` < `text-5xl` < `text-6xl` < `text-7xl`

#### Change Grid Columns

**Current code:**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**What it means:**
- `grid-cols-1` = 1 column on mobile
- `md:grid-cols-3` = 3 columns on tablets and up
- `gap-8` = Space between items

**To change to 2 columns on desktop:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

#### Change Background Color

**Current code:**
```html
<section class="bg-gray-900 text-white">
```

**What it means:**
- `bg-gray-900` = Very dark gray background
- `text-white` = White text

**Available colors:**
- Grays: `bg-gray-50`, `bg-gray-100`, `bg-gray-200`, ... `bg-gray-900`
- Colors: `bg-red-500`, `bg-blue-500`, `bg-green-500`, etc.

**To change to a different background:**
```html
<section class="bg-gray-800 text-white">
```

#### Change Border Style

**Current code:**
```html
<div class="border border-gray-700 rounded-xl">
```

**What it means:**
- `border` = Add a border
- `border-gray-700` = Border color (dark gray)
- `rounded-xl` = Round the corners

**To remove border:**
```html
<div class="rounded-xl">
```

**To change border color:**
```html
<div class="border border-red-500 rounded-xl">
```

**To change corner roundness:**
- `rounded-none` = No rounding
- `rounded-sm` = Slightly rounded
- `rounded-lg` = Rounded
- `rounded-xl` = Very rounded
- `rounded-full` = Completely round

#### Change Shadow Effect

**Current code:**
```html
<div class="shadow-lg hover:shadow-2xl">
```

**What it means:**
- `shadow-lg` = Large shadow
- `hover:shadow-2xl` = Extra large shadow on hover

**Shadow options:**
- `shadow-sm` = Small shadow
- `shadow` = Normal shadow
- `shadow-lg` = Large shadow
- `shadow-xl` = Extra large shadow
- `shadow-2xl` = Huge shadow
- `shadow-none` = No shadow

### Adding Custom Styles

For styles not available in Tailwind, use inline styles:

**Current code:**
```html
<span style="color: #FF5A5F;">Executive Shuttle</span>
```

**To change the color:**
```html
<span style="color: #00FF00;">Your Text</span>
```

**Common inline styles:**
- `style="color: #FF5A5F;"` = Text color
- `style="background-color: #FF5A5F;"` = Background color
- `style="font-size: 20px;"` = Font size
- `style="margin: 20px;"` = Margin
- `style="padding: 20px;"` = Padding

---

## Fixing and Managing Links

### Understanding Links in This Project

The landing page has several types of links:

1. **Internal Navigation Links** - Links to sections on the same page
2. **External Links** - Links to external websites
3. **Email Links** - Links that open email
4. **Phone Links** - Links that make phone calls
5. **Footer Links** - Links to other pages

### Current Links Analysis

#### Navigation Links (Header & Mobile Menu)

**Location:** Lines 71-77 (Desktop) and 95-102 (Mobile)

**Current code:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
```

**How they work:**
- `href="#features"` tells the browser to jump to the section with `id="features"`
- These are internal links (same page)
- They're working correctly and don't need changes unless you rename section IDs

#### Booking Links (External)

**Location:** Multiple locations - Lines 79, 141, 143, 548

**Current code:**
```html
<a href="https://pogisostours.co.za/booking" class="btn-outline">Book Now</a>
```

**To update the booking URL:**
1. Find all instances of `https://pogisostours.co.za/booking`
2. Replace with your booking page URL
3. Keep the link text the same or change it as needed

**How to find all booking links:**
- Use keyboard shortcut: `Ctrl+F` (Windows) or `Cmd+F` (Mac)
- Search for: `pogisostours.co.za/booking`
- Replace each one with your URL

#### Email Links

**Location:** Lines 552, 709

**Current code:**
```html
<a href="mailto:info@pogisostours.co.za" class="btn-outline">
    <i class="fas fa-envelope mr-2"></i>info@pogisostours.co.za
</a>
```

**To update the email:**
1. Find `mailto:info@pogisostours.co.za`
2. Replace `info@pogisostours.co.za` with your email address
3. Also update the visible text to match

**Example:**
```html
<a href="mailto:contact@yourcompany.com" class="btn-outline">
    <i class="fas fa-envelope mr-2"></i>contact@yourcompany.com
</a>
```

#### Phone Links

**Location:** Lines 554 (Contact CTA)

**Current code:**
```html
<a href="https://pogisostours.co.za/booking" class="btn-outline-yellow">
    <i class="fas fa-phone mr-2"></i>Get a Quote
</a>
```

**To add a phone link instead:**
```html
<a href="tel:+27123456789" class="btn-outline-yellow">
    <i class="fas fa-phone mr-2"></i>+27 (123) 456-789
</a>
```

**Format:** `href="tel:+[country code][number]"`

#### Footer Links

**Location:** Lines 689-710

**Services Links (Lines 689-693):**
```html
<li><a href="#features" class="hover:text-white transition-colors duration-300">Corporate Transfers</a></li>
<li><a href="#features" class="hover:text-white transition-colors duration-300">Airport Shuttles</a></li>
<li><a href="#features" class="hover:text-white transition-colors duration-300">VIP Tours</a></li>
<li><a href="#features" class="hover:text-white transition-colors duration-300">Event Transport</a></li>
```

**These all point to #features.** To customize:
- Keep `href="#features"` for services overview
- Or create separate sections for each service and link to them
- Change the link text to match your services

**Company Links (Lines 698-702):**
```html
<li><a href="#about" class="hover:text-white transition-colors duration-300">About Us</a></li>
<li><a href="#testimonials" class="hover:text-white transition-colors duration-300">Testimonials</a></li>
<li><a href="#faq" class="hover:text-white transition-colors duration-300">FAQ</a></li>
<li><a href="https://pogisostours.co.za/booking" class="hover:text-white transition-colors duration-300">Book Now</a></li>
```

**These are correct.** Only update the booking URL.

**Legal Links (Lines 707-710):**
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="hover:text-white transition-colors duration-300">Blog</a></li>
```

**These point to files that need to be created.** See the next section.

### Step-by-Step: Update All Links

**Step 1: Find the Booking URL**
1. Open `index.html`
2. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac)
3. Type: `pogisostours.co.za/booking`
4. Note how many results appear (should be around 4-5)

**Step 2: Replace Booking URLs**
1. Click the replace option (usually shows "Replace All" button)
2. Type your booking page URL
3. Click "Replace All"
4. Save the file

**Step 3: Update Email Address**
1. Press `Ctrl+F` again
2. Search for: `info@pogisostours.co.za`
3. Replace with your email
4. Save the file

**Step 4: Verify All Links**
1. Open the file in a web browser
2. Click each link to ensure it works
3. Check that internal links jump to correct sections
4. Check that external links open in new tabs

### Common Link Issues and Fixes

**Issue: Link doesn't work**
- **Cause:** Typo in URL
- **Fix:** Copy and paste the correct URL
- **Example:** `https://pogisostours.co.za/booking` (not `pogisostours.co.za/booking`)

**Issue: Internal link doesn't jump to section**
- **Cause:** Section ID doesn't match link href
- **Fix:** Ensure `href="#features"` matches `id="features"` on the section
- **Check:** Look for `<section id="features">` in the HTML

**Issue: Email link doesn't open email client**
- **Cause:** Missing `mailto:` prefix
- **Fix:** Use `href="mailto:email@example.com"`

**Issue: Phone link doesn't dial**
- **Cause:** Missing `tel:` prefix
- **Fix:** Use `href="tel:+1234567890"`

---

## Adding Privacy and Terms Pages

The landing page currently links to `privacy.html` and `terms.html` in the footer (lines 707-708), but these files don't exist yet. Follow this guide to create them.

### Step 1: Create the Privacy Policy Page

**1. Create a new file:**
1. Open your text editor (same one you use for index.html)
2. Click "File" > "New File"
3. Copy and paste the code below
4. Save as `privacy.html` in the same folder as `index.html`

**2. Privacy Policy HTML Template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Pogiso's Tours">
    <meta name="author" content="Pogiso's Tours">
    <title>Privacy Policy | Pogiso's Tours</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            letter-spacing: -0.02em;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <i class="fas fa-shuttle-van text-3xl" style="color: #FF5A5F;"></i>
                <span class="text-2xl font-bold" style="color: #FF5A5F;">Pogiso's Tours</span>
            </div>
            
            <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">
                <i class="fas fa-arrow-left mr-2"></i>Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 px-4 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold mb-12">
                Privacy <span style="color: #FF5A5F;">Policy</span>
            </h1>
            
            <div class="space-y-8 text-gray-300 leading-relaxed">
                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">1. Introduction</h2>
                    <p>
                        Pogiso's Tours ("we," "us," "our," or "Company") is committed to protecting your privacy. 
                        This Privacy Policy explains how we collect, use, disclose, and otherwise process personal 
                        information in connection with our services.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">2. Information We Collect</h2>
                    <p class="mb-4">We collect information you provide directly, such as:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Name and contact information</li>
                        <li>Email address and phone number</li>
                        <li>Booking and travel preferences</li>
                        <li>Payment information</li>
                        <li>Communication preferences</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">3. How We Use Your Information</h2>
                    <p class="mb-4">We use the information we collect to:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Provide and improve our transportation services</li>
                        <li>Process bookings and payments</li>
                        <li>Communicate with you about your bookings</li>
                        <li>Send promotional materials (with your consent)</li>
                        <li>Comply with legal obligations</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">4. Information Sharing</h2>
                    <p>
                        We do not sell, trade, or rent your personal information to third parties. We may share 
                        information with service providers who assist us in operating our website and conducting 
                        our business, subject to confidentiality agreements.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">5. Data Security</h2>
                    <p>
                        We implement appropriate technical and organizational measures to protect your personal 
                        information against unauthorized access, alteration, disclosure, or destruction. However, 
                        no method of transmission over the internet is 100% secure.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">6. Your Rights</h2>
                    <p class="mb-4">Depending on your location, you may have the right to:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Access your personal information</li>
                        <li>Correct inaccurate information</li>
                        <li>Request deletion of your information</li>
                        <li>Opt-out of marketing communications</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">7. Contact Us</h2>
                    <p>
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                        <br><br>
                        <strong>Email:</strong> <a href="mailto:info@pogisostours.co.za" class="text-blue-400 hover:text-blue-300">info@pogisostours.co.za</a>
                        <br>
                        <strong>Last Updated:</strong> January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto text-center text-gray-400 font-light">
            <p>&copy; 2025 Pogiso's Tours. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

**3. Customize the Privacy Policy:**
1. Replace `info@pogisostours.co.za` with your email
2. Update the company name if needed
3. Modify the sections to match your actual practices
4. Update the "Last Updated" date

### Step 2: Create the Terms of Service Page

**1. Create a new file:**
1. Open your text editor
2. Click "File" > "New File"
3. Copy and paste the code below
4. Save as `terms.html` in the same folder as `index.html`

**2. Terms of Service HTML Template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Pogiso's Tours">
    <meta name="author" content="Pogiso's Tours">
    <title>Terms of Service | Pogiso's Tours</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            letter-spacing: -0.02em;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <i class="fas fa-shuttle-van text-3xl" style="color: #FF5A5F;"></i>
                <span class="text-2xl font-bold" style="color: #FF5A5F;">Pogiso's Tours</span>
            </div>
            
            <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">
                <i class="fas fa-arrow-left mr-2"></i>Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 px-4 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold mb-12">
                Terms of <span style="color: #FF5A5F;">Service</span>
            </h1>
            
            <div class="space-y-8 text-gray-300 leading-relaxed">
                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">1. Acceptance of Terms</h2>
                    <p>
                        By accessing and using this website and booking our transportation services, you accept and 
                        agree to be bound by the terms and provision of this agreement. If you do not agree to abide 
                        by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">2. Use License</h2>
                    <p class="mb-4">Permission is granted to temporarily download one copy of the materials (information or software) 
                    on Pogiso's Tours website for personal, non-commercial transitory viewing only. This is the grant of a license, 
                    not a transfer of title, and under this license you may not:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">3. Booking and Reservations</h2>
                    <p class="mb-4">
                        When you book a transportation service through our website or by contacting us directly:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>You agree to provide accurate and complete information</li>
                        <li>You are responsible for confirming your booking details</li>
                        <li>We will confirm your booking via email</li>
                        <li>Bookings are subject to availability</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">4. Cancellation Policy</h2>
                    <p class="mb-4">
                        <strong>Cancellations made 24 hours or more before the scheduled pickup:</strong> Free of charge
                        <br><br>
                        <strong>Cancellations made within 24 hours:</strong> 50% cancellation fee
                        <br><br>
                        <strong>Cancellations made within 2 hours of pickup:</strong> Full charge applies
                        <br><br>
                        Corporate clients may negotiate customized cancellation terms based on their volume and usage patterns.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">5. Payment Terms</h2>
                    <p>
                        Payment is required at the time of booking or as per your agreed corporate arrangement. 
                        We accept credit cards, bank transfers, and cash payments. All prices are subject to change 
                        without notice. We reserve the right to refuse service if payment cannot be verified.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">6. Liability Disclaimer</h2>
                    <p>
                        The materials on Pogiso's Tours website are provided on an 'as is' basis. Pogiso's Tours makes 
                        no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, 
                        without limitation, implied warranties or conditions of merchantability, fitness for a particular 
                        purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">7. Limitations</h2>
                    <p>
                        In no event shall Pogiso's Tours or its suppliers be liable for any damages (including, without limitation, 
                        damages for loss of data or profit, or due to business interruption) arising out of the use or inability 
                        to use the materials on Pogiso's Tours website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">8. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on Pogiso's Tours website could include technical, typographical, or 
                        photographic errors. Pogiso's Tours does not warrant that any of the materials on its website are accurate, 
                        complete, or current. Pogiso's Tours may make changes to the materials contained on its website at any time 
                        without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">9. Links</h2>
                    <p>
                        Pogiso's Tours has not reviewed all of the sites linked to its website and is not responsible for the 
                        contents of any such linked site. The inclusion of any link does not imply endorsement by Pogiso's Tours 
                        of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">10. Modifications</h2>
                    <p>
                        Pogiso's Tours may revise these terms of service for its website at any time without notice. 
                        By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">11. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of South Africa, 
                        and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4 text-white">12. Contact Information</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                        <br><br>
                        <strong>Email:</strong> <a href="mailto:info@pogisostours.co.za" class="text-blue-400 hover:text-blue-300">info@pogisostours.co.za</a>
                        <br>
                        <strong>Last Updated:</strong> January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto text-center text-gray-400 font-light">
            <p>&copy; 2025 Pogiso's Tours. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

**3. Customize the Terms of Service:**
1. Replace `info@pogisostours.co.za` with your email
2. Update the company name if needed
3. Modify the cancellation policy to match your actual policy
4. Update the governing law section if needed
5. Update the "Last Updated" date

### Step 3: Verify the Links Work

**1. Test from the main page:**
1. Open `index.html` in your web browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`

**2. Test the back button:**
1. From either policy page, click "Back to Home"
2. It should return to `index.html`

**3. Troubleshooting:**
- If links don't work, check that all three files (`index.html`, `privacy.html`, `terms.html`) are in the same folder
- Check that file names match exactly (case-sensitive on some systems)
- Ensure no extra spaces in file names

### Step 4: Create Additional Pages (Optional)

You can create a `blog.html` page using the same template structure. Just replace the content section with your blog posts.

---

## Color Scheme Customization

The landing page uses two primary brand colors:

| Color | Hex Code | Used For | CSS |
|-------|----------|----------|-----|
| Primary Red | `#FF5A5F` | Headlines, accents, buttons | `style="color: #FF5A5F;"` |
| Secondary Yellow | `#FFD166` | Highlights, alternate accents | `style="color: #FFD166;"` |

### Changing the Brand Colors

**Step 1: Find all color instances**
1. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac)
2. Search for: `#FF5A5F`
3. Note how many instances appear (approximately 30+)

**Step 2: Choose your new colors**
- Visit [Color Picker](https://htmlcolorcodes.com/) to find hex codes
- Select your primary and secondary colors
- Note the hex codes (e.g., `#0066FF`)

**Step 3: Replace colors systematically**

**Option A: Replace All (Recommended)**
1. Use Find & Replace (usually `Ctrl+H` or `Cmd+H`)
2. Find: `#FF5A5F`
3. Replace with: Your new primary color hex code
4. Click "Replace All"
5. Repeat for `#FFD166` with your secondary color

**Option B: Manual replacement**
1. Find each instance
2. Replace one by one to ensure consistency

### Example: Change to Blue and Orange Theme

**Original:**
```html
<span style="color: #FF5A5F;">Executive Shuttle</span>
```

**Changed to Blue:**
```html
<span style="color: #0066FF;">Executive Shuttle</span>
```

**Original:**
```html
<span style="color: #FFD166;">VIP Transport</span>
```

**Changed to Orange:**
```html
<span style="color: #FF8C00;">VIP Transport</span>
```

### Color Recommendations

**Professional Blue Theme:**
- Primary: `#0066FF` (Blue)
- Secondary: `#00D4FF` (Cyan)

**Luxury Gold Theme:**
- Primary: `#1A1A1A` (Black)
- Secondary: `#D4AF37` (Gold)

**Modern Green Theme:**
- Primary: `#00AA44` (Green)
- Secondary: `#00FF88` (Bright Green)

### Changing Background Colors

**Current dark background:**
```html
<body class="bg-gray-900 text-white">
```

**To change to a different shade:**
- `bg-gray-800` = Slightly lighter
- `bg-gray-950` = Even darker
- `bg-black` = Pure black

**Example:**
```html
<body class="bg-gray-950 text-white">
```

---

## Troubleshooting Guide

### Common Issues and Solutions

#### Issue 1: Page Doesn't Look Right

**Symptoms:**
- Text is overlapping
- Colors look wrong
- Layout is broken

**Solutions:**
1. **Clear browser cache:**
   - Chrome: Press `Ctrl+Shift+Delete` (Windows) or `Cmd+Shift+Delete` (Mac)
   - Select "Cached images and files"
   - Click "Clear data"
   - Refresh the page

2. **Check for typos:**
   - Look for missing closing tags: `</div>`, `</section>`
   - Verify all quotes are matching: `"` with `"`
   - Check class names are spelled correctly

3. **Validate HTML:**
   - Visit [HTML Validator](https://validator.w3.org/)
   - Paste your HTML code
   - Fix any errors shown

#### Issue 2: Links Not Working

**Symptoms:**
- Clicking a link does nothing
- Link opens wrong page
- Navigation doesn't scroll to section

**Solutions:**
1. **Check href attribute:**
   ```html
   <!-- Wrong -->
   <a href="features">Link</a>
   
   <!-- Correct -->
   <a href="#features">Link</a>
   ```

2. **Verify section IDs exist:**
   - Search for `id="features"` in the HTML
   - If not found, add it: `<section id="features">`

3. **Check file paths:**
   - For external files: `href="privacy.html"` (same folder)
   - For external URLs: `href="https://example.com"`
   - For email: `href="mailto:email@example.com"`

4. **Test in different browser:**
   - Try Chrome, Firefox, or Safari
   - Some browsers handle links differently

#### Issue 3: Mobile Menu Not Working

**Symptoms:**
- Mobile menu button doesn't open/close
- Menu items don't respond to clicks
- Menu stays hidden

**Solutions:**
1. **Check JavaScript:**
   - Ensure JavaScript section is not deleted (lines 728-770)
   - Verify no syntax errors in the code

2. **Verify HTML structure:**
   ```html
   <!-- Check these exist -->
   <button class="mobile-menu-button md:hidden">
   <div class="mobile-menu hidden">
   ```

3. **Clear cache and refresh:**
   - Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)

#### Issue 4: Styling Not Applied

**Symptoms:**
- Tailwind classes don't work
- Colors don't appear
- Spacing is wrong

**Solutions:**
1. **Verify Tailwind CSS CDN:**
   - Check line 28: `<script src="https://cdn.tailwindcss.com"></script>`
   - Ensure this line is present and not deleted

2. **Check class syntax:**
   ```html
   <!-- Correct -->
   <div class="p-8 mb-4 text-white">
   
   <!-- Wrong -->
   <div class="p-8, mb-4, text-white">
   ```

3. **Verify responsive classes:**
   ```html
   <!-- Correct -->
   <div class="text-2xl md:text-4xl lg:text-6xl">
   
   <!-- Wrong -->
   <div class="text-2xl md text-4xl lg text-6xl">
   ```

#### Issue 5: Images Not Showing

**Symptoms:**
- Background images don't appear
- Icons are missing
- Hero section looks empty

**Solutions:**
1. **Check image URL:**
   ```html
   <!-- External image -->
   <img src="https://images.unsplash.com/photo-...?w=1200" alt="Description">
   ```

2. **Verify Font Awesome icons:**
   - Check line 31: Font Awesome CSS is loaded
   - Use correct icon names: `fa-shuttle-van`, `fa-star`, etc.

3. **Test image URL:**
   - Copy the image URL into browser address bar
   - If it doesn't load, the URL is broken

#### Issue 6: FAQ Accordion Not Working

**Symptoms:**
- Clicking FAQ questions does nothing
- Answers don't appear/disappear
- Icons don't rotate

**Solutions:**
1. **Check JavaScript:**
   - Ensure FAQ JavaScript code is present (lines 757-770)
   - Look for: `const faqItems = document.querySelectorAll('.faq-item');`

2. **Verify HTML structure:**
   - Each FAQ item must have correct classes:
   ```html
   <div class="faq-item">
       <div class="faq-question">
           <h3>Question</h3>
           <i class="faq-icon"></i>
       </div>
       <div class="faq-answer hidden">
           <p>Answer</p>
       </div>
   </div>
   ```

3. **Clear cache and refresh:**
   - Hard refresh: `Ctrl+Shift+R`

#### Issue 7: Form Not Submitting

**Symptoms:**
- Contact form doesn't send
- No confirmation message
- No error message

**Solutions:**
1. **Check Web3Forms API key:**
   - Line 598: `<input type="hidden" name="access_key" value="3bb39263-2490-491b-89f8-213fa513edae">`
   - This is a demo key - you need your own
   - Visit [Web3Forms](https://web3forms.com/) to get your key
   - Replace the value with your API key

2. **Verify form HTML:**
   ```html
   <!-- Must have these attributes -->
   <form action="https://api.web3forms.com/submit" method="POST">
       <input type="hidden" name="access_key" value="YOUR_KEY">
   </form>
   ```

3. **Test form fields:**
   - Ensure all required fields have `required` attribute
   - Check field names match: `name="name"`, `name="email"`, `name="message"`

#### Issue 8: Responsive Design Broken

**Symptoms:**
- Page looks bad on mobile
- Text is too large or too small
- Elements overlap on tablets

**Solutions:**
1. **Test responsive design:**
   - Right-click > "Inspect" or press `F12`
   - Click device toggle icon (top-left of inspector)
   - Test different screen sizes

2. **Check viewport meta tag:**
   - Line 4: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
   - This must be present

3. **Verify responsive classes:**
   ```html
   <!-- Correct responsive design -->
   <div class="text-2xl md:text-4xl lg:text-6xl p-4 md:p-8 lg:p-16">
   
   <!-- Responsive grid -->
   <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
   ```

### Getting Help

**If you still have issues:**

1. **Check browser console for errors:**
   - Press `F12` to open Developer Tools
   - Click "Console" tab
   - Look for red error messages
   - Screenshot the error

2. **Validate your code:**
   - Visit [W3C Validator](https://validator.w3.org/)
   - Paste your HTML
   - Fix any errors shown

3. **Common error messages:**
   - "Cannot read property of null" - HTML element not found
   - "Unexpected token" - Syntax error in code
   - "404 Not Found" - File or URL doesn't exist

---

## Quick Reference Checklist

### Before Publishing

- [ ] All text content updated
- [ ] Company name changed throughout
- [ ] Booking URL updated in all locations
- [ ] Email address updated
- [ ] Phone number added (if applicable)
- [ ] Privacy policy page created and linked
- [ ] Terms of service page created and linked
- [ ] All links tested and working
- [ ] Mobile menu tested
- [ ] FAQ accordion tested
- [ ] Contact form tested
- [ ] Colors customized to brand
- [ ] Images and icons displaying correctly
- [ ] Page responsive on mobile, tablet, desktop
- [ ] No broken links or 404 errors
- [ ] Browser cache cleared and tested

### File Structure

```
Your Project Folder/
├── index.html          ✓ Main landing page
├── privacy.html        ✓ Privacy policy
├── terms.html          ✓ Terms of service
└── blog.html           (Optional)
```

### Key Sections to Update

| Section | Lines | What to Change |
|---------|-------|-----------------|
| Company Name | 58, 672, 724 | Replace "Pogiso's Tours" |
| Hero Headline | 123-130 | Main title and subtitle |
| Features | 189-220 | Icons, titles, descriptions |
| Benefits | 245-284 | Icons, titles, descriptions |
| Testimonials | 340-395 | Names, quotes, titles |
| About Us | 408-440 | Company story and stats |
| FAQ | 475-540 | Questions and answers |
| Footer | 672-710 | Links and information |
| Booking URL | Multiple | Update to your booking page |
| Email | Multiple | Update to your email |

---

## Final Notes

This landing page is built with modern, maintainable code. By following this guide, you can:

✅ Update all text content easily  
✅ Modify colors and styling without breaking the design  
✅ Add new sections and pages  
✅ Fix broken links and issues  
✅ Maintain mobile responsiveness  
✅ Customize to your brand  

**Remember:**
- Always back up your files before making major changes
- Test changes in a browser before publishing
- Use Find & Replace carefully - preview changes first
- Keep file names consistent (case-sensitive on some systems)
- Validate your HTML regularly

For questions or issues, refer to the **Troubleshooting Guide** section above.

Good luck with your Pogiso's Tours website! 🚀