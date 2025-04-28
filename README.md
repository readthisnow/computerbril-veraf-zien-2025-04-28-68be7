# Landing Page Maintenance Guide

This guide will help you maintain and customize the Computerbril landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and brand name. To update:

1. **Brand Name:**
```html
<a href="/" class="text-2xl font-bold text-indigo-600">Computerbril</a>
```
Replace "Computerbril" with your desired brand name.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-indigo-600">Kenmerken</a>
<a href="#benefits" class="text-gray-600 hover:text-indigo-600">Voordelen</a>
<a href="#faq" class="text-gray-600 hover:text-indigo-600">FAQ</a>
```
Replace "Kenmerken", "Voordelen", and "FAQ" with your desired menu items.

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900">
    Computerbril Veraf Zien
    <span class="block text-indigo-600 mt-2">Nu 20% Korting!</span>
</h1>
```

To modify:
1. Change the main headline by replacing "Computerbril Veraf Zien"
2. Update the promotion text "Nu 20% Korting!"
3. Adjust text size using Tailwind classes:
   - `text-4xl`: Default size
   - `sm:text-5xl`: Size on small screens
   - `lg:text-6xl`: Size on large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg">
    <h3 class="text-xl font-semibold mb-4">Verbeterd Zicht</h3>
    <p class="text-gray-600">Speciaal ontworpen voor optimaal zicht...</p>
</div>
```

To update:
1. Locate the feature you want to change
2. Replace the `<h3>` text with your feature title
3. Update the `<p>` text with your feature description

## Managing Links

### Navigation Links
Current navigation links are:

```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="https://computerbril.org/winkel">Bestel Nu</a>
```

To update:
1. Internal links (starting with #): Update the href to match your section IDs
2. External links: Replace the full URL in href
3. Example updating shop link:
```html
<a href="https://your-shop-url.com">Bestel Nu</a>
```

### Call-to-Action Buttons
Located in hero and features sections:

```html
<a href="https://computerbril.org/winkel" class="inline-flex items-center...">
    Profiteer Nu
</a>
```

Update by:
1. Changing the href URL
2. Modifying button text
3. Maintaining the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links:

```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Algemene Voorwaarden</a></li>
</ul>
```

To link to new pages:

1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Layout:**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all div tags are properly closed
   - Maintain the responsive classes (sm:, md:, lg: prefixes)

2. **Links Not Working:**
   - Ensure href attributes start with "/" for root-relative paths
   - Check for typos in URLs
   - Verify file names match exactly (case-sensitive)

3. **Styling Problems:**
   - Don't remove classes containing flex, grid, or container
   - Maintain the existing spacing classes (px-4, py-2, etc.)
   - Keep responsive design classes intact

### Need Help?

If you encounter issues:
1. Compare your changes against the original code
2. Verify all HTML tags are properly nested
3. Check the browser console for errors
4. Ensure all required files (Tailwind CSS, Alpine.js) are properly linked

Remember to test all changes across different screen sizes using your browser's developer tools.