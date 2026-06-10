# Unlearn to Return

A women-only Quran and Hadith learning program website — bilingual (English / اردو), dark theme with gold accents.

**Live:** https://unlearntoreturn.com
**Repo:** https://github.com/waqarsheikh07/unlearntoreturn

---

## Quick Start

No build tools needed. Just open `index.html` in a browser.

To deploy changes: edit → commit → push to `main` → live in ~60 seconds via GitHub Pages.

```bash
git add .
git commit -m "your change description"
git push origin main
```

## Tech Stack

| Component | Details |
|-----------|---------|
| Site | Single-file HTML (`index.html`) — no framework, no build step |
| Styling | Inline CSS, CSS custom properties, dark theme |
| Fonts | Google Fonts — Inter (EN), Noto Nastaliq Urdu (UR) |
| Hosting | GitHub Pages (from `main` branch) |
| Domain | `unlearntoreturn.com` (Hostinger DNS → GitHub Pages) |
| Email | FormSubmit.co → `contact@unlearntoreturn.com` → `durreshehwar411@gmail.com` |
| Tracking | Meta Pixel (ID: `1303676877923844`) |
| Blog | Markdown-based, client-side rendered with Marked.js |

## Project Structure

```
├── index.html              # Main site (all HTML, CSS, JS in one file)
├── thank-you.html          # Post-submission page with Meta Lead event
├── CNAME                   # Custom domain config for GitHub Pages
├── images/
│   ├── logo.png            # Brand logo (528x65)
│   ├── teacher.jpg         # Teacher portrait (600x600)
│   ├── teacher-sm.jpg      # Teacher portrait mobile (300x300)
│   ├── favicon-32.png      # Browser tab icon
│   ├── favicon-192.png     # Android/PWA icon
│   └── apple-touch-icon.png # iOS icon
├── blog/
│   ├── index.html          # Blog listing page
│   ├── post.html           # Single post reader (renders Markdown)
│   ├── posts.json          # Post manifest (add entries here)
│   └── posts/              # Markdown blog posts
│       └── why-we-unlearn.md
└── docs/
    ├── PROJECT-OVERVIEW.md # Tech stack, features, design tokens
    ├── DEPLOYMENT.md       # GitHub Pages, DNS, SSL, email forwarding
    ├── CONTENT-GUIDE.md    # How to update text, images, styles
    ├── BLOG-GUIDE.md       # How to add new blog posts
    └── CHANGELOG.md        # Full history of every change
```

## Key Features

- **Bilingual** — Full EN/UR with RTL layout, language toggle, localStorage persistence
- **Application form** — Email field, 200-word qualifying essays, handpicked selection
- **Blog system** — Write `.md` files, add to `posts.json`, push — live in 60 seconds
- **Meta Pixel tracking** — PageView on all pages, Lead event on thank-you page
- **Email delivery** — Form submissions sent to email via FormSubmit.co (free, unlimited)
- **Responsive** — Mobile-first, breakpoints at 600/768/1024px

## Application Flow

1. Applicant fills out form (name, email, city, age, 200-word essay, fee question)
2. On submit → Meta Pixel fires `Lead` event → data sent to email → redirect to thank-you page
3. Thank-you page fires another `Lead` event, tells applicant candidates are handpicked
4. Team reviews applications at `contact@unlearntoreturn.com` (forwards to `durreshehwar411@gmail.com`)
5. Selected candidates are informed via email

## How to Add a Blog Post

1. Create `blog/posts/your-slug.md`
2. Add entry to `blog/posts.json`:
   ```json
   {
     "slug": "your-slug",
     "title": "Your Title",
     "titleUr": "اردو عنوان",
     "date": "2026-06-01",
     "excerpt": "Brief summary for the listing page.",
     "excerptUr": "اردو خلاصہ",
     "author": "Unlearn to Return"
   }
   ```
3. `git add . && git commit -m "blog: Your Title" && git push origin main`

Full guide: [`docs/BLOG-GUIDE.md`](docs/BLOG-GUIDE.md)

## DNS & Hosting

- **Domain:** `unlearntoreturn.com` (registered at Hostinger)
- **DNS A records:** `185.199.108-111.153` (GitHub Pages IPs)
- **CNAME:** `www` → `waqarsheikh07.github.io`
- **SSL:** Auto-provisioned by GitHub (Let's Encrypt), HTTPS enforced
- **Email forwarding:** `contact@unlearntoreturn.com` → `durreshehwar411@gmail.com` (Hostinger)

Full guide: [`docs/DEPLOYMENT.md`](docs/DEPLOYMENT.md)

## Design Tokens

```
--bg:       #0A0A0A   (page background)
--surface:  #111111   (card background)
--text:     #F5F1EA   (primary text)
--text-muted: #9A9A9A (secondary text)
--accent:   #C9A961   (gold — buttons, highlights)
```

## Documentation

| File | What it covers |
|------|---------------|
| [`docs/PROJECT-OVERVIEW.md`](docs/PROJECT-OVERVIEW.md) | Tech stack, features, contacts, design theme |
| [`docs/DEPLOYMENT.md`](docs/DEPLOYMENT.md) | GitHub Pages, DNS records, SSL, email forwarding, Meta setup |
| [`docs/CONTENT-GUIDE.md`](docs/CONTENT-GUIDE.md) | How to update text, images, styles, contact info |
| [`docs/BLOG-GUIDE.md`](docs/BLOG-GUIDE.md) | Step-by-step guide to adding blog posts |
| [`docs/CHANGELOG.md`](docs/CHANGELOG.md) | Full chronological history of every change |

---

## Changelog (Summary)

### 2026-06-10 — Qualifying Filter & Handpicked Selection
- Removed WhatsApp from form submission — email only via FormSubmit.co
- Added 200-word minimum on qualifying essays (live word counter)
- Thank-you page emphasizes handpicked selection, email notification
- Apply section intro updated: "Candidates are handpicked"
- Replaced "intelligent" with "wisdom" in philosophy quote (EN + UR)

### 2026-05-23 — Meta Conversion Tracking & Email Capture
- Added email field to application form
- Integrated FormSubmit.co for email delivery (free, unlimited)
- Created `thank-you.html` with Meta Pixel `Lead` conversion event
- Form flow: validate → fire Lead event → send email → redirect to thank-you page

### 2026-05-22 — Blog, Docs & Form Validation
- Built blog system (Markdown-based, bilingual, client-side rendered)
- Added "Blog" link to nav (EN + UR)
- Created sample post: "Why We Unlearn"
- Added character/word limits and validation to form fields
- Created 5 documentation files in `docs/`
- Meta Pixel tracking code added
- Facebook domain verification
- Hero section spacing tightened
- Contact email updated to `contact@unlearntoreturn.com`
- Domain changed to `unlearntoreturn.com`, HTTPS enforced

### 2026-05-07 — Initial Launch
- Built complete single-page bilingual website
- Full EN/UR content with RTL support
- Dark theme, gold accents, scroll animations
- WhatsApp contact form
- Logo + favicon processing and integration
- Deployed to GitHub Pages with custom domain
- DNS configured at Hostinger

Full changelog: [`docs/CHANGELOG.md`](docs/CHANGELOG.md)
