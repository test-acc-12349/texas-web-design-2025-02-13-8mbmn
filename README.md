# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text (TWD)**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">TWD</a>
```
- Replace "TWD" with your desired text
- The gradient effect will automatically apply to your new text

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Texas Web Design</h1>
<p class="text-xl md:text-2xl lg:text-3xl mb-12 text-gray-300">Best Websites In Texas</p>
```
- Update heading text while maintaining the gradient classes
- Modify subheading text within the `<p>` tag
- The responsive text sizes (`text-4xl`, `md:text-6xl`, etc.) ensure proper display on all devices

### Features Section
To update feature cards:
```html
<div class="bg-gray-900 p-8 rounded-2xl hover:scale-105 transition-transform duration-300">
    <i class="fas fa-server text-4xl text-purple-400 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-400">Professional hosting included with every website package.</p>
</div>
```
- Change icon by updating the `fa-server` class to any [Font Awesome](https://fontawesome.com/icons) icon
- Modify heading text in the `<h3>` tag
- Update description in the `<p>` tag

## Managing Links

### Internal Navigation Links
Current internal links use section IDs:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Locate the section you want to link to
2. Ensure it has an `id` attribute: `<section id="your-section-name">`
3. Update the `href` to match: `<a href="#your-section-name">`

### External Links
The main call-to-action buttons currently point to a placeholder URL:
```html
<a href="https://twd.com" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
```
To update:
1. Replace `https://twd.com` with your actual website URL
2. Test the link to ensure it opens correctly
3. Consider adding `target="_blank"` for external links to open in new tabs

### Email Links
The contact section contains an email link:
```html
<a href="mailto:admin@twd.com">Contact Us</a>
```
Update by replacing `admin@twd.com` with your actual email address

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links in the footer:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy policy page (e.g., `privacy.html`)
2. Create your terms of service page (e.g., `terms.html`)
3. Update the links in the footer:
```html
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradient Text**
If gradient text disappears:
- Ensure all three classes are present:
  ```html
  bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
  ```

2. **Responsive Design Issues**
If elements look wrong on mobile:
- Check for responsive classes (md:, lg:)
- Ensure the viewport meta tag is present:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```

3. **Missing Icons**
If Font Awesome icons don't appear:
- Verify the Font Awesome CDN link is present in the head:
  ```html
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
  ```

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test all changes across different devices and browsers

Remember to always backup your files before making significant changes!