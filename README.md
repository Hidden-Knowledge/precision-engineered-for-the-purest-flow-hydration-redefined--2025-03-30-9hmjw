# AquaFlow Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the AquaFlow landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <div class="flex items-center">
            <a href="/" class="text-2xl font-bold text-blue-600">AquaFlow</a>
        </div>
        <!-- Navigation items -->
    </nav>
</header>
```

To modify:
- Company name: Change the text "AquaFlow" within the `<a>` tag
- Text color: Modify `text-blue-600` to other colors (e.g., `text-red-600`)
- Font size: Adjust `text-2xl` to `text-3xl` for larger text

### Hero Section
The main banner section contains:

```html
<div class="max-w-4xl mx-auto text-center text-white">
    <h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
        Precision-Engineered for the Purest Flow—Hydration Redefined.
    </h1>
    <p class="text-xl md:text-2xl mb-8">
        Smart hydration systems backed by hydrodynamics science
    </p>
</div>
```

To modify:
- Heading: Replace text within the `<h1>` tag
- Subheading: Update text within the `<p>` tag
- Text size: Adjust `text-4xl` or `text-xl` classes
- Spacing: Modify `mb-6` or `mb-8` for different margins

### Tailwind CSS Class Guide
Common classes used:
- Text sizes: `text-sm`, `text-xl`, `text-2xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-600`
- Spacing: `px-4` (padding), `my-8` (margin)
- Responsive: `md:text-6xl` (applies at medium screens)

## Managing Links

### Navigation Menu Links
Current navigation links:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="https//stripe.com" class="bg-blue-600 text-white">Buy Now</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. Replace with new URL or section ID
3. For internal links, use `#section-name`
4. For external links, use complete URLs starting with `https://`

### Fix Broken Links
Current broken link:
```html
<a href="https//stripe.com">
```
Should be:
```html
<a href="https://stripe.com">
```

## Adding Privacy and Terms Pages

### Footer Links Setup
Current footer structure:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update footer links:
   ```html
   <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

## Troubleshooting

### Common Issues

1. **Broken Images**
   - Check image URLs in `src` attributes
   - Ensure images exist at specified paths
   - Verify image file extensions

2. **Responsive Issues**
   - Look for `md:` prefixed classes
   - Test at different screen sizes
   - Ensure mobile menu button works

3. **Link Problems**
   - Verify all `href` attributes have correct syntax
   - Check for missing `https://` in external links
   - Confirm internal section IDs match their targets

### Need Help?
- Check browser developer tools (F12) for errors
- Verify all files are in correct directories
- Ensure Tailwind CSS CDN link is working
- Test all interactive elements after changes

Remember to:
- Back up files before making changes
- Test on multiple browsers
- Validate HTML using W3C validator
- Check mobile responsiveness

---
For additional support or questions, contact your development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).