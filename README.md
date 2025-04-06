# Bloom Landing Page - Maintenance & Customization Guide

This guide provides detailed instructions for maintaining and customizing the Bloom florist landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name**
```html
<a href="/" class="text-2xl font-['Playfair_Display'] font-bold text-gray-800">Bloom</a>
```
- Replace "Bloom" with your company name
- Keep the Playfair Display font class for consistent styling

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `text-gray-600` and `hover:text-gray-900` classes for consistent hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Discover Stunning Floral Arrangements for Every Occasion
</h1>
```
- Update heading text while keeping all classes
- The `md:text-5xl lg:text-6xl` classes ensure proper sizing on different screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="w-16 h-16 bg-rose-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4 text-gray-900">Expert Florists</h3>
    <p class="text-gray-600 leading-relaxed">Our team of skilled professionals...</p>
</div>
```
To modify:
1. Update the `<h3>` title text
2. Change the description in the `<p>` tag
3. Keep all Tailwind classes to maintain styling and animations

## Managing Links

### Navigation Links
Current placeholder links that need updating:

1. **Main Navigation**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
- Keep the `#` prefix for internal section links
- For external pages, use full URLs: `href="https://yoursite.com/page"`

2. **Call-to-Action Buttons**
```html
<a href="https://yourwebsite.com" class="inline-block px-8 py-4 bg-rose-500...">
```
Replace `https://yourwebsite.com` with:
- Your order form URL
- Shopping cart page
- Contact page

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Social media icons -->
    </a>
</div>
```
Replace `#` with your social media profiles:
- Facebook: `https://facebook.com/your-page`
- Twitter: `https://twitter.com/your-handle`
- Instagram: `https://instagram.com/your-profile`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert the following code in the footer's Quick Links section:
```html
<ul class="space-y-4">
    <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
    <!-- Add these new lines -->
    <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match link hrefs
- Example: `<section id="features">` matches `<a href="#features">`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These control how elements appear on different screen sizes

3. **Style Inconsistencies**
- Keep the same color classes (e.g., `text-rose-500`)
- Maintain font classes: `font-['Playfair_Display']` for headings

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to test all changes across different devices and browsers before publishing updates to your live site.