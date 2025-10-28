# FiberNet Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, customizing, and managing your fiber optic internet landing page.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Styles with Tailwind CSS](#modifying-styles-with-tailwind-css)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Mobile Responsiveness](#mobile-responsiveness)
8. [Troubleshooting](#troubleshooting)
9. [Best Practices](#best-practices)

---

## Getting Started

### What You'll Need

- A text editor (Notepad++, Visual Studio Code, or Sublime Text recommended)
- Basic understanding of HTML tags and structure
- A web browser for testing changes
- An FTP client or web hosting dashboard to upload files (if hosting online)

### Opening Your File

1. **Right-click** on your `index.html` file
2. Select **"Open With"** → Choose your text editor
3. The entire page code will appear in the editor
4. Make changes and save with **Ctrl+S** (Windows) or **Cmd+S** (Mac)

### Testing Your Changes

After making updates:
1. Save your file
2. Open the `index.html` file in your web browser
3. Refresh the page with **F5** or **Ctrl+R**
4. Check that your changes appear correctly

---

## Understanding the Page Structure

Your landing page is organized into distinct sections. Here's what each section contains:

### Header & Navigation (Lines 26-58)
- **Logo and branding** ("FiberNet")
- **Desktop navigation menu** (Features, Benefits, FAQ, Testimonials)
- **Mobile menu** (hidden on small screens, appears on phones/tablets)
- **Call Now button** with phone number

### Hero Section (Lines 60-86)
- **Main headline** with gradient text
- **Subheading** describing the service
- **Two call-to-action buttons** (Call and Email)
- **Decorative background elements**

### Features Section (Lines 88-188)
- **Section title** and description
- **Six feature cards** in a grid layout
- Each card includes an icon, title, description, and bullet points

### Benefits Section (Lines 190-265)
- **Section title**
- **Four benefit items** with icons
- **Statistics display** (download speeds, uptime, satisfaction)
- **Feature image**

### CTA Section (Lines 267-294)
- **Call-to-action** with background image
- **Headline and description**
- **Action buttons**

### Testimonials Section (Lines 296-370)
- **Section title**
- **Four customer testimonials** with star ratings
- **Customer names and titles**

### About Us Section (Lines 372-426)
- **Company story and mission**
- **Company statistics**
- **Company image**

### FAQ Section (Lines 428-532)
- **Five accordion-style questions and answers**
- **Expandable/collapsible answers**

### Footer (Lines 578-641)
- **Company information**
- **Quick links**
- **Support information**
- **Legal links**
- **Social media icons**
- **Copyright information**

---

## Updating Text Content

### Important: How to Edit Text Without Breaking the Page

When editing text, **never delete the HTML tags** (the words in angle brackets like `<h1>`, `<p>`, `</div>`). Only change the actual words between the opening and closing tags.

**Example:**
```html
<!-- WRONG - This breaks the page -->
<h1>FiberNet</h1>
becomes:
<h1>MyInternet</h1> ✓ CORRECT

<!-- WRONG - Don't delete the tags -->
MyInternet
✗ INCORRECT
```

### Updating the Company Name

Your company name appears in multiple places. Here's how to update it:

#### 1. Header Logo (Line 35)
**Find this code:**
```html
<span class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">FiberNet</span>
```

**Change to:**
```html
<span class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">Your Company Name</span>
```

#### 2. About Section Title (Line 373)
**Find this code:**
```html
<h2 class="text-4xl md:text-5xl font-bold mb-4 tracking-tight">
    About <span class="bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">FiberNet</span>
</h2>
```

**Change to:**
```html
<h2 class="text-4xl md:text-5xl font-bold mb-4 tracking-tight">
    About <span class="bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">Your Company Name</span>
</h2>
```

#### 3. Footer Logo (Line 598)
**Find this code:**
```html
<span class="text-xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">FiberNet</span>
```

**Change to:**
```html
<span class="text-xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">Your Company Name</span>
```

#### 4. Footer Copyright (Line 634)
**Find this code:**
```html
&copy; 2025 FiberNet. All rights reserved. | Delivering premium fiber optic internet across the USA
```

**Change to:**
```html
&copy; 2025 Your Company Name. All rights reserved. | Delivering premium fiber optic internet across the USA
```

### Updating Contact Information

#### Phone Number
Your phone number is used in multiple locations. Search for `8886322232` and replace with your actual phone number.

**Locations to update:**
- Line 46: Header "Call Now" button
- Line 77: Hero section call button
- Line 294: CTA section call button
- Line 542: Final CTA call button
- Line 610: Footer phone link

**Example - Header Call Button (Line 46):**
```html
<!-- BEFORE -->
<a href="tel:8886322232" class="bg-gradient-to-r from-blue-500 to-cyan-500 px-6 py-2 rounded-lg font-semibold button-primary hover:shadow-lg text-white">Call Now</a>

<!-- AFTER -->
<a href="tel:5551234567" class="bg-gradient-to-r from-blue-500 to-cyan-500 px-6 py-2 rounded-lg font-semibold button-primary hover:shadow-lg text-white">Call Now</a>
```

#### Email Address
Your email is used in the footer and CTA sections. Search for `info@bestinternetandtv.com` and replace with your actual email.

**Locations to update:**
- Line 79: Hero section email button
- Line 296: CTA section email button
- Line 544: Final CTA email button
- Line 611: Footer email link

**Example - Hero Section Email (Line 79):**
```html
<!-- BEFORE -->
<a href="mailto:info@bestinternetandtv.com" class="border-2 border-cyan-500 px-8 py-4 rounded-lg font-bold text-lg hover:bg-cyan-500 hover:text-gray-900 transition-all duration-300 inline-flex items-center gap-2">
    <i class="fas fa-envelope"></i> Get More Info
</a>

<!-- AFTER -->
<a href="mailto:your-email@yourcompany.com" class="border-2 border-cyan-500 px-8 py-4 rounded-lg font-bold text-lg hover:bg-cyan-500 hover:text-gray-900 transition-all duration-300 inline-flex items-center gap-2">
    <i class="fas fa-envelope"></i> Get More Info
</a>
```

### Updating Hero Section Text

The hero section is the first thing visitors see. Here's how to customize it:

#### Main Headline (Line 67)
**Find this code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight tracking-tight">
    <span class="bg-gradient-to-r from-blue-400 via-cyan-400 to-blue-400 bg-clip-text text-transparent">Fiber Optic Internet</span>
</h1>
```

**Change to:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight tracking-tight">
    <span class="bg-gradient-to-r from-blue-400 via-cyan-400 to-blue-400 bg-clip-text text-transparent">Your Headline Here</span>
</h1>
```

#### Hero Subheading (Line 70)
**Find this code:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 leading-relaxed max-w-3xl mx-auto">
    Experience the best internet plans in the USA with lightning-fast fiber optic connectivity, no contracts, and unbeatable reliability
</p>
```

**Change to:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 leading-relaxed max-w-3xl mx-auto">
    Your description text goes here
</p>
```

### Updating Feature Cards

The features section contains six cards. Each card follows the same structure:

#### Feature 1: Lightning-Fast Speeds (Lines 99-116)

**Find this section:**
```html
<!-- Feature 1: Lightning-Fast Speeds -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">
    <div class="bg-gradient-to-br from-blue-500 to-cyan-500 w-16 h-16 rounded-lg flex items-center justify-center mb-6 group-hover:shadow-lg group-hover:shadow-cyan-500/50 transition-all duration-300">
        <i class="fas fa-bolt text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Lightning-Fast Speeds</h3>
    <p class="text-gray-400 leading-relaxed mb-4">
        Experience download speeds up to 1 Gigabit per second...
    </p>
    <ul class="space-y-2 text-sm text-gray-300">
        <li class="flex items-center gap-2"><i class="fas fa-check text-cyan-400"></i> Up to 1 Gbps download speeds</li>
        <li class="flex items-center gap-2"><i class="fas fa-check text-cyan-400"></i> Consistent upload speeds</li>
        <li class="flex items-center gap-2"><i class="fas fa-check text-cyan-400"></i> Zero throttling guarantee</li>
    </ul>
</div>
```

**To customize:**

1. **Change the title:** Replace `Lightning-Fast Speeds` with your feature title
2. **Change the description:** Replace the paragraph text with your description
3. **Update bullet points:** Replace each `<li>` item with your features
4. **Change the icon:** Replace `fa-bolt` with another Font Awesome icon (see icon list below)

**Example:**
```html
<!-- Feature 1: Custom Feature -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">
    <div class="bg-gradient-to-br from-blue-500 to-cyan-500 w-16 h-16 rounded-lg flex items-center justify-center mb-6 group-hover:shadow-lg group-hover:shadow-cyan-500/50 transition-all duration-300">
        <i class="fas fa-rocket text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Super Fast Performance</h3>
    <p class="text-gray-400 leading-relaxed mb-4">
        Our service delivers incredible speed for all your needs.
    </p>
    <ul class="space-y-2 text-sm text-gray-300">
        <li class="flex items-center gap-2"><i class="fas fa-check text-cyan-400"></i> Fast downloads</li>
        <li class="flex items-center gap-2"><i class="fas fa-check text-cyan-400"></i> Quick uploads</li>
        <li class="flex items-center gap-2"><i class="fas fa-check text-cyan-400"></i> No delays</li>
    </ul>
</div>
```

#### Popular Font Awesome Icons

Replace `fa-bolt` with any of these icons:

| Icon Class | Icon Name | Use Case |
|-----------|-----------|----------|
| `fa-bolt` | Lightning bolt | Speed, power |
| `fa-file-contract` | Contract | Agreements, terms |
| `fa-shield-alt` | Shield | Security, protection |
| `fa-headset` | Headset | Support, customer service |
| `fa-tools` | Tools | Installation, setup |
| `fa-dollar-sign` | Dollar sign | Pricing, money |
| `fa-wifi` | WiFi | Internet, connectivity |
| `fa-rocket` | Rocket | Launch, speed |
| `fa-star` | Star | Quality, rating |
| `fa-check-circle` | Check mark | Verified, complete |
| `fa-globe` | Globe | World, international |
| `fa-lock` | Lock | Security, privacy |
| `fa-phone` | Phone | Call, contact |
| `fa-envelope` | Email | Message, contact |
| `fa-cloud` | Cloud | Cloud services |
| `fa-server` | Server | Infrastructure |

### Updating Testimonials

Each testimonial card can be customized. Here's the first testimonial (Lines 319-337):

**Find this code:**
```html
<!-- Testimonial 1 -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 hover:shadow-xl">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-300 mb-6 leading-relaxed">
        "Finally ditched my old cable internet! The speed difference is night and day..."
    </p>
    <div class="flex items-center gap-3">
        <div class="w-12 h-12 bg-gradient-to-br from-blue-500 to-cyan-500 rounded-full flex items-center justify-center">
            <i class="fas fa-user text-white"></i>
        </div>
        <div>
            <p class="font-bold text-white">Sarah Mitchell</p>
            <p class="text-sm text-gray-400">Remote Software Developer</p>
        </div>
    </div>
</div>
```

**To customize:**

1. **Change the quote:** Replace the text between the quotation marks
2. **Change the name:** Replace `Sarah Mitchell`
3. **Change the title:** Replace `Remote Software Developer`
4. **Adjust stars:** Remove or add `<i class="fas fa-star text-yellow-400"></i>` lines for different ratings

**Example:**
```html
<!-- Testimonial 1 -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 hover:shadow-xl">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-300 mb-6 leading-relaxed">
        "This service changed my life! I can finally work from home without connection issues."
    </p>
    <div class="flex items-center gap-3">
        <div class="w-12 h-12 bg-gradient-to-br from-blue-500 to-cyan-500 rounded-full flex items-center justify-center">
            <i class="fas fa-user text-white"></i>
        </div>
        <div>
            <p class="font-bold text-white">John Smith</p>
            <p class="text-sm text-gray-400">Business Owner</p>
        </div>
    </div>
</div>
```

### Updating FAQ Questions and Answers

Each FAQ item contains a question and answer. Here's the first one (Lines 441-456):

**Find this code:**
```html
<!-- FAQ Item 1 -->
<div class="faq-item bg-gray-900 border border-gray-700 rounded-lg overflow-hidden hover:border-cyan-500 transition-all duration-300">
    <button class="faq-question w-full px-6 py-4 flex items-center justify-between hover:bg-gray-800 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-semibold text-left">What internet speeds will I get with fiber optic service?</span>
        <i class="fas fa-chevron-down faq-icon text-cyan-400"></i>
    </button>
    <div class="faq-answer hidden px-6 py-4 border-t border-gray-700 bg-gray-800 bg-opacity-50">
        <p class="text-gray-300 leading-relaxed">
            Our fiber optic internet plans offer download speeds ranging from 300 Mbps...
        </p>
    </div>
</div>
```

**To customize:**

1. **Change the question:** Replace the text in the `<span class="text-lg font-semibold text-left">` tag
2. **Change the answer:** Replace the text in the `<p class="text-gray-300 leading-relaxed">` tag

**Example:**
```html
<!-- FAQ Item 1 -->
<div class="faq-item bg-gray-900 border border-gray-700 rounded-lg overflow-hidden hover:border-cyan-500 transition-all duration-300">
    <button class="faq-question w-full px-6 py-4 flex items-center justify-between hover:bg-gray-800 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-semibold text-left">How fast is your internet?</span>
        <i class="fas fa-chevron-down faq-icon text-cyan-400"></i>
    </button>
    <div class="faq-answer hidden px-6 py-4 border-t border-gray-700 bg-gray-800 bg-opacity-50">
        <p class="text-gray-300 leading-relaxed">
            Our internet speeds are incredibly fast, reaching up to 1 Gbps for most customers.
        </p>
    </div>
</div>
```

---

## Modifying Styles with Tailwind CSS

### Understanding Tailwind CSS Classes

This landing page uses **Tailwind CSS**, a utility-first CSS framework. Instead of writing custom CSS, you add pre-made classes to HTML elements.

**How Tailwind Classes Work:**

```html
<!-- Example: A button with Tailwind classes -->
<button class="bg-blue-500 text-white px-6 py-2 rounded-lg hover:bg-blue-600">
    Click Me
</button>
```

Breaking down the classes:
- `bg-blue-500` = Blue background color
- `text-white` = White text color
- `px-6` = Horizontal padding (left and right)
- `py-2` = Vertical padding (top and bottom)
- `rounded-lg` = Rounded corners (large)
- `hover:bg-blue-600` = Darker blue on mouse hover

### Common Tailwind Classes Used in This Page

#### Colors

| Class | Effect |
|-------|--------|
| `bg-gray-900` | Dark gray background |
| `bg-gray-800` | Slightly lighter gray background |
| `text-white` | White text |
| `text-gray-300` | Light gray text |
| `text-gray-400` | Medium gray text |
| `bg-blue-500` | Blue background |
| `bg-cyan-500` | Cyan background |
| `hover:bg-blue-500` | Blue background on hover |

#### Spacing

| Class | Effect |
|-------|--------|
| `p-4` | Padding on all sides (small) |
| `p-8` | Padding on all sides (large) |
| `px-6` | Horizontal padding |
| `py-4` | Vertical padding |
| `mb-4` | Margin below element |
| `mt-6` | Margin above element |
| `gap-4` | Space between flex items |

#### Layout

| Class | Effect |
|-------|--------|
| `flex` | Display as flexbox |
| `grid` | Display as grid |
| `grid-cols-1` | Single column grid |
| `md:grid-cols-2` | Two columns on medium screens |
| `lg:grid-cols-3` | Three columns on large screens |
| `justify-center` | Center items horizontally |
| `items-center` | Center items vertically |

#### Sizing

| Class | Effect |
|-------|--------|
| `w-full` | 100% width |
| `h-12` | Fixed height |
| `rounded-lg` | Rounded corners (large) |
| `rounded-xl` | Rounded corners (extra large) |

### Changing Colors

#### Hero Section Background

The hero section uses a gradient background. To change it:

**Find this code (Line 60):**
```html
<section class="hero-gradient py-24 md:py-32 lg:py-40 relative overflow-hidden">
```

The `hero-gradient` class is defined in the `<style>` tag (Line 16):
```css
.hero-gradient {
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
}
```

**To change the gradient colors:**

1. Find the `<style>` section near the top (Lines 14-24)
2. Locate `.hero-gradient`
3. Change the hex color codes:

```css
/* Current colors: dark blue to navy */
.hero-gradient {
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
}

/* Change to purple to pink */
.hero-gradient {
    background: linear-gradient(135deg, #2d1b4e 0%, #5a2e7d 100%);
}

/* Change to dark green to teal */
.hero-gradient {
    background: linear-gradient(135deg, #1a3a3a 0%, #0d5d5d 100%);
}
```

**Common Hex Colors:**
- Dark Blue: `#1a1a2e`
- Navy: `#16213e`
- Purple: `#2d1b4e`
- Dark Green: `#1a3a3a`
- Dark Red: `#3a1a1a`
- Black: `#000000`

#### Button Colors

**Find the primary button (Line 46):**
```html
<a href="tel:8886322232" class="bg-gradient-to-r from-blue-500 to-cyan-500 px-6 py-2 rounded-lg font-semibold button-primary hover:shadow-lg text-white">Call Now</a>
```

**To change button colors, modify these classes:**
- `from-blue-500` = Starting color
- `to-cyan-500` = Ending color

**Replace with:**
```html
<!-- Purple to pink gradient -->
<a href="tel:8886322232" class="bg-gradient-to-r from-purple-500 to-pink-500 px-6 py-2 rounded-lg font-semibold button-primary hover:shadow-lg text-white">Call Now</a>

<!-- Green to teal gradient -->
<a href="tel:8886322232" class="bg-gradient-to-r from-green-500 to-teal-500 px-6 py-2 rounded-lg font-semibold button-primary hover:shadow-lg text-white">Call Now</a>

<!-- Red to orange gradient -->
<a href="tel:8886322232" class="bg-gradient-to-r from-red-500 to-orange-500 px-6 py-2 rounded-lg font-semibold button-primary hover:shadow-lg text-white">Call Now</a>
```

**Available Tailwind Colors:**
- Blue: `blue-500`
- Cyan: `cyan-500`
- Purple: `purple-500`
- Pink: `pink-500`
- Green: `green-500`
- Teal: `teal-500`
- Red: `red-500`
- Orange: `orange-500`
- Yellow: `yellow-500`
- Indigo: `indigo-500`

### Changing Text Sizes

#### Main Headline Size

**Find the hero headline (Line 67):**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight tracking-tight">
```

The classes control size:
- `text-4xl` = Extra large (mobile)
- `md:text-5xl` = Even larger (tablets)
- `lg:text-6xl` = Largest (desktops)

**To make the headline smaller:**
```html
<!-- Smaller sizes -->
<h1 class="text-2xl md:text-3xl lg:text-4xl font-bold mb-6 leading-tight tracking-tight">

<!-- Larger sizes -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-6 leading-tight tracking-tight">
```

**Text Size Scale:**
- `text-xs` = Extra small
- `text-sm` = Small
- `text-base` = Normal
- `text-lg` = Large
- `text-xl` = Extra large
- `text-2xl` = 2x
- `text-3xl` = 3x
- `text-4xl` = 4x
- `text-5xl` = 5x
- `text-6xl` = 6x
- `text-7xl` = 7x

### Changing Spacing and Padding

#### Feature Card Padding

**Find a feature card (Line 99):**
```html
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">
```

The `p-8` class adds padding. To adjust:

```html
<!-- Less padding -->
<div class="card-hover bg-gray-900 border border-gray-700 p-4 rounded-xl hover:border-cyan-500 group">

<!-- More padding -->
<div class="card-hover bg-gray-900 border border-gray-700 p-12 rounded-xl hover:border-cyan-500 group">
```

**Padding Values:**
- `p-2` = Small
- `p-4` = Medium
- `p-6` = Large
- `p-8` = Extra large
- `p-12` = Extra extra large

#### Section Spacing

**Find a section (Line 88):**
```html
<section id="features" class="py-24 bg-gray-800 bg-opacity-50 backdrop-blur-sm">
```

The `py-24` adds vertical padding. To adjust:

```html
<!-- Less vertical spacing -->
<section id="features" class="py-12 bg-gray-800 bg-opacity-50 backdrop-blur-sm">

<!-- More vertical spacing -->
<section id="features" class="py-32 bg-gray-800 bg-opacity-50 backdrop-blur-sm">
```

### Changing Border Styles

#### Feature Card Border

**Find a feature card (Line 99):**
```html
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">
```

**To remove the border:**
```html
<div class="card-hover bg-gray-900 p-8 rounded-xl hover:border-cyan-500 group">
```

**To change border color:**
```html
<!-- Blue border -->
<div class="card-hover bg-gray-900 border border-blue-500 p-8 rounded-xl hover:border-cyan-500 group">

<!-- Red border -->
<div class="card-hover bg-gray-900 border border-red-500 p-8 rounded-xl hover:border-cyan-500 group">
```

**To change border thickness:**
```html
<!-- Thicker border -->
<div class="card-hover bg-gray-900 border-2 border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">

<!-- Very thick border -->
<div class="card-hover bg-gray-900 border-4 border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">
```

### Changing Rounded Corners

**Find an element with rounded corners (Line 99):**
```html
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-xl hover:border-cyan-500 group">
```

**To adjust corner radius:**
```html
<!-- No rounded corners -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 hover:border-cyan-500 group">

<!-- Slightly rounded -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded hover:border-cyan-500 group">

<!-- Medium rounded -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-lg hover:border-cyan-500 group">

<!-- Very rounded (almost circle for small elements) -->
<div class="card-hover bg-gray-900 border border-gray-700 p-8 rounded-full hover:border-cyan-500 group">
```

### Changing Opacity (Transparency)

**Find an element with opacity (Line 62):**
```html
<div class="absolute inset-0 opacity-10">
```

The `opacity-10` makes the element 10% visible (90% transparent).

**To adjust transparency:**
```html
<!-- More transparent (less visible) -->
<div class="absolute inset-0 opacity-5">

<!-- Slightly transparent -->
<div class="absolute inset-0 opacity-20">

<!-- More opaque (more visible) -->
<div class="absolute inset-0 opacity-50">

<!-- Fully opaque (completely visible) -->
<div class="absolute inset-0 opacity-100">
```

---

## Fixing and Managing Links

### Understanding HTML Links

A link in HTML has this structure:
```html
<a href="destination">Link Text</a>
```

- `<a>` = Anchor tag (creates the link)
- `href="destination"` = Where the link goes
- `Link Text` = What users see and click on

### Types of Links on Your Page

#### 1. **Internal Navigation Links** (Same page, different section)
These links jump to sections on the same page using `#section-id`

**Example:**
```html
<a href="#features">Features</a>
```

This links to an element with `id="features"`:
```html
<section id="features" class="py-24 bg-gray-800 bg-opacity-50 backdrop-blur-sm">
```

#### 2. **Phone Links** (Calls when clicked on mobile)
These use the `tel:` protocol

**Example:**
```html
<a href="tel:8886322232">Call Now</a>
```

#### 3. **Email Links** (Opens email client)
These use the `mailto:` protocol

**Example:**
```html
<a href="mailto:info@bestinternetandtv.com">Email Us</a>
```

#### 4. **External Links** (Goes to another website)
These use the full URL starting with `http://` or `https://`

**Example:**
```html
<a href="https://www.example.com">Visit Example</a>
```

#### 5. **Internal Page Links** (Goes to another page on your website)
These use relative paths

**Example:**
```html
<a href="privacy.html">Privacy Policy</a>
```

### Finding All Links on Your Page

Use your text editor's **Find** function (**Ctrl+F** on Windows, **Cmd+F** on Mac) to search for `href=` to find all links.

### Current Links on Your Page

Here's a complete list of all links and where to find them:

#### Navigation Menu Links (Lines 40-44)
```html
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#faq" class="...">FAQ</a>
<a href="#testimonials" class="...">Testimonials</a>
```

**Status:** ✓ These are correct and link to sections on the page

#### Mobile Menu Links (Lines 48-52)
```html
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#faq" class="...">FAQ</a>
<a href="#testimonials" class="...">Testimonials</a>
```

**Status:** ✓ These are correct and link to sections on the page

#### Call Now Buttons
Located at:
- Line 46 (Header)
- Line 77 (Hero section)
- Line 294 (CTA section)
- Line 542 (Final CTA)

```html
<a href="tel:8886322232" class="...">Call Now</a>
```

**Status:** ⚠️ Update `8886322232` with your actual phone number

#### Email Links
Located at:
- Line 79 (Hero section)
- Line 296 (CTA section)
- Line 544 (Final CTA)

```html
<a href="mailto:info@bestinternetandtv.com" class="...">Email Us</a>
```

**Status:** ⚠️ Update `info@bestinternetandtv.com` with your actual email

#### Footer Links (Lines 605-622)

**Quick Links:**
```html
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#testimonials" class="...">Testimonials</a>
<a href="#faq" class="...">FAQ</a>
```

**Status:** ✓ These are correct

**Support Links:**
```html
<a href="tel:8886322232" class="...">Call: 1-888-632-2232</a>
<a href="mailto:info@bestinternetandtv.com" class="...">Email: info@bestinternetandtv.com</a>
<a href="#" class="...">Live Chat</a>
<a href="#" class="...">Contact Us</a>
```

**Status:** ⚠️ Update phone and email, and replace `#` with actual links

**Legal Links:**
```html
<a href="privacy.html" class="...">Privacy Policy</a>
<a href="terms.html" class="...">Terms of Service</a>
<a href="blog.html" class="...">Blog</a>
<a href="#" class="...">Sitemap</a>
```

**Status:** ⚠️ These need to be updated or created

#### Social Media Links (Lines 615-627)
```html
<a href="#" class="...">Facebook</a>
<a href="#" class="...">Twitter</a>
<a href="#" class="...">LinkedIn</a>
<a href="#" class="...">Instagram</a>
```

**Status:** ⚠️ Replace `#` with actual social media URLs

### Updating Links: Step-by-Step

#### Step 1: Update Your Phone Number

1. Use **Find & Replace** (Ctrl+H or Cmd+H)
2. Find: `8886322232`
3. Replace with: `5551234567` (your number)
4. Click **Replace All**

**Or manually:**
1. Find each instance of `tel:8886322232`
2. Change to `tel:5551234567`

#### Step 2: Update Your Email

1. Use **Find & Replace**
2. Find: `info@bestinternetandtv.com`
3. Replace with: `your-email@yourcompany.com`
4. Click **Replace All**

#### Step 3: Update Social Media Links

**Find the social media section (Lines 615-627):**
```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook text-white"></i>
</a>
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="Twitter">
    <i class="fab fa-twitter text-white"></i>
</a>
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="LinkedIn">
    <i class="fab fa-linkedin text-white"></i>
</a>
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="Instagram">
    <i class="fab fa-instagram text-white"></i>
</a>
```

**Replace with your actual URLs:**
```html
<a href="https://www.facebook.com/yourpage" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook text-white"></i>
</a>
<a href="https://www.twitter.com/yourhandle" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="Twitter">
    <i class="fab fa-twitter text-white"></i>
</a>
<a href="https://www.linkedin.com/company/yourcompany" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="LinkedIn">
    <i class="fab fa-linkedin text-white"></i>
</a>
<a href="https://www.instagram.com/yourprofile" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-500 transition-colors duration-300" aria-label="Instagram">
    <i class="fab fa-instagram text-white"></i>
</a>
```

#### Step 4: Update Footer Support Links

**Find the support section (Lines 618-622):**
```html
<li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Live Chat</a></li>
<li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Contact Us</a></li>
```

**Replace with:**
```html
<li><a href="https://chat.example.com" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Live Chat</a></li>
<li><a href="contact.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Contact Us</a></li>
```

#### Step 5: Update Sitemap Link

**Find (Line 626):**
```html
<li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Sitemap</a></li>
```

**Replace with:**
```html
<li><a href="sitemap.xml" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Sitemap</a></li>
```

### Troubleshooting Link Issues

#### Problem: Link doesn't work
**Solution:**
1. Check the `href` value is spelled correctly
2. Make sure the file exists (for internal links like `privacy.html`)
3. Check for typos in phone numbers (should be all digits)
4. Check email format (should have `@` and domain)

#### Problem: Phone link doesn't call on mobile
**Solution:**
Make sure the link uses `tel:` protocol:
```html
<!-- Wrong -->
<a href="8886322232">Call</a>

<!-- Correct -->
<a href="tel:8886322232">Call</a>
```

#### Problem: Email link doesn't open email client
**Solution:**
Make sure the link uses `mailto:` protocol:
```html
<!-- Wrong -->
<a href="info@example.com">Email</a>

<!-- Correct -->
<a href="mailto:info@example.com">Email</a>
```

---

## Adding Privacy and Terms Pages

### Understanding What You Need

You need to create two new HTML files:
1. `privacy.html` - Your privacy policy page
2. `terms.html` - Your terms of service page

### Step 1: Create the Privacy Policy Page

1. **Create a new file:**
   - In your text editor, go to **File** → **New**
   - A blank document appears

2. **Add this basic HTML structure:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for FiberNet - Learn how we protect your data">
    <title>Privacy Policy | FiberNet</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800 shadow-lg">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
            <div class="flex justify-between items-center">
                <!-- Logo -->
                <div class="flex items-center gap-2">
                    <div class="bg-gradient-to-r from-blue-500 to-cyan-500 p-2 rounded-lg">
                        <i class="fas fa-wifi text-white text-xl"></i>
                    </div>
                    <a href="index.html" class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">FiberNet</a>
                </div>

                <!-- Navigation -->
                <div class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Home</a>
                    <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Features</a>
                    <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
                </div>

                <!-- Mobile Menu Button -->
                <button class="md:hidden p-2 rounded-lg hover:bg-gray-800 transition-colors duration-300" aria-label="Toggle menu">
                    <i class="fas fa-bars text-xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold mb-8">Privacy Policy</h1>
            
            <div class="prose prose-invert max-w-none space-y-8">
                <div>
                    <h2 class="text-2xl font-bold mb-4">Introduction</h2>
                    <p class="text-gray-300 leading-relaxed">
                        At FiberNet, we are committed to protecting your privacy and ensuring you have a positive experience on our website and when using our services. This Privacy Policy explains how we collect, use, disclose, and otherwise handle your information.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">Information We Collect</h2>
                    <p class="text-gray-300 leading-relaxed mb-4">
                        We may collect information about you in various ways, including:
                    </p>
                    <ul class="list-disc list-inside text-gray-300 space-y-2">
                        <li>Information you provide directly (name, email, phone number)</li>
                        <li>Information collected automatically (IP address, browser type, pages visited)</li>
                        <li>Information from third parties (service providers, partners)</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">How We Use Your Information</h2>
                    <p class="text-gray-300 leading-relaxed mb-4">
                        We use the information we collect for various purposes:
                    </p>
                    <ul class="list-disc list-inside text-gray-300 space-y-2">
                        <li>To provide and improve our services</li>
                        <li>To communicate with you about your account</li>
                        <li>To send promotional emails and marketing materials</li>
                        <li>To analyze website usage and trends</li>
                        <li>To comply with legal obligations</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">Data Security</h2>
                    <p class="text-gray-300 leading-relaxed">
                        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet is 100% secure.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">Your Rights</h2>
                    <p class="text-gray-300 leading-relaxed mb-4">
                        You have the right to:
                    </p>
                    <ul class="list-disc list-inside text-gray-300 space-y-2">
                        <li>Access your personal information</li>
                        <li>Correct inaccurate data</li>
                        <li>Request deletion of your data</li>
                        <li>Opt-out of marketing communications</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">Contact Us</h2>
                    <p class="text-gray-300 leading-relaxed">
                        If you have questions about this Privacy Policy, please contact us at:
                    </p>
                    <p class="text-gray-300 mt-4">
                        Email: <a href="mailto:info@bestinternetandtv.com" class="text-cyan-400 hover:text-cyan-300">info@bestinternetandtv.com</a><br>
                        Phone: <a href="tel:8886322232" class="text-cyan-400 hover:text-cyan-300">1-888-632-2232</a>
                    </p>
                </div>

                <p class="text-gray-400 text-sm">
                    Last updated: January 2025
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; 2025 FiberNet. All rights reserved.
                </p>
                <div class="flex justify-center gap-6">
                    <a href="index.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Terms</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Mobile Menu Toggle (if needed)
            const mobileMenuButton = document.querySelector('header nav button');
            if (mobileMenuButton) {
                mobileMenuButton.addEventListener('click', () => {
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

3. **Save the file:**
   - Click **File** → **Save As**
   - Name it: `privacy.html`
   - Make sure it's in the same folder as `index.html`
   - Click **Save**

### Step 2: Create the Terms of Service Page

1. **Create another new file** (File → New)

2. **Add this HTML structure:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for FiberNet - Read our terms and conditions">
    <title>Terms of Service | FiberNet</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800 shadow-lg">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
            <div class="flex justify-between items-center">
                <!-- Logo -->
                <div class="flex items-center gap-2">
                    <div class="bg-gradient-to-r from-blue-500 to-cyan-500 p-2 rounded-lg">
                        <i class="fas fa-wifi text-white text-xl"></i>
                    </div>
                    <a href="index.html" class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">FiberNet</a>
                </div>

                <!-- Navigation -->
                <div class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Home</a>
                    <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Features</a>
                    <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
                </div>

                <!-- Mobile Menu Button -->
                <button class="md:hidden p-2 rounded-lg hover:bg-gray-800 transition-colors duration-300" aria-label="Toggle menu">
                    <i class="fas fa-bars text-xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold mb-8">Terms of Service</h1>
            
            <div class="prose prose-invert max-w-none space-y-8">
                <div>
                    <h2 class="text-2xl font-bold mb-4">1. Acceptance of Terms</h2>
                    <p class="text-gray-300 leading-relaxed">
                        By accessing and using this website and our services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">2. Use License</h2>
                    <p class="text-gray-300 leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on FiberNet's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside text-gray-300 space-y-2">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">3. Disclaimer</h2>
                    <p class="text-gray-300 leading-relaxed">
                        The materials on FiberNet's website are provided on an 'as is' basis. FiberNet makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">4. Limitations</h2>
                    <p class="text-gray-300 leading-relaxed">
                        In no event shall FiberNet or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on FiberNet's website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-300 leading-relaxed">
                        The materials appearing on FiberNet's website could include technical, typographical, or photographic errors. FiberNet does not warrant that any of the materials on its website are accurate, complete, or current. FiberNet may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">6. Links</h2>
                    <p class="text-gray-300 leading-relaxed">
                        FiberNet has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by FiberNet of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">7. Modifications</h2>
                    <p class="text-gray-300 leading-relaxed">
                        FiberNet may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">8. Governing Law</h2>
                    <p class="text-gray-300 leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold mb-4">Contact Information</h2>
                    <p class="text-gray-300 leading-relaxed">
                        If you have questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="text-gray-300 mt-4">
                        Email: <a href="mailto:info@bestinternetandtv.com" class="text-cyan-400 hover:text-cyan-300">info@bestinternetandtv.com</a><br>
                        Phone: <a href="tel:8886322232" class="text-cyan-400 hover:text-cyan-300">1-888-632-2232</a>
                    </p>
                </div>

                <p class="text-gray-400 text-sm">
                    Last updated: January 2025
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; 2025 FiberNet. All rights reserved.
                </p>
                <div class="flex justify-center gap-6">
                    <a href="index.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Terms</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Mobile Menu Toggle (if needed)
            const mobileMenuButton = document.querySelector('header nav button');
            if (mobileMenuButton) {
                mobileMenuButton.addEventListener('click', () => {
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

3. **Save the file:**
   - Click **File** → **Save As**
   - Name it: `terms.html`
   - Save in the same folder as `index.html`
   - Click **Save**

### Step 3: Update Links in index.html

Now you need to update the footer links in your main `index.html` file to point to these new pages.

#### Update Footer Legal Links (Line 623-625)

**Find this code:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Blog</a></li>
```

**This is already correct!** The links are already pointing to `privacy.html` and `terms.html`.

If you want to remove the Blog link (since you haven't created that page), change it to:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Terms of Service</a></li>
<li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors duration-300">Sitemap</a></li>
```

### Step 4: Verify All Files Are in the Same Folder

You should now have three files in the same folder:
1. `index.html` - Main landing page
2. `privacy.html` - Privacy policy
3. `terms.html` - Terms of service

**Folder structure:**
```
your-website-folder/
├── index.html
├── privacy.html
└── terms.html
```

### Step 5: Test the Links

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`
5. On those pages, click "Home" to return to the main page

### Important: Customize the Policy Content

The privacy and terms pages I provided are **templates**. You should:

1. **Replace placeholder text** with your actual policies
2. **Update company information** to match your business
3. **Consult a lawyer** to ensure your policies comply with laws in your jurisdiction
4. **Update contact information** to match your company details

### Resources for Creating Policies

- **TermsFeed** (termsfeed.com) - Generate privacy policies and terms
- **iubenda** (iubenda.com) - Privacy policy generator
- **Consult a lawyer** - For legal compliance in your area

---

## Mobile Responsiveness

### Understanding Responsive Design

Your landing page automatically adapts to different screen sizes (phones, tablets, desktops) using **Tailwind CSS responsive classes**.

### How Responsive Classes Work

Tailwind uses prefixes to apply styles at different screen sizes:

```html
<div class="text-2xl md:text-4xl lg:text-6xl">
    This text is:
    - 2xl size on mobile
    - 4xl size on tablets (md)
    - 6xl size on desktops (lg)
</div>
```

### Breakpoints

| Prefix | Screen Size | Devices |
|--------|------------|---------|
| (none) | < 640px | Mobile phones |
| `sm:` | ≥ 640px | Large phones |
| `md:` | ≥ 768px | Tablets |
| `lg:` | ≥ 1024px | Desktops |
| `xl:` | ≥ 1280px | Large desktops |
| `2xl:` | ≥ 1536px | Extra large desktops |

### Testing Mobile Responsiveness

#### In Your Browser

1. Open your page in Chrome, Firefox, or Safari
2. Press **F12** to open Developer Tools
3. Click the **phone/tablet icon** in the top-left
4. Choose a device to preview
5. Resize the window to see changes in real-time

#### Common Mobile Issues and Fixes

**Issue: Text is too small on mobile**

Find the text class and adjust:
```html
<!-- Before: Too small on mobile -->
<h1 class="text-4xl">Headline</h1>

<!-- After: Larger on mobile -->
<h1 class="text-2xl md:text-4xl">Headline</h1>
```

**Issue: Images are too wide on mobile**

The page already handles this with:
```html
<img src="..." class="w-full h-auto object-cover">
```

The `w-full` makes images fill their container, and `h-auto` maintains aspect ratio.

**Issue: Navigation menu is broken on mobile**

The mobile menu is already built in! It uses:
- `hidden md:flex` - Hidden on mobile, visible on tablets+
- `mobile-menu hidden md:hidden` - Visible on mobile, hidden on tablets+

### Making Custom Elements Responsive

If you add new content, use these patterns:

**Responsive Grid:**
```html
<!-- 1 column on mobile, 2 on tablets, 3 on desktops -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```

**Responsive Padding:**
```html
<!-- Small padding on mobile, large on desktops -->
<div class="px-4 md:px-8 lg:px-16 py-4 md:py-8 lg:py-16">
    Content
</div>
```

**Responsive Font Size:**
```html
<!-- Small text on mobile, large on desktops -->
<p class="text-sm md:text-base lg:text-lg">
    Paragraph text
</p>
```

**Hide on Mobile, Show on Desktop:**
```html
<!-- Hidden on mobile, visible on tablets+ -->
<div class="hidden md:block">
    Desktop only content
</div>
```

**Show on Mobile, Hide on Desktop:**
```html
<!-- Visible on mobile, hidden on tablets+ -->
<div class="md:hidden">
    Mobile only content
</div>
```

---

## Troubleshooting

### Common Issues and Solutions

#### Issue: Page doesn't look right after editing

**Solution:**
1. Make sure you saved the file (Ctrl+S)
2. Hard refresh your browser (Ctrl+Shift+R on Windows, Cmd+Shift+R on Mac)
3. Clear your browser cache
4. Try a different browser

#### Issue: Text is cut off or overlapping

**Solution:**
1. Check that you didn't delete any HTML tags
2. Make sure opening and closing tags match:
   ```html
   <p>Text</p>  ✓ Correct
   <p>Text</div> ✗ Wrong - mismatched tags
   ```
3. Use proper spacing and indentation

#### Issue: Links don't work

**Solution:**
1. Check the `href` value is correct
2. For email: `href="mailto:your-email@example.com"`
3. For phone: `href="tel:5551234567"`
4. For internal pages: `href="privacy.html"` (same folder)
5. For external sites: `href="https://example.com"`

#### Issue: Mobile menu doesn't work

**Solution:**
1. Check that the JavaScript is still in the page (Lines 553-573)
2. Make sure the `mobile-menu-button` and `mobile-menu` classes are present
3. Try refreshing the page

#### Issue: Colors don't change

**Solution:**
1. Make sure you're using valid Tailwind color names:
   ```html
   <!-- Correct -->
   <div class="bg-blue-500">

   <!-- Incorrect -->
   <div class="bg-myblue">
   ```
2. Check that you're using the right format:
   ```html
   <!-- Correct -->
   class="bg-blue-500"

   <!-- Incorrect -->
   class="background-color: blue"
   ```

#### Issue: Page looks different on different devices

**Solution:**
This is usually correct behavior! The page is responsive and adapts to screen size. Test on:
- Mobile phone
- Tablet
- Desktop

Use browser DevTools to preview different sizes.

#### Issue: Buttons don't look clickable

**Solution:**
Make sure buttons have the correct classes:
```html
<!-- Correct -->
<a href="..." class="bg-blue-500 px-6 py-2 rounded-lg hover:bg-blue-600">Button</a>

<!-- Missing hover effect -->
<a href="..." class="bg-blue-500 px-6 py-2 rounded-lg">Button</a>
```

#### Issue: Images don't load

**Solution:**
1. Check the image URL is correct
2. For external images (from Unsplash), make sure the URL starts with `https://`
3. For local images, make sure the file is in the same folder as `index.html`

Example:
```html
<!-- External image (works) -->
<img src="https://images.unsplash.com/photo-..." alt="Description">

<!-- Local image (must be in same folder) -->
<img src="my-image.jpg" alt="Description">
```

#### Issue: Gradients don't appear

**Solution:**
Make sure you're using the correct gradient class format:
```html
<!-- Correct -->
<div class="bg-gradient-to-r from-blue-500 to-cyan-500">

<!-- Incorrect -->
<div class="gradient-blue-cyan">
```

### Getting Help

If you encounter issues:

1. **Check the browser console for errors:**
   - Press F12
   - Click the "Console" tab
   - Look for red error messages

2. **Validate your HTML:**
   - Visit validator.w3.org
   - Paste your HTML code
   - Check for errors

3. **Compare with the original:**
   - Make sure you didn't accidentally delete important code
   - Check that all tags are properly closed

---

## Best Practices

### 1. Always Back Up Your Files

Before making major changes:
1. Right-click on your file
2. Select "Copy"
3. Paste it as `index-backup.html`
4. Keep this as a safety copy

### 2. Make One Change at a Time

1. Make a single change
2. Save and test in browser
3. If it works, move to next change
4. If it breaks, undo and try differently

### 3. Use Meaningful Changes

**Good approach:**
```html
<!-- Before -->
<h1 class="text-4xl">Fiber Optic Internet</h1>

<!-- After -->
<h1 class="text-4xl">Our Internet Service</h1>
```

**Avoid:**
```html
<!-- Risky - removing important classes -->
<h1>Our Internet Service</h1>
```

### 4. Keep Contact Information Updated

Maintain a list of all places contact info appears:
- [ ] Header phone number
- [ ] Hero section phone
- [ ] CTA sections
- [ ] Footer contact
- [ ] Email links

### 5. Test on Real Devices

Don't just test in browser DevTools:
- Test on an actual phone
- Test on a tablet
- Test on different browsers (Chrome, Firefox, Safari)

### 6. Check Links Regularly

Monthly, verify that:
- All phone links work
- All email links work
- All internal page links work
- Social media links go to correct profiles

### 7. Update Content Regularly

Keep your page fresh by:
- Updating testimonials
- Refreshing feature descriptions
- Updating pricing if it changes
- Adding new FAQ items

### 8. Use Consistent Formatting

Keep your code organized:
- Use proper indentation
- Keep similar elements consistent
- Comment sections for clarity

Example:
```html
<!-- Header Section -->
<header>
    <!-- Navigation -->
    <nav>
        <!-- Logo -->
        <div>...</div>
        <!-- Menu -->
        <div>...</div>
    </nav>
</header>

<!-- Main Content -->
<main>
    ...
</main>
```

### 9. Optimize for Performance

- Use optimized images (compressed)
- Minimize custom CSS
- Keep JavaScript lightweight
- Test page loading speed

### 10. Maintain Accessibility

- Always include `alt` text for images
- Use semantic HTML (proper heading hierarchy)
- Ensure sufficient color contrast
- Test with keyboard navigation

---

## Summary

You now have a comprehensive guide for maintaining and customizing your FiberNet landing page. Here's what you learned:

✓ How to update text content throughout the page
✓ How to modify styles using Tailwind CSS classes
✓ How to fix and manage all links
✓ How to create and link privacy and terms pages
✓ How to ensure mobile responsiveness
✓ How to troubleshoot common issues
✓ Best practices for ongoing maintenance

### Quick Reference Checklist

**Before Launching:**
- [ ] Update company name
- [ ] Update phone number (all locations)
- [ ] Update email address (all locations)
- [ ] Update social media links
- [ ] Create and link privacy.html
- [ ] Create and link terms.html
- [ ] Test all links work
- [ ] Test on mobile devices
- [ ] Test on different browsers

**Regular Maintenance:**
- [ ] Check all links monthly
- [ ] Update testimonials quarterly
- [ ] Review and update content annually
- [ ] Monitor page performance
- [ ] Update copyright year

### File Structure

```
your-website-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy policy)
├── terms.html          (Terms of service)
└── [optional: images/] (If using local images)
```

---

**Last Updated: January 2025**

For questions or additional support, consult the Tailwind CSS documentation at tailwindcss.com or reach out to a web developer in your area.