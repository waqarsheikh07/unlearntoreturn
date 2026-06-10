# Changelog

All notable changes to the Unlearn to Return website.

## 2026-06-10

### Qualifying Filter & Handpicked Selection
- Removed WhatsApp field from application form
- Removed WhatsApp from form submission flow — email only via FormSubmit.co
- Added **200-word minimum** requirement on "Why do you want to learn?" textarea
- Added **200-word minimum** requirement on "Why are you a worthy learner?" textarea (waiver applicants)
- Live word counter on textareas (green when met, red when insufficient)
- Updated apply section intro: "Candidates are handpicked. Write with depth and sincerity." (EN + UR)
- Updated thank-you page messaging:
  - "Candidates are handpicked"
  - "Not everyone will be accepted"
  - "You will be informed via email"
- Removed WhatsApp references from thank-you page
- Replaced "intelligent" with "wisdom" in philosophy quote (EN: "Islam is for people of wisdom", UR: "اسلام حکمت والوں کے لیے ہے")

## 2026-05-23

### Meta Conversion Tracking & Email Capture
- Added **email field** to application form (required, `type="email"`)
- Integrated **FormSubmit.co** for email delivery (free, unlimited submissions)
- Form submissions now sent to `contact@unlearntoreturn.com` via FormSubmit.co
- Created **`thank-you.html`** — post-submission page with:
  - Meta Pixel `Lead` conversion event (fires on page load)
  - Bilingual content (EN/UR) with same dark theme
  - "What happens next" steps
  - Animated checkmark icon
- Updated form submission flow: validate → fire Meta Lead event → send to FormSubmit.co → redirect to thank-you page
- Updated submit button text: "Send via WhatsApp" → "Submit Application" (EN + UR)
- Form field reordering: Name → Email + WhatsApp → City + Age → Essay → Fee question

## 2026-05-22

### Blog System
- Created `blog/index.html` — blog listing page with post cards
- Created `blog/post.html` — single post reader, renders Markdown with Marked.js
- Created `blog/posts.json` — post manifest file
- Created `blog/posts/why-we-unlearn.md` — sample first blog post
- Added "Blog" link to main site navigation (EN: "Blog", UR: "بلاگ")
- Blog supports bilingual titles and excerpts

### Documentation
- Created `docs/PROJECT-OVERVIEW.md` — tech stack, features, design tokens, contacts
- Created `docs/DEPLOYMENT.md` — GitHub Pages, DNS records, SSL, email forwarding, Meta/Facebook setup
- Created `docs/CONTENT-GUIDE.md` — how to update text, images, styles, WhatsApp number, email
- Created `docs/BLOG-GUIDE.md` — step-by-step guide to adding new blog posts
- Created `docs/CHANGELOG.md` — chronological change history

### Form Validation
- Added character limits: Name (2-60), City (2-40), WhatsApp (10-16)
- Added live character counters on textareas
- Added required field validation with red border on empty submit
- Error clears as user types

### Meta Pixel & Domain Verification
- Added Meta Pixel tracking code (ID: `1303676877923844`) to `<head>`
- Fires `PageView` event on every page load
- Added Facebook domain verification meta tag (`t9r2qm19468fo8h13ieakt9cyo0tr2`)

### Hero Section Fix
- Reduced hero `min-height` from `90vh` to `70vh`
- Changed content alignment from `center` to `flex-end` (less empty space above headline)
- Adjusted padding: `padding-top: 140px`, `padding-bottom: 80px`

### Contact Email Update
- Changed contact email from `hello@unlearntoreturn.online` to `contact@unlearntoreturn.com`
- Updated in: form section, footer, and both EN/UR i18n translations
- Email forwarding configured in Hostinger: `contact@unlearntoreturn.com` → `durreshehwar411@gmail.com`

### Domain Change
- Updated `og:url` meta tag from `unlearntoreturn.online` to `unlearntoreturn.com`
- Updated CNAME file to `unlearntoreturn.com`
- Enabled HTTPS enforcement on GitHub Pages
- SSL certificate provisioned for `unlearntoreturn.com` + `www.unlearntoreturn.com`

### Teacher Image
- Added teacher portrait photo (`images/teacher.jpg`, 600x600, 21KB)
- Added mobile-optimized version (`images/teacher-sm.jpg`, 300x300, 6KB)
- Replaced placeholder "U" icon in "About the Teacher" section with actual photo

## 2026-05-07

### Initial Launch
- Built complete single-page bilingual website from scratch in `index.html`
- Full English/Urdu content with RTL support via `dir="rtl"` and CSS logical properties
- Language toggle (EN/UR) in nav and footer, persisted in localStorage
- Dark theme with gold accents:
  - Background: `#0A0A0A`, Surface: `#111111`
  - Text: `#F5F1EA`, Accent: `#C9A961` (gold)
- Scroll-reveal animations using IntersectionObserver
- WhatsApp contact form (pre-fills message and sends to +92 318 4001193)
- Responsive design (mobile-first, breakpoints at 600/768/1024px)
- Google Fonts: Inter (EN) + Noto Nastaliq Urdu (UR)
- No dependencies, no build tools, no CDN (except Google Fonts)

### Site Structure (sections in order)
1. **Navigation** — Logo, section links (Philosophy, Curriculum, Details, Apply), language toggle
2. **Hero** — Headline, subline, CTA buttons (Apply Now, Read the philosophy)
3. **The Approach** — 5 lens cards (Political, Scientific, Psychological, Awareness, Power)
4. **Philosophy** — Program philosophy text + quote
5. **Who This Is For / Who This Is Not For** — Two-column audience section
6. **About the Teacher** — Teacher bio + portrait photo
7. **The Structure** — Stats grid (duration, format, schedule, cost)
8. **The Waiver** — Intellectual honesty disclaimer for fee waivers
9. **Apply** — Application form with qualifying essays
10. **Footer** — Logo, tagline, contact links, language toggle, copyright

### Logo & Favicons
- Processed brand logo from 2048x2048 square → auto-cropped to 528x65 content bounds using PIL
- Generated 3 favicon sizes from UR monogram image:
  - `favicon-32.png` (32x32, browser tab)
  - `favicon-192.png` (192x192, Android/PWA)
  - `apple-touch-icon.png` (180x180, iOS home screen)

### Deployment
- Deployed to GitHub Pages (`waqarsheikh07/unlearntoreturn`)
- Made repository public (required for GitHub Pages free plan)
- Configured custom domain with CNAME file
- Set up DNS A records at Hostinger pointing to GitHub Pages IPs (185.199.108-111.153)
- SSL certificate auto-provisioned by GitHub/Let's Encrypt

### Domain History
- Started with `unlearntoreturn.online`
- Briefly used `learntounlearn.online`
- Final domain: `unlearntoreturn.com`
