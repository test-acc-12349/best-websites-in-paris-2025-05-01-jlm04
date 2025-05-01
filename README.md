# ParisWeb Landing Page Maintenance Guide

This guide will help you maintain and customize the ParisWeb landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-800">Paris<span class="text-blue-600">Web</span></a>
```
- Change "Paris" and "Web" to your desired text
- The blue color is controlled by `text-blue-600`

2. **Navigation Items**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other navigation items -->
</div>
```
- Update text between `>` and `</a>`
- Keep the `href` attributes matching your section IDs

### Hero Section
Find the hero section starting with:
```html
<section class="pt-32 pb-24 bg-gradient-to-br from-blue-50 to-white">
```
To modify:
1. Main heading: Update text between `<h1>` tags
2. Subheading: Update text in the `<p>` tag
3. Button text: Modify the text inside the `<a>` tag

### Tailwind CSS Tips
- Font sizes use classes like `text-xl`, `text-2xl`, etc.
- Colors use format `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing uses format `p-{number}` for padding, `m-{number}` for margin
- Responsive classes start with screen sizes: `md:`, `lg:`

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to match your section ID
2. Section IDs are defined like: `<section id="features">`
3. For external links, use complete URLs: `href="https://example.com"`

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600...">
```
To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link after updating

### Social Media Links
Found in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Other social links -->
</div>
```
Replace `#` with your social media profile URLs

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Find this section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Replace the `#` with:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check for typos in `href` attributes
- Ensure section IDs match exactly
- Test all links after updating

2. **Styling Problems**
- Verify Tailwind CSS classes are spelled correctly
- Check for missing closing tags
- Maintain the responsive design classes (e.g., `md:`, `lg:`)

3. **Layout Issues**
- Keep the container structure intact:
```html
<div class="container mx-auto px-6">
    <!-- Content here -->
</div>
```
- Don't remove responsive grid classes like `grid-cols-1 md:grid-cols-3`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test on multiple devices and browsers

Remember to always make a backup before making changes to your code.