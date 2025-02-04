# PolicyPals Landing Page - Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-400">PolicyPals</a>
```

To change the company name:
1. Locate this line in the header section
2. Replace "PolicyPals" with your desired text
3. Adjust text size using Tailwind classes if needed:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Discover Your Ideal Policy with PolicyPals.co.uk
</p>
```

To modify:
1. Find these elements in the first `<section>` tag
2. Update text content between the tags
3. Responsive text sizes are controlled by:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-900 rounded-2xl p-8 hover:transform hover:scale-105">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description text here.</p>
</div>
```

To update features:
1. Locate the `id="features"` section
2. Find each feature card within the grid
3. Modify the `<h3>` and `<p>` text as needed
4. Keep hover effects by maintaining these classes:
   - `hover:transform`
   - `hover:scale-105`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the navigation `<div>` in the header
2. For internal links (same page sections):
   - Use `#section-id` format (e.g., `href="#features"`)
3. For external links:
   - Replace `#` with full URL (e.g., `href="https://www.example.com"`)

### Call-to-Action Links
The main CTA buttons currently point to:

```html
<a href="https://www.PolicyPals.Co.Uk" class="inline-block px-8 py-4 bg-blue-500">
    Find Your Perfect Policy
</a>
```

To update:
1. Find all instances of `https://www.PolicyPals.Co.Uk`
2. Replace with your desired URL
3. Maintain the class structure for consistent styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

### Broken Responsive Design
If mobile layout breaks:
1. Check for removed `md:` prefixed classes
2. Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Missing Styles
If Tailwind styles don't apply:
1. Verify the Tailwind CDN link is present:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
2. Check for typos in class names
3. Ensure classes are space-separated

### Links Not Working
If internal links don't scroll:
1. Verify the `scroll-smooth` class is on the `<html>` tag
2. Check that section IDs match href values exactly
3. Ensure no spaces in IDs

Remember to:
- Test all changes on multiple devices
- Keep backup copies before making major changes
- Validate HTML using W3C validator
- Test all links after updating

Need additional help? Contact support@policypals.co.uk