# Connected Employees Landing Page - Maintenance Guide

This guide will help you maintain and customize the Connected Employees landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo Text:**
```html
<!-- Find this section in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    ConnectedEmployees  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Better Engagement & Collaboration Through Connected Employees  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Get that sense of belonging & attachment to colleagues now  <!-- Subheading -->
</p>
```

### Understanding Tailwind CSS Classes
Common classes used in this page:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-gray-600`, `text-white`, `bg-purple-600`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive design: `md:text-xl` (applies at medium screens and up)

## Fixing Broken Links

### Navigation Menu Links
Current internal links and how to update them:

```html
<!-- In the navigation menu -->
<div class="hidden md:flex space-x-8">
    <!-- These are section links - update the href to match your section IDs -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Call-to-Action (CTA) Links
Update the main website URL:

```html
<!-- Find all instances of this URL and update it -->
<a href="https://www.connectedemployees.co.uk" class="inline-flex items-center...">
```

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <!-- Update these href attributes with your social media profiles -->
    <a href="#" class="text-gray-400 hover:text-white">Twitter</a>
    <a href="#" class="text-gray-400 hover:text-white">LinkedIn</a>
</div>
```

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
In the footer, locate this section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes to point to your policy pages -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating New Policy Pages
1. Create new files named `privacy.html` and `terms.html` in the same directory
2. Use the same styling classes for consistency
3. Example structure for policy pages:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy the same head section from index.html -->
</head>
<body class="font-['Inter'] antialiased bg-white text-gray-900">
    <!-- Copy the header from index.html -->
    
    <main class="pt-32 px-6">
        <div class="container mx-auto max-w-3xl">
            <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your policy content here -->
        </div>
    </main>

    <!-- Copy the footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
   - Check that you haven't removed any `md:` or `lg:` prefixed classes
   - Ensure the viewport meta tag is present in the head section

2. **Missing Styles**
   - Verify the Tailwind CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

3. **Gradient Text Not Showing**
   - Ensure these classes are present for gradient text:
   ```html
   bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent
   ```

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Verify all links start with either `http://`, `https://`, or `#` for internal links

Remember to test all changes across different screen sizes and browsers before deploying to production.