# DharaMitra Landing Page - Maintenance Guide

This guide will help you maintain and customize the DharaMitra landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <div class="text-2xl font-bold text-green-600">DharaMitra</div>
        <!-- Navigation items -->
    </nav>
</header>
```

To modify:
1. Change company name: Update the text "DharaMitra" within the `<div>` tag
2. Adjust logo size: Modify `text-2xl` to `text-3xl` for larger text
3. Change color: Replace `text-green-600` with other Tailwind colors (e.g., `text-blue-600`)

### Hero Section
The main banner section contains:

```html
<div class="max-w-4xl mx-auto text-center text-white">
    <h1 class="text-4xl md:text-6xl font-bold mb-6">DharaMitra(Trichoderma viride)...</h1>
    <p class="text-xl md:text-2xl mb-8">Biocontrol Fungus Containing...</p>
</div>
```

To modify:
1. Update heading: Replace text within the `<h1>` tag
2. Change subheading: Modify text within the `<p>` tag
3. Adjust spacing: Modify `mb-6` and `mb-8` values (margin-bottom)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow">
    <div class="text-green-600 text-4xl mb-4">
        <i class="fas fa-shield-alt"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Controls Rhizome Rot</h3>
    <p class="text-gray-600">Effectively prevents and controls...</p>
</div>
```

To modify:
1. Change icon: Replace `fa-shield-alt` with other FontAwesome icons
2. Update feature title: Modify text within `<h3>` tags
3. Edit description: Update text within `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation structure:

```html
<div class="hidden md:flex space-x-6">
    <a href="#features" class="hover:text-green-600 transition-colors">Features</a>
    <a href="#benefits" class="hover:text-green-600 transition-colors">Benefits</a>
    <a href="#faq" class="hover:text-green-600 transition-colors">FAQ</a>
</div>
```

To update links:
1. Internal links: Keep the `#` prefix for same-page sections
2. External links: Replace `href="#features"` with full URLs
3. Add new links: Copy existing `<a>` tag structure and modify

### WhatsApp Button
Current WhatsApp link structure:

```html
<a href="https://wa.me/917032666266?text=Dharamitra" 
   class="bg-green-600 text-white px-6 py-2 rounded-full hover:bg-green-700">
    Buy Now
</a>
```

To modify:
1. Update phone number: Change `917032666266` to new number
2. Edit message: Modify `text=Dharamitra` parameter
3. Change button text: Update "Buy Now" text

## Adding Policy Pages

### Footer Policy Links
Current policy link section:

```html
<div>
    <h4 class="text-xl font-bold mb-4">Policies</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-green-400">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-green-400">Terms of Service</a></li>
        <li><a href="#" class="hover:text-green-400">Shipping Policy</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create new HTML files:
   ```html
   privacy.html
   terms.html
   shipping.html
   ```

2. Update href attributes:
   ```html
   <li><a href="privacy.html" class="hover:text-green-400">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-green-400">Terms of Service</a></li>
   <li><a href="shipping.html" class="hover:text-green-400">Shipping Policy</a></li>
   ```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in ID names
   - Verify that sections have unique IDs

2. **Responsive Design Issues**
   - Keep `md:` prefixed classes for responsive behavior
   - Test on multiple screen sizes
   - Don't remove `container` classes

3. **Icon Display Problems**
   - Verify FontAwesome CSS is properly linked
   - Check icon class names against FontAwesome documentation
   - Ensure internet connectivity for CDN access

### Need Help?
For additional support:
- Check Tailwind CSS documentation
- Verify HTML syntax
- Test all links before deploying
- Maintain backup copies before making changes

Remember to always test changes in a development environment before pushing to production.