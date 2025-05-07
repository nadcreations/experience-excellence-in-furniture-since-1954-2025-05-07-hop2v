# Al Mutlaq Furniture Landing Page - Maintenance Guide

This guide will help you maintain and customize the Al Mutlaq Furniture landing page. It's written for beginners and provides detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<span class="text-2xl font-bold text-gray-900">Al Mutlaq</span>
```

To change the company name, simply modify the text between the `<span>` tags.

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Experience Excellence in Furniture Since 1954
</h1>
<p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto mb-12">
    Elegant Designs. Premium Quality. Tailored Solutions.
</p>
```

Understanding the Tailwind classes:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing (2rem)

### Features and Benefits Sections
Each feature card follows this structure:

```html
<div class="bg-gray-50 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
    <!-- Icon container -->
    <div class="w-12 h-12 bg-gray-900 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Project Management</h3>
    <p class="text-gray-600">Expert guidance from concept to completion...</p>
</div>
```

To update:
1. Change the heading text within `<h3>` tags
2. Modify the description within `<p>` tags
3. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
Current navigation links are found in the header:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="https://almutlaqfurniture.com/" class="inline-flex items-center...">Contact Us</a>
</div>
```

To update links:
1. Internal links (starting with #) connect to sections on the same page
2. External links (starting with http) go to other websites
3. Update the `href` attribute with your new URL

### Contact Button Links
The main contact buttons need updating in two places:

```html
<!-- Hero section button -->
<a href="https://almutlaqfurniture.com/" class="inline-flex items-center...">
    Explore Our Collection
</a>

<!-- CTA section button -->
<a href="mailto:projects@almutlaqfurniture.com" class="inline-flex items-center...">
    Contact Us Today
</a>
```

## Adding Privacy and Terms Pages

### Current Footer Links
The privacy and terms links are in the footer:

```html
<div>
    <h4 class="text-sm font-semibold text-gray-900 uppercase tracking-wider mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your website folder
2. Update the href attributes:

```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in the ID names
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `max-w-7xl` class on container elements
   - Maintain the existing responsive grid classes

3. **Animation Problems**
   - Check that AOS script is loaded
   - Verify `data-aos` attributes are spelled correctly
   - Ensure the AOS initialization code is present:

```html
<script>
    AOS.init({
        duration: 1000,
        once: true,
    });
</script>
```

Remember to always test changes across different screen sizes using your browser's developer tools before publishing updates.

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).