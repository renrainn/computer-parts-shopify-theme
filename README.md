# Coffee Gear Demo Store (Shopify Theme Customization)

> **Personal practice project.** This is a demo store I built to practice Shopify theme development. It is not a client project or a live business.

A development store for a fictional coffee gear shop, built on Shopify's free **Dawn** theme. The goal was to practice writing custom Liquid sections that merchants can control from the theme editor.

## What I built vs. what came from Dawn

| Area | Source |
| --- | --- |
| Base theme, header, footer, product and cart templates | Dawn (unmodified, except for the items below) |
| Colors, fonts, and theme settings | Customized by me |
| `sections/testimonials-slider.liquid` | Written by me |
| `sections/featured-collection-custom.liquid` | Written by me |
| `sections/countdown-banner.liquid` | Written by me |

## Custom sections

### 1. Testimonials slider
- Merchant adds, removes, and reorders testimonials as **blocks** (up to 8)
- Each block has a quote, customer name, label, and 1 to 5 star rating
- CSS scroll-snap slider, no JavaScript
- Settings for heading, background color, and text color

### 2. Featured collection (custom layout)
- Pick any collection and the number of products to show
- Two layouts: standard grid, or "featured first" with a large first product
- Configurable desktop columns
- "Sale" and "Sold out" badges, compare-at price display
- Responsive images using `image_url` and `image_tag`

### 3. Countdown banner
- Live countdown to a date set in the theme editor
- Customizable message, button, and colors
- Shows a custom message when the countdown ends
- Safely hides the timer if the date is invalid

## Screenshots

<!-- Add your screenshots here, for example: -->
<!-- ![Homepage](screenshots/homepage.png) -->
<!-- ![Theme editor with custom sections](screenshots/theme-editor.png) -->

## Run it locally

Requires Node.js and [Shopify CLI](https://shopify.dev/docs/api/shopify-cli).

```bash
npm install -g @shopify/cli@latest
shopify auth login --store your-store.myshopify.com
shopify theme dev --store your-store.myshopify.com
```

The `shopify theme dev` command gives you a local preview URL with hot reload.

## Project structure

```
sections/
  testimonials-slider.liquid
  featured-collection-custom.liquid
  countdown-banner.liquid
```

(The rest of the repo is the standard Dawn theme structure.)

## What I learned

<!-- Fill this in with your own words. Suggestions: -->
<!-- - How section schema, settings, and blocks map to the theme editor -->
<!-- - Why presets are needed for a section to appear in "Add section" -->
<!-- - Something that broke and how you fixed it -->

## Contact

[Your name] | [your email] | [your GitHub profile]
