# Landing Page Maintenance Guide
## For Sexy Underneath E-commerce Site

This guide provides detailed instructions for maintaining and customizing the Sexy Underneath landing page. Perfect for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<a href="/" class="text-2xl font-bold">Sexy Underneath</a>

<!-- How to modify -->
<a href="/" class="text-2xl font-bold">Your Brand Name</a>
```

#### Hero Section
Look for the following section and update the text between the tags:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
    Luxury Lingerie for Confidence & Comfort
</h1>
<p class="text-xl md:text-2xl mb-8">
    Shop the best lingerie—approved by real women.
</p>
```

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` prefix means the style applies only on medium screens and larger
- Example: `text-4xl md:text-6xl` means:
  - Normal screens: text is extra-large (4xl)
  - Medium screens and up: text is super-large (6xl)

#### Common Class Patterns
```html
<!-- Button styling -->
class="bg-black text-white px-6 py-2 rounded-full hover:bg-gray-800 transition-colors duration-300"
- bg-black: Black background
- text-white: White text
- px-6: Horizontal padding
- py-2: Vertical padding
- rounded-full: Rounded corners
- hover:bg-gray-800: Darker background on hover
- transition-colors: Smooth color transition
```

## Fixing Broken Links

### Navigation Menu Links
Current placeholder links in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-black transition-colors duration-300">Shop</a>
    <a href="#" class="text-gray-600 hover:text-black transition-colors duration-300">Collections</a>
    <a href="#" class="text-gray-600 hover:text-black transition-colors duration-300">About</a>
    <a href="#" class="text-gray-600 hover:text-black transition-colors duration-300">Contact</a>
</div>
```

To update these links:
1. Replace `#` with your actual page URLs
2. Example:
```html
<a href="/shop" class="text-gray-600 hover:text-black transition-colors duration-300">Shop</a>
```

### Footer Links
Current footer links that need updating:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Shop</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
</ul>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to the "Quick Links" section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <!-- Add these new links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Privacy and Terms Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Check for `md:` prefixes in classes
   - Ensure you haven't removed important responsive classes
   - Test on different screen sizes

2. **Missing Styles**
   - Verify the Tailwind CSS link is present:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```

3. **Links Not Working**
   - Check for typos in URLs
   - Ensure files exist in the correct directory
   - Use relative paths (e.g., `/shop`) for internal links
   - Use full URLs (e.g., `https://example.com`) for external links

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Test all changes in multiple browsers
- Maintain a backup of the original files

Remember: Always test your changes thoroughly before pushing to production!