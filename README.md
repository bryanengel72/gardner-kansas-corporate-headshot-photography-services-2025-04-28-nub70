# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header Section
```html
<a href="/" class="text-xl font-semibold tracking-tight">101Headshots</a>
```
To update the company name:
1. Locate this line in the `<header>` section
2. Replace "101Headshots" with your desired text
3. Keep the surrounding HTML tags and classes intact

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tighter mb-6">
    Gardner, Kansas Corporate Headshot Photography Services
</h1>
```
To modify the main headline:
1. Find this `<h1>` tag in the first `<section>`
2. Change only the text between the opening and closing tags
3. Maintain the existing classes to preserve responsive design

### Tailwind CSS Classes Explained

#### Understanding Responsive Classes
The landing page uses Tailwind's responsive prefixes:
- `md:` - applies styles on medium screens (768px and up)
- `lg:` - applies styles on large screens (1024px and up)

Example:
```html
<p class="text-xl md:text-2xl text-gray-600 leading-relaxed mb-10">
```
This paragraph has:
- `text-xl` - large text on mobile
- `md:text-2xl` - larger text on medium screens
- `text-gray-600` - gray color
- `leading-relaxed` - comfortable line height
- `mb-10` - bottom margin

#### Common Class Modifications

To change colors:
- Background: Replace `bg-white` with `bg-[color]-[shade]` (e.g., `bg-blue-500`)
- Text: Replace `text-gray-900` with `text-[color]-[shade]` (e.g., `text-blue-600`)

To adjust spacing:
- Padding: `p-[number]` (all sides), `py-[number]` (top/bottom), `px-[number]` (left/right)
- Margin: `m-[number]` (all sides), `my-[number]` (top/bottom), `mx-[number]` (left/right)

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update navigation links:
1. Locate the navigation menu in the `<header>`
2. For internal page sections, use `#section-id` format
3. For external links, use complete URLs starting with `https://`
4. Update the text between `<a>` tags to match your link names

### Book Now Button
```html
<a href="https://www.101headshots.com" class="hidden md:inline-block px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition-colors duration-300">Book Now</a>
```

To update the booking link:
1. Find all instances of `https://www.101headshots.com`
2. Replace with your booking system URL
3. Keep all classes to maintain button styling

## Adding Privacy and Terms Pages

### Footer Link Updates
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new files named `privacy.html` and `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in ID names
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the head section
   - Test on different screen sizes using browser dev tools

3. **Style Changes Not Working**
   - Verify Tailwind CDN link is present and working
   - Check for typos in class names
   - Ensure classes are space-separated

4. **Contact Information Updates**
   - Search for "bryan@101headshots.com" and "Gardner, Kansas"
   - Update all instances with your information
   - Check both visible text and meta tags

Remember to always test changes in multiple browsers and screen sizes before publishing updates to your live site.