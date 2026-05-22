# Unlearn to Return — Project Overview

## What Is This?

A single-page bilingual (English/Urdu) website for **Unlearn to Return**, a women-only Quran and Hadith learning program. The site serves as a landing page to explain the program's philosophy, curriculum, and application process.

## Live URL

- **Primary domain:** https://unlearntoreturn.com
- **GitHub repo:** https://github.com/waqarsheikh07/unlearntoreturn

## Tech Stack

| Component | Technology |
|-----------|-----------|
| **Structure** | Single-file HTML (`index.html`) — no build step, no framework |
| **Styling** | Inline CSS with CSS custom properties (dark theme, gold accents) |
| **JavaScript** | Inline vanilla JS — language toggle, scroll animations, form handling |
| **Fonts** | Google Fonts — Inter (English), Noto Nastaliq Urdu (Urdu) |
| **Hosting** | GitHub Pages (from `main` branch) |
| **Domain** | Purchased from Hostinger, DNS pointed to GitHub Pages |
| **Contact form** | Submits via WhatsApp link (no backend needed) |
| **Tracking** | Meta Pixel (Facebook) for analytics |

## Key Features

- **Bilingual support:** Full English/Urdu with RTL layout switching
- **Language toggle:** EN/Urdu buttons in nav and footer, persisted in localStorage
- **Scroll animations:** IntersectionObserver-based reveal animations
- **WhatsApp form:** Contact form builds a pre-filled WhatsApp message
- **Responsive:** Mobile-first design with breakpoints at 600px, 768px, 1024px
- **No dependencies:** Zero npm packages, no build tools, no CDN dependencies (except Google Fonts)

## Design Theme

- **Dark background:** `#0A0A0A` (near black)
- **Surface color:** `#111111` (cards, sections)
- **Text:** `#F5F1EA` (warm off-white)
- **Accent:** `#C9A961` (gold — buttons, highlights, borders)
- **Glass effects:** Subtle `rgba(255,255,255,0.08)` borders for depth

## Contact Information

- **WhatsApp:** +92 318 4001193
- **Email:** contact@unlearntoreturn.com (forwards to durreshehwar411@gmail.com)

## Team

- **Waqar Sheikh** (waqarsheikh07) — developer, GitHub owner
