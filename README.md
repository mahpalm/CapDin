# Mah Dining Room — Website

A single-file, responsive restaurant website for **Mah Dining Room**, a South-South Nigerian cuisine restaurant on Airport Road, Benin City, Edo State — founded by Chef Mahmud.

## Overview

This is a self-contained `index.html` file (no build tools, no npm install) that includes all HTML, CSS, and JavaScript needed to run the site. It's built on Bootstrap 5.3 with a custom bronze/coral/palm color palette inspired by Benin bronze-casting and Edo cultural heritage.

## Features

- **Responsive navbar** with dropdown menu categories and quick-access Order/Reserve/Delivery buttons
- **Hero section** with restaurant tagline and call-to-action buttons
- **About section** highlighting founder Chef Mahmud
- **Filterable menu** across 4 categories — Main Dish, Grills & Protein, Small Chops & Dessert, and Drinks — with 18 dishes total
- **Animated testimonials** section using `IntersectionObserver` to fade/slide guest reviews into view on scroll
- **Photo gallery** with a custom lightbox (click to enlarge)
- **Delivery section** with animated floating icons and delivery info cards
- **Reservation form** with client-side validation and a confirmation toast
- **Order Now modal** for placing delivery/pickup orders
- **Contact section** with an embedded Google Maps iframe and enquiry form
- **Footer** with social links, sitemap, and business hours

## Tech Stack

| Component | Details |
|---|---|
| CSS Framework | Bootstrap 5.3.3 (CDN) |
| Fonts | Google Fonts — Cinzel (headings) & Jost (body) |
| JavaScript | Vanilla JS (no framework) |
| Icons | Inline SVG + emoji |
| Maps | Google Maps embed (iframe) |

## File Structure

```
index.html          → the entire site (HTML + CSS + JS in one file)
```

### Required Image Assets

The following image files must sit alongside `index.html` for the page to render correctly:

**About**
`imgchef.jpeg`

**Menu (dishes)**
`Afang.jpeg`, `Banga.jpeg`, `Black.jpeg`, `imagho.jpeg`, `Onu.jpeg`, `Suya.jpeg`, `Cat.jpeg`, `Azu.jpeg`, `Tuk.jpeg`, `Puf.jpeg`, `Chin.jpeg`, `Sam.jpeg`, `Zob.jpeg`, `Co.jpeg`, `zobo.jpeg`, `Chap.jpeg`, `Palm.jpeg`

**Gallery**
`Front.jpeg`, `Dan.jpeg`, `All.jpeg`, `Bar.jpeg`, `Bar2.jpeg`, `Night.jpeg`, `Roof.jpeg`

> ⚠️ Note: The gallery section's lightbox `onclick` handlers currently reference placeholder tokens (`{{GAL1_IMG}}`, `{{GAL2_IMG}}`, `{{AFANG_IMG}}`, etc.) instead of real file paths. These need to be replaced with actual image URLs/paths before the lightbox will work — see **Known Issues** below.

## Known Issues / TODO

- [ ] **Gallery lightbox placeholders**: `onclick="openLightbox('{{GAL1_IMG}}')"` and similar template tokens throughout the gallery grid are unresolved — swap these for real image paths (likely the same files already used in each `<img src>`, or higher-res versions).
- [ ] Forms (Reservation, Contact, Order) currently simulate submission with a toast notification only — no backend or email service (e.g. EmailJS) is wired up yet.
- [ ] Consider adding real social media links (Instagram, Facebook, WhatsApp are currently `href="#"`).

## Setup / Deployment

1. Place `index.html` and all image assets listed above in the same folder.
2. Open `index.html` directly in a browser, or upload the folder to any static host (Netlify, Vercel, GitHub Pages, cPanel, etc.).
3. No build step, dependencies, or server-side code required.

## Contact Info (as listed on site)

- **Address:** Airport Road, Benin City, Edo State, Nigeria
- **Phone / WhatsApp:** +234 704 943 7888
- **Email:** roycemahmud@gmail.com
- **Hours:** Daily, 10:00am – 10:00pm

---
*Design system: bronze (#b98a46), coral (#7a2331), ivory (#f2e8d6), palm green (#4c5e37) — reflecting Edo/Benin heritage motifs.*
