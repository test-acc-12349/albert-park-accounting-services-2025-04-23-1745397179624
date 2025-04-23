# Albert Park Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Modifying Text Content

The landing page is divided into several key sections. Here's how to update text in each:

#### Header (Navigation)
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold">
    Albert Park  <!-- Change company name here -->
</a>
```

#### Hero Section
```html
<!-- Main headline -->
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold">
    Your financial success is our bottom line  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300">
    Premium accounting services...  <!-- Update subheadline here -->
</p>
```

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-semibold mb-4">
        Tax Optimization  <!-- Feature title -->
    </h3>
    <p class="text-gray-400">
        Strategic tax planning...  <!-- Feature description -->
    </p>
</div>
```

### Understanding Tailwind Classes

Key Tailwind classes used in this design:

- Layout Classes:
  - `container`: Centers content
  - `mx-auto`: Horizontal center alignment
  - `px-6`: Horizontal padding
  - `py-24`: Vertical padding

- Responsive Classes:
  - `md:text-5xl`: Applies at medium screens
  - `lg:text-7xl`: Applies at large screens

- Design Classes:
  - `bg-gray-900`: Dark background
  - `text-gray-100`: Light text
  - `rounded-2xl`: Rounded corners
  - `hover:scale-105`: Hover animation

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. Call-to-Action Links:
```html
<!-- Update this URL -->
<a href="https://theaccountants.com" class="inline-block px-8 py-4">
    Get Started Today
</a>
```

3. Footer Links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#">About Us</a></li>  <!-- Add proper URLs -->
    <li><a href="#">Careers</a></li>
    <li><a href="#">Blog</a></li>
</ul>
```

### How to Update Links
1. Internal Links (same page):
   - Use `#section-id` format
   - Example: `<a href="#features">Features</a>`

2. External Links:
   - Use full URL including https://
   - Example: `<a href="https://your-domain.com/about">About Us</a>`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer section:
```html
<div>
    <ul class="space-y-2 text-gray-400">
        <!-- Add after existing footer links -->
        <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
Create two new files in your root directory:
- `privacy.html`
- `terms.html`

Use the same header and footer structure as `index.html` for consistency.

## Troubleshooting

Common Issues and Solutions:

1. **Broken Responsive Design**
   - Check `md:` and `lg:` prefixes are correct
   - Verify Tailwind CDN is loading
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Links Not Working**
   - Ensure IDs match href attributes exactly
   - Check for typos in URLs
   - Verify file paths are correct

3. **Styling Issues**
   - Confirm class names are spelled correctly
   - Check for missing closing tags
   - Verify all required classes are present

Remember:
- Always test changes across different screen sizes
- Backup files before making major changes
- Use browser developer tools to inspect elements
- Keep the gradient styling consistent across sections

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)