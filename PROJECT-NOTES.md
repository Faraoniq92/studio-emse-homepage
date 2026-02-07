# Studio Emsé — Homepage V2 — Project Notes

**Last updated:** 2026-02-07

---

## Overview

Single-page homepage for **Studio Emsé**, an interior architecture & design studio based in Paris (75014). The site is a marketing landing page showcasing projects, services, and testimonials.

**Owner:** Marie-Camille (architect)
**Domain:** studioemse.com
**Email:** contact@studioemse.com
**Phone:** +33 6 18 28 85 30
**Address:** 60 rue Raymond Losserand, 75014 Paris

---

## Tech Stack

- **Pure HTML/CSS/JS** — Single `index.html` file, no framework
- **Font:** Manrope (Google Fonts)
- **Images:** Hosted on Squarespace CDN (`images.squarespace-cdn.com`)
- **Videos:** Local files (`hero-video.mp4`, `Video_Generation_With_Specific_Adjustments.mp4`)
- **Hosting:** Static — can be deployed anywhere (GitHub Pages, Netlify, Vercel, etc.)

---

## File Structure

```
V2/
├── index.html                                    # Full homepage (HTML + inline CSS + JS)
├── hero-video.mp4                                # Unused hero video (original)
├── Video_Generation_With_Specific_Adjustments.mp4 # Active hero video
├── robots.txt                                    # Crawler directives
├── sitemap.xml                                   # Sitemap for SEO
├── SEO-AUDIT.md                                  # SEO audit report
└── PROJECT-NOTES.md                              # This file
```

---

## Page Sections

1. **Nav** — Fixed, changes on scroll (mix-blend-mode → solid bg). Mobile hamburger menu.
2. **Hero** — Fullscreen video background with overlay, title, subtitle, CTA
3. **Marquee** — Animated text ticker (brand values)
4. **Trust Bar** — 40+ projects, 6 years, 100% sur-mesure
5. **Manifesto** — "Notre approche" section with text + images
6. **Image Trio** — 3-column layout: image / quote / image
7. **Projects Slider** — Horizontal scroll with 7 project cards (Goncourt, Vavin, Bonne Nouvelle, Papillotes, Magenta, Villiers, Boulogne)
8. **Mid-page CTA** — "Un projet similaire ?"
9. **Full Bleed Image** — Bonne Nouvelle project
10. **Services** — 6 cards (Étude de faisabilité, Visite-conseil, Conception, Décoration, Maîtrise d'œuvre, Design sur-mesure)
11. **Image Duo** — 2-column offset images
12. **Studio** — "Le studio" section
13. **Testimonials** — Auto-rotating slider with 6 reviews (5/5 Google)
14. **CTA** — Contact section (email + phone)
15. **Full End Image** — Bonne Nouvelle project
16. **Footer** — Navigation, address, contact, copyright

---

## Design System

| Token | Value |
|-------|-------|
| `--brand` | `#3F0305` (dark red/maroon) |
| `--ink` | `#1A1615` (near-black) |
| `--cream` | `#F6F2EE` |
| `--white` | `#FDFBF9` |
| `--font` | Manrope |
| `--max` | 1200px |
| `--ease` | `cubic-bezier(0.16, 1, 0.3, 1)` |

---

## JS Features

- **Scroll-aware nav** — Toggles `.scrolled` class at 80px
- **Mobile menu** — Toggle open/close with hamburger
- **Project slider** — Arrow-driven horizontal scroll
- **Custom cursor** — Dot + label on `[data-cursor-text]` elements (hidden on mobile)
- **Reveal animations** — IntersectionObserver-based `.r`, `.rs`, `.r-scale`, `.r-blur`
- **Parallax** — `[data-parallax]` elements get scroll-based transform
- **Testimonial slider** — Auto-advance (5s), arrow/dot navigation

---

## External Dependencies

- Google Fonts (Manrope)
- Squarespace CDN (all images — ~15 images)

---

## GitHub Repo

- **Repo:** `Faraoniq92/studio-emse-homepage`
- **Branch:** main
- **Status:** Public

---

## Key Decisions & Notes

- Hero video is `Video_Generation_With_Specific_Adjustments.mp4` (1.7MB), NOT `hero-video.mp4` (1.2MB)
- All CSS is inline in `<head>` (no external stylesheet)
- All JS is inline at bottom of `<body>` (no external scripts)
- Project links point to `/nosprojets/...` paths (Squarespace-style URLs)
- Site language: French (`lang="fr"`)
- Testimonials are from real Google reviews (5/5 rating)
