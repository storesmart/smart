# Elevate Smart Vending — Website

A premium, production-ready static website for a smart vending machine service business. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies.

## Quick Start

1. Clone or download this repository
2. Open `index.html` in any browser — that's it

No build step, no npm install, no server required.

## Deploy to GitHub Pages

1. Create a new GitHub repository
2. Push all files to the `main` branch
3. Go to **Settings > Pages**
4. Under "Source", select `main` branch and `/ (root)` folder
5. Click **Save**
6. Your site will be live at `https://yourusername.github.io/repo-name/`

## Customization Guide

### Replace Business Name

Search and replace these strings across all files:

| Placeholder | Replace With |
|-------------|-------------|
| `Elevate Smart Vending` | Your business name |
| `Elevate` (in nav/logo) | Your short brand name |

**Files to update:** `index.html`

### Replace Phone Number

Search for `(555) 123-4567` and replace with your actual phone number.

**Files to update:** `index.html`

### Replace Email

Search for `info@elevatesmartvending.com` and replace with your actual email.

**Files to update:** `index.html`

### Replace Address

Search for `123 Commerce Blvd, Suite 200, Edmonton, AB T5J 2R1` and replace with your actual address.

**Files to update:** `index.html` (contact section, footer, JSON-LD schema)

### Replace Logo

1. Create your logo as an SVG or PNG file
2. Place it in `assets/logo/`
3. In `index.html`, find the SVG in the `<header>` nav and replace it with an `<img>` tag:
   ```html
   <img src="assets/logo/your-logo.svg" alt="Your Brand" width="32" height="32">
   ```
4. Also update the logo in the `<footer>`

### Replace Images

All images are in `assets/images/`. Replace with your own photos:

| File | Used For | Recommended Size |
|------|----------|-----------------|
| `hero-lobby.jpg` | Hero section, contact sidebar | 1200x1600px (portrait) |
| `cooler-closeup.jpg` | About section, showcase background, gallery | 2560x1978px (landscape) |
| `gallery-1.png` | Gallery grid | 2250x2250px (square) |
| `gallery-2.png` | Gallery grid | 2250x2250px (square) |
| `gallery-3.png` | Gallery grid | 2250x2250px (square) |

**Tips:**
- Use real photos of your vending machines in actual locations
- Compress images with [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/) for faster loading
- Maintain aspect ratios or update CSS if changing dimensions
- Add more gallery images by copying `.gallery-item` blocks in the HTML

### Replace Service Area

Update the "Edmonton" references in:
- Hero section text
- About section
- Industries section
- JSON-LD schema (`"areaServed"`)
- All meta tags
- Footer

### Change Colors

Edit the CSS custom properties at the top of `styles.css`:

```css
:root {
  --color-primary: #111827;     /* Deep charcoal */
  --color-secondary: #2563EB;   /* Modern blue */
  --color-accent: #10B981;      /* Fresh green */
  --color-bg: #FAFAFA;          /* Background */
  --color-surface: #FFFFFF;      /* Cards */
}
```

Also update the dark mode colors in the `[data-theme="dark"]` block.

### Change Fonts

1. Visit [Google Fonts](https://fonts.google.com/)
2. Select your fonts and copy the `<link>` tag
3. Replace the Google Fonts `<link>` in `index.html` `<head>`
4. Update `--font-heading` and `--font-body` in `styles.css`

## File Structure

```
/
├── index.html          # Main page (all sections, SEO, schema)
├── styles.css          # Complete stylesheet (light/dark, responsive, animations)
├── script.js           # Interactions (animations, lightbox, dark mode, form)
├── assets/
│   └── images/         # Product and lifestyle photos
│       ├── hero-lobby.jpg
│       ├── cooler-closeup.jpg
│       ├── gallery-1.png
│       ├── gallery-2.png
│       └── gallery-3.png
└── README.md           # This file
```

## Features

- **17 sections** — Hero, trust bar, about, why choose us, showcase, comparison, industries, products, how it works, gallery, testimonials, statistics, FAQ, contact, footer
- **Dark mode** — Toggle with localStorage persistence and system preference detection
- **Scroll animations** — Fade-up on scroll via Intersection Observer
- **Animated counters** — Numbers count up when statistics section enters viewport
- **Lightbox gallery** — Click any gallery image for full-screen view
- **FAQ accordion** — Smooth expand/collapse with single-open behavior
- **Mobile responsive** — Hamburger menu, stacked grids, touch-friendly
- **SEO optimized** — Meta tags, Open Graph, Twitter Card, JSON-LD LocalBusiness schema
- **Accessible** — ARIA labels, focus management, keyboard navigation, prefers-reduced-motion
- **Zero dependencies** — No frameworks, no build tools, no jQuery

## Performance Notes

- All images use `loading="lazy"` except the hero image
- CSS and JS are minification-ready (no ES6 modules that need bundling)
- No external dependencies to load (except Google Fonts)
- Target: 90+ Lighthouse score on a fast connection

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
