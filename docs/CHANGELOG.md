# Changelog

All notable changes to the Unlearn to Return website.

## 2026-05-22

### Meta Pixel & Domain Verification
- Added Meta Pixel tracking code (ID: `1303676877923844`) to `<head>`
- Added Facebook domain verification meta tag

### Hero Section Fix
- Reduced hero `min-height` from `90vh` to `70vh`
- Changed content alignment from `center` to `flex-end` (less empty space above headline)
- Adjusted padding for tighter layout

### Contact Email Update
- Changed contact email from `hello@unlearntoreturn.online` to `contact@unlearntoreturn.com`
- Updated in: form section, footer, and both EN/UR i18n translations
- Email forwarding: `contact@unlearntoreturn.com` → `durreshehwar411@gmail.com` (configured in Hostinger)

### Domain Change
- Updated `og:url` meta tag from `unlearntoreturn.online` to `unlearntoreturn.com`
- Updated CNAME to `unlearntoreturn.com`
- Enabled HTTPS enforcement on GitHub Pages

### Teacher Image
- Added teacher portrait photo (`images/teacher.jpg`, 600x600, 21KB)
- Added mobile-optimized version (`images/teacher-sm.jpg`, 300x300, 6KB)
- Replaced placeholder in "About the Teacher" section with actual photo

## 2026-05-07

### Initial Launch
- Built complete single-page bilingual website from scratch
- Full English/Urdu content with RTL support
- Language toggle with localStorage persistence
- Dark theme with gold accents (Neon Pop style)
- Scroll-reveal animations using IntersectionObserver
- WhatsApp contact form (pre-fills message and sends to +92 318 4001193)
- Responsive design (mobile-first, breakpoints at 600/768/1024px)
- Google Fonts: Inter (EN) + Noto Nastaliq Urdu (UR)

### Site Structure (sections in order)
1. **Navigation** — Logo, section links, language toggle
2. **Hero** — Headline, subline, CTA buttons
3. **The Approach** — 5 lens cards (Political, Scientific, Psychological, Awareness, Power)
4. **Philosophy** — Program philosophy text
5. **Who This Is For / Who This Is Not For** — Two-column audience section
6. **About the Teacher** — Teacher bio + portrait
7. **The Structure** — Stats grid (duration, format, schedule, cost)
8. **The Waiver** — Intellectual honesty disclaimer
9. **Apply** — Contact form (name, city, why, optional question)
10. **Footer** — Logo, tagline, contact links, language toggle, copyright

### Logo & Favicons
- Processed brand logo from 2048x2048 square → auto-cropped to 528x65 text content
- Generated 3 favicon sizes from UR monogram image:
  - `favicon-32.png` (browser tab)
  - `favicon-192.png` (Android/PWA)
  - `apple-touch-icon.png` (iOS)

### Deployment
- Deployed to GitHub Pages (`waqarsheikh07/unlearntoreturn`)
- Made repository public (required for GitHub Pages free plan)
- Configured custom domain with CNAME file
- Set up DNS A records at Hostinger pointing to GitHub Pages IPs
- SSL certificate auto-provisioned by GitHub/Let's Encrypt

### Domain History
- Started with `unlearntoreturn.online`
- Briefly used `learntounlearn.online`
- Final domain: `unlearntoreturn.com`
