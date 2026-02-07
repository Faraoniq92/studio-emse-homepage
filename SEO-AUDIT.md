# SEO Audit — Studio Emsé Homepage V2

**Date:** 2026-02-07
**URL:** https://www.studioemse.com
**Scope:** Single-page homepage (index.html)

---

## Issues Found & Fixes Applied

### Critical (High Impact)

| # | Issue | Status |
|---|-------|--------|
| 1 | **No meta description** — Search engines had no snippet text | Fixed |
| 2 | **No Open Graph tags** — Social sharing produced blank previews | Fixed |
| 3 | **No Twitter Card tags** — No rich preview on Twitter/X | Fixed |
| 4 | **No canonical URL** — Risk of duplicate content issues | Fixed |
| 5 | **No JSON-LD structured data** — No rich results in Google (LocalBusiness, rating) | Fixed |
| 6 | **No robots.txt** — Crawlers had no directives | Fixed (file created) |
| 7 | **No sitemap.xml** — Crawlers couldn't discover pages efficiently | Fixed (file created) |

### Medium (Moderate Impact)

| # | Issue | Status |
|---|-------|--------|
| 8 | **No favicon** — No brand icon in tabs/bookmarks, hurts trust signals | Fixed |
| 9 | **No theme-color meta** — No branded browser chrome on mobile | Fixed |
| 10 | **Video preload mismatch** — `<link rel="preload">` pointed to `hero-video.mp4` but actual `<video>` uses `Video_Generation_With_Specific_Adjustments.mp4` | Fixed |
| 11 | **No video poster** — White/black flash before video loads (poor LCP) | Fixed |
| 12 | **Copyright year outdated** — Showed 2025 instead of 2026 | Fixed |
| 13 | **Title too generic** — Missing location keyword "Paris" | Fixed |

### Low (Minor Impact)

| # | Issue | Status |
|---|-------|--------|
| 14 | **Testimonial dots missing aria-labels** — Accessibility gap, indirect SEO signal | Fixed |
| 15 | **No keywords meta** — Minor relevance, but added for completeness | Fixed |
| 16 | **No author meta** — Added for brand attribution | Fixed |

---

## What Was Added

### Meta Tags (in `<head>`)
- `<meta name="description">` — 160-char French description with keywords
- `<meta name="keywords">` — Relevant architecture/design keywords
- `<meta name="author">` — "Studio Emsé"
- `<meta name="robots">` — "index, follow"
- `<meta name="theme-color">` — Brand color `#3F0305`
- `<link rel="canonical">` — Points to `https://www.studioemse.com/`

### Open Graph Tags
- `og:type`, `og:title`, `og:description`, `og:url`, `og:site_name`, `og:image`, `og:image:width`, `og:image:height`, `og:locale`

### Twitter Card Tags
- `twitter:card`, `twitter:title`, `twitter:description`, `twitter:image`

### Favicon
- `<link rel="icon">` and `<link rel="apple-touch-icon">` using existing logo from Squarespace CDN

### JSON-LD Structured Data
- **Type:** `LocalBusiness`
- **Includes:** name, description, URL, phone, email, address, geo coordinates, image, price range, aggregate rating (5/5, 6 reviews), opening hours, area served, expertise areas

### Files Created
- `robots.txt` — Allows all crawlers, references sitemap
- `sitemap.xml` — Lists homepage with priority 1.0

---

## Remaining Recommendations (Future)

| Priority | Recommendation |
|----------|---------------|
| High | **Host images locally** — Currently all images load from `images.squarespace-cdn.com`. Hosting locally improves load speed, reduces external dependencies, and allows proper image optimization (WebP/AVIF) |
| High | **Add width/height attributes to images** — Prevents Cumulative Layout Shift (CLS). Every `<img>` should declare dimensions |
| ~~High~~ | ~~**Create a proper favicon.ico + SVG**~~ — Done: `studioemse-favicon.svg` added locally |
| Medium | **Add hreflang tag** — `<link rel="alternate" hreflang="fr" href="...">` since the site is French-only |
| Medium | **Optimize video file** — `Video_Generation_With_Specific_Adjustments.mp4` (1.7MB) could be compressed further. Consider WebM format as fallback |
| Medium | **Add social media links** — The `sameAs` array in JSON-LD is empty; populate with Instagram, LinkedIn, etc. |
| Medium | **Performance: Inline critical CSS** — The full CSS is already inline which is good, but consider splitting above/below-the-fold |
| Low | **Add `fetchpriority="high"` to LCP element** — The hero video or poster image should get high fetch priority |
| Low | **Preconnect to Squarespace CDN** — Add `<link rel="preconnect" href="https://images.squarespace-cdn.com">` |
| Low | **Internal linking** — Project cards link to `/nosprojets/...` paths that need actual pages or redirects |

---

## SEO Score Estimate

| Category | Before | After |
|----------|--------|-------|
| Meta Tags | 1/10 | 9/10 |
| Structured Data | 0/10 | 9/10 |
| Social Sharing | 0/10 | 9/10 |
| Technical SEO | 3/10 | 8/10 |
| Accessibility | 7/10 | 8/10 |
| Content Quality | 8/10 | 8/10 |
| **Overall** | **~3/10** | **~8.5/10** |
