# BusinessPlan.AI Landing Page - Maintenance Guide

This guide will help you maintain and customize the BusinessPlan.AI landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections
The landing page is divided into these key sections:

1. Header (Navigation)
2. Hero Section
3. Features Section
4. Benefits Section
5. FAQ Section
6. Call-to-Action Section
7. Footer

### How to Update Text Content

#### Header/Navigation
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-600">BusinessPlan.AI</a>
```
To change the logo text, simply replace "BusinessPlan.AI" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">How To Start An Online Business</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">3 Step Business Plan Generator</p>
```
Replace the text between the `<h1>` and `<p>` tags to update your main headline and subheading.

### Understanding Tailwind CSS Classes

Key class patterns used in this landing page:

1. Spacing Classes:
   - `px-6`: Padding left/right 1.5rem
   - `py-4`: Padding top/bottom 1rem
   - `mb-8`: Margin bottom 2rem

2. Responsive Classes:
   - `md:text-2xl`: Apply style on medium screens and up
   - `lg:text-6xl`: Apply style on large screens and up

3. Color Classes:
   - `text-blue-600`: Blue text color
   - `bg-white`: White background
   - `text-gray-600`: Gray text color

Example of modifying a button:
```html
<!-- Original -->
<a href="https://ninja200.online" class="inline-block px-8 py-4 bg-blue-600 text-white">

<!-- Modified for green color -->
<a href="https://ninja200.online" class="inline-block px-8 py-4 bg-green-600 text-white">
```

## Managing Links

### Current Link Inventory

1. Navigation Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

2. Call-to-Action Links:
```html
<a href="https://ninja200.online">Get Started</a>
```

### Updating Links

1. Internal Links (Same Page):
```html
<!-- Format -->
<a href="#section-id">Link Text</a>

<!-- Example: Updating Features link -->
<a href="#new-section-id">New Section Name</a>
```

2. External Links:
```html
<!-- Format -->
<a href="https://your-external-url.com">Link Text</a>

<!-- Example: Updating Get Started button -->
<a href="https://your-generator-url.com">Get Started</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. Broken Links
```
Problem: Clicking links leads to "404 Not Found"
Solution: Double-check href attributes and file names match exactly
```

2. Responsive Design Issues
```
Problem: Design looks wrong on mobile
Solution: Ensure you haven't removed any "md:" or "lg:" prefixed classes
```

3. Color Inconsistencies
```
Problem: Colors don't match the design
Solution: Use the exact Tailwind color classes (e.g., blue-600) consistently
```

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check that all files are in the correct directory
- Verify all file names match exactly (case-sensitive)
- Test all links after making changes

Remember to always backup your files before making changes, and test your website on different devices and browsers after updates.