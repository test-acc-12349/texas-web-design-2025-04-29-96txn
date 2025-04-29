# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Texas Web Design  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Best Websites In Texas  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Creating stunning, high-performance websites that drive results  <!-- Update subheadline -->
</p>
```

### Tailwind CSS Class Guide
Common classes used in this landing page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom (e.g., `py-24`)
- `px-[size]`: Adds padding left and right (e.g., `px-6`)

To modify responsive design:
```html
<!-- Example of responsive classes -->
<h1 class="text-5xl md:text-6xl lg:text-7xl">  <!-- Different sizes for different screens -->
```
- Default: `text-5xl` (mobile)
- `md:text-6xl` (medium screens)
- `lg:text-7xl` (large screens)

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Change the `href` value
2. Update the display text
3. Maintain the class structure

### Call-to-Action Buttons
Located in multiple sections:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-gradient-to-r from-blue-600 to-purple-600">
    Start Your Project  <!-- Update button text -->
</a>
```
Replace `https://twd.com` with your actual website URL.

### Footer Links
Located at the bottom of the page:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Links</h4>
    <ul class="space-y-2">
        <li><a href="#features">Features</a></li>
        <li><a href="#benefits">Benefits</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling

Example structure for policy pages:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-6 py-32">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check that all `href` attributes start with `/` for root-relative paths
   - Verify file names match exactly (case-sensitive)
   - Test all links after updating

2. **Styling Issues**
   - Keep the original class structure when updating
   - Don't remove responsive classes (e.g., `md:`, `lg:` prefixes)
   - Maintain gradient classes for consistent branding

3. **Responsive Design**
   - Test on multiple screen sizes after changes
   - Keep the `viewport` meta tag in the head section
   - Don't remove `container` classes from main sections

Need help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).