# Landing Page Maintenance Guide
> A comprehensive guide for maintaining and customizing the Nachtbril Over Bril landing page.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Nachtbril
</a>
```
- Replace "Nachtbril" with your desired brand name
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Kenmerken</a>
    <!-- More menu items -->
</div>
```
- Update the text inside each `<a>` tag
- Maintain the `href` attributes that match your section IDs
- Keep the `hidden md:flex` class for proper mobile responsiveness

### Hero Section
Located in the first `<section>` after the header:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Nachtbril Over Bril
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Nu met 10% Korting - Nog maar enkele stuks beschikbaar!
</p>
```
- Update the h1 text while keeping the gradient classes
- Modify the promotional text in the paragraph
- The responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`) ensure proper scaling

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-xl`, `px-4`) indicate size
- `md:` and `lg:` prefixes apply styles at specific screen sizes
- Color classes follow the pattern: `text-{color}-{shade}` or `bg-{color}-{shade}`
- Don't remove `container`, `mx-auto`, or responsive classes as they maintain layout

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
- These are internal links to page sections
- The `#` symbol indicates they point to ID attributes

2. Call-to-Action Links:
```html
<a href="https://nachtbril.com/shop" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold px-8 py-4 rounded-full">
    Bestel Nu Met 10% Korting
</a>
```
- Replace `https://nachtbril.com/shop` with your actual shop URL
- Maintain the classes for proper button styling

### Updating Links Step-by-Step
1. Identify the link to update
2. Locate the `href` attribute
3. Replace the value with your new URL
4. Test the link after updating

Example:
```html
<!-- Before -->
<a href="https://nachtbril.com/shop">

<!-- After -->
<a href="https://your-domain.com/shop">
```

## Adding Policy Pages

### Footer Modification
Add policy links in the footer section:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-sm text-gray-400">
    <p>&copy; 2024 Nachtbril Over Bril. Alle rechten voorbehouden.</p>
    <!-- Add this below the copyright text -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling

Example structure for policy pages:
```html
<!DOCTYPE html>
<html lang="nl" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-sans antialiased bg-white text-gray-900">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-32">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
- Ensure section IDs match the href attributes
- IDs are case-sensitive
- Check for extra spaces in IDs

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `container` class on main sections
- Maintain the viewport meta tag in the head

3. **Gradient Text Not Showing**
- Ensure all three classes are present:
  - `bg-gradient-to-r`
  - `bg-clip-text`
  - `text-transparent`

4. **Mobile Menu Problems**
- Keep the `hidden md:flex` classes on the navigation
- Ensure the mobile menu button has the correct classes

Need more help? Contact support@example.com