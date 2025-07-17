# XstreamFlex Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the XstreamFlex landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line in the header section:
```html
<a href="/" class="text-2xl font-bold text-indigo-600">XstreamFlex</a>
```
Replace "XstreamFlex" with your desired text.

2. **Navigation Items**: Located in both desktop and mobile menus:
```html
<a href="#features" class="text-gray-600 hover:text-indigo-600">Features</a>
<a href="#benefits" class="text-gray-600 hover:text-indigo-600">Benefits</a>
<a href="#faq" class="text-gray-600 hover:text-indigo-600">FAQ</a>
```
Modify the text between `<a>` tags to change menu items.

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">
    Xstream Flex, the Idea Launch Platform
</h1>
<p class="text-xl md:text-2xl text-white/90 mb-8 max-w-3xl mx-auto">
    Take your ideas to full live launch in days not weeks
</p>
```
- Change the heading by modifying text inside the `<h1>` tag
- Update the subheading by changing text inside the `<p>` tag
- The `md:text-6xl` means text size changes on medium screens - don't modify unless you understand responsive design

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-{size}`: Controls text size (xl, 2xl, etc.)
- `font-{weight}`: Controls text thickness (bold, semibold)
- `text-{color}-{shade}`: Sets text color (text-indigo-600)
- `bg-{color}-{shade}`: Sets background color
- `p-{number}`: Sets padding
- `m-{number}`: Sets margin
- `rounded-{size}`: Controls corner rounding

## Managing Links

### Navigation Links
1. Internal section links use hashtags:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
These correspond to section IDs in the HTML. To change:
- Update both the `href` and corresponding `id` attribute
- Example: `<a href="#new-section">` should match `<section id="new-section">`

### External Links
The main call-to-action button links to:
```html
<a href="https://pay.xstreamflex.com/order/starterlaunch/">
```
To update:
1. Replace the URL with your payment or signup page
2. Update this link everywhere it appears (hero section, features, CTA section)

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">
        <!-- Social icons here -->
    </a>
</div>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Find these lines in the footer:
```html
<li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```
Replace with:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Problems**
- Don't remove `md:` or `lg:` prefixes from classes
- These control how elements appear on different screen sizes
- Test your changes on mobile and desktop views

3. **Style Inconsistencies**
- Copy existing classes for new elements to maintain consistency
- Example: New buttons should use:
```html
class="inline-block bg-indigo-600 text-white px-6 py-3 rounded-full hover:bg-indigo-700 transition-colors duration-200"
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all changes in multiple browsers
- Test responsiveness using browser developer tools
- Keep a backup of the original code before making changes

Remember to always test your changes across different devices and browsers to ensure consistency in appearance and functionality.