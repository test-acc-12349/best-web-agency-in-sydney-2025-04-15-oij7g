# Web Agency Landing Page - Maintenance Guide

This guide will help you maintain and customize the Web Agency landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Company Name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-white tracking-tight">WebAgency</a>
```
Simply replace "WebAgency" with your company name.

### Hero Section
The main headline and subheading can be found here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Best Web Agency In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-10">
    Grow your business with clicks
</p>
```
- Replace "Best Web Agency In Sydney" with your main headline
- Replace "Grow your business with clicks" with your tagline

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-6`, `mb-10`)
- `bg-[color]`: Sets background color (e.g., `bg-gray-900`)
- `text-[color]`: Sets text color (e.g., `text-white`, `text-gray-300`)

To modify spacing:
```html
<!-- Example: Increasing bottom margin from 6 to 8 -->
<h1 class="mb-6">  →  <h1 class="mb-8">
```

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to (e.g., `id="features"`)
2. Use that ID in your href with a # prefix (e.g., `href="#features"`)

### Call-to-Action Links
The main CTA buttons currently point to "https://fixrr.online":
```html
<!-- Find these lines and update the href -->
<a href="https://fixrr.online" class="inline-flex items-center...">
```
Replace with your desired URL.

### Footer Links
Update company information and links in the footer:
```html
<!-- Company contact -->
<p class="text-gray-400">Contact: contact@example.com</p>

<!-- Service links -->
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Web Design</a></li>
    <!-- Add your service page URLs here -->
</ul>
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
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Links Not Working**
   - Check that the href value exactly matches the section ID
   - Ensure IDs don't contain spaces
   - Verify file paths are correct for external pages

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for typos in class names
   - Maintain the responsive classes (e.g., `md:`, `lg:` prefixes)

3. **Animation Issues**
   - Verify AOS script is loaded
   - Check data-aos attributes are properly set
   - Ensure AOS.init() is called

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes, and test all modifications across different devices and browsers.