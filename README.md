# DiferenciasEntre Landing Page - Maintenance Guide

This guide will help you maintain and customize the DiferenciasEntre landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-xl font-bold text-blue-600">DiferenciasEntre</a>
```
- Replace "DiferenciasEntre" with your desired text
- The `text-blue-600` class controls the blue color
- `text-xl` controls the size

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#caracteristicas" class="text-gray-600 hover:text-blue-600">Características</a>
    <!-- Other menu items -->
</div>
```
- Update text between `<a>` tags
- Keep the `href` attributes matching your section IDs
- `space-x-8` controls spacing between items

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight">
    Diferencias Entre Conceptos y Términos Explicadas de Forma Clara
</h1>
```
- Update the heading text while maintaining the multi-line structure
- The classes control responsive text sizes:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features and Benefits
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg">
    <h3 class="text-xl font-semibold mb-4">Comparaciones Claras</h3>
    <p class="text-gray-600">Explicaciones detalladas y fáciles de entender...</p>
</div>
```
- Update heading and paragraph text
- Maintain the existing classes for consistent styling
- `shadow-lg` adds the box shadow effect
- `rounded-xl` controls corner rounding

## Managing Links

### Internal Navigation Links
Current internal links are:
```html
<a href="#caracteristicas">Características</a>
<a href="#beneficios">Beneficios</a>
<a href="#faq">FAQ</a>
<a href="#contacto">Contacto</a>
```
To update:
1. Ensure the `href` matches the section ID
2. Section IDs are defined like: `<section id="caracteristicas">`
3. Keep the `#` prefix for smooth scrolling

### External Links
The main call-to-action buttons link to:
```html
<a href="https://diferenciasentre.net/" class="inline-block bg-blue-600">
    Comenzar Ahora
</a>
```
To update:
1. Replace the URL in `href`
2. Test the link after updating
3. Maintain the existing classes for styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Términos de Uso</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Términos de Uso</a></li>
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links:**
- Check that section IDs match exactly with href attributes
- Section IDs are case-sensitive
- Ensure there are no spaces in IDs

2. **Responsive Design Issues:**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `container` class on parent divs
- Maintain the existing grid structure in sections

3. **Styling Problems:**
- Always include both the base and hover classes (e.g., `text-gray-600 hover:text-blue-600`)
- Keep the `transition-colors duration-300` for smooth effects
- Maintain the hierarchy of padding and margin classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test all changes across different screen sizes using browser dev tools

Remember to always backup your files before making changes and test thoroughly across different devices and browsers.