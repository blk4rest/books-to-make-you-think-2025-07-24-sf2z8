# ThinkBooks Landing Page - Maintenance Guide

This guide will help you maintain and customize the ThinkBooks landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu:

```html
<header class="fixed w-full bg-white/90 backdrop-blur-sm z-50 border-b border-gray-100">
    <nav class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
            <a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">ThinkBooks</a>
```

To update:
1. Change logo text: Replace "ThinkBooks" with your desired text
2. Modify logo colors: Adjust `from-purple-600 to-blue-500` to different Tailwind color classes
   - Example: `from-red-600 to-orange-500` for a warm gradient
   - [Tailwind Colors Reference](https://tailwindcss.com/docs/customizing-colors)

### Hero Section
The main headline and introduction are in the hero section:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Books to Make You Think</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Discover transformative books that challenge your perspective and expand your mind.</p>
```

To modify:
1. Update headline: Replace text between `<h1>` tags
2. Change subtitle: Modify text in the `<p>` tag
3. Adjust text sizes:
   - `text-5xl`: Base size
   - `md:text-6xl`: Medium screens
   - `lg:text-7xl`: Large screens

### Feature Cards
Each feature card follows this structure:

```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-2xl font-bold mb-4">Philosophy Books</h3>
    <p class="text-gray-600">Explore profound ideas...</p>
</div>
```

To customize:
1. Change title: Update text in `<h3>` tags
2. Modify description: Edit text in `<p>` tags
3. Adjust colors:
   - Background: Change `bg-white`
   - Icon background: Modify `bg-purple-100`
   - Text color: Update `text-gray-600`

## Managing Links

### Navigation Menu Links
Current navigation structure:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Books</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Internal links (same page):
   - Use `#section-id` format
   - Example: `href="#features"`
2. External links:
   - Use full URL
   - Example: `href="https://example.com/page"`

### Contact Email
Update the email link:

```html
<a href="mailto:somewhatskepticalauthor@protonmail.com" class="text-xl text-purple-600 hover:text-purple-700 transition-colors duration-300">somewhatskepticalauthor@protonmail.com</a>
```

Replace both the `href="mailto:..."` and visible email address with your contact email.

## Adding Privacy and Terms Pages

### Step 1: Create Footer Links
Add to the footer section before the copyright notice:

```html
<div class="flex space-x-6 mb-4">
    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy header and footer from index.html
3. Add content between them
4. Maintain consistent styling

Example privacy.html structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-['Inter'] antialiased bg-white text-gray-900">
    <!-- Copy header section -->
    
    <main class="pt-32 px-6">
        <div class="container mx-auto max-w-3xl">
            <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add privacy policy content -->
        </div>
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common Issues:
1. **Broken Gradients**
   - Ensure Tailwind CSS CDN link is working
   - Check for typos in color class names
   - Verify `bg-gradient-to-r` class is present

2. **Responsive Issues**
   - Check responsive prefixes (`md:`, `lg:`)
   - Verify container classes are present
   - Test on different screen sizes

3. **Link Problems**
   - Confirm file paths are correct
   - Check for proper `href` syntax
   - Ensure IDs match link targets

Need help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).