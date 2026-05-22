# How to Update Content

Everything lives in a single file: `index.html`. No build tools required — edit, commit, push.

## Updating Text Content

All text is managed through a JavaScript `i18n` object near the bottom of `index.html` (search for `const i18n`). There are two language blocks:

```javascript
const i18n = {
  en: {
    "hero.headline": "Study the Quran like your mind depends on it.",
    "hero.subline": "A women-only learning circle...",
    // ... all English text
  },
  ur: {
    "hero.headline": "قرآن کا مطالعہ ایسے کریں جیسے آپ کی سوچ اس پر منحصر ہو۔",
    "hero.subline": "...",
    // ... all Urdu text
  }
};
```

### To change text:
1. Find the key in the `i18n` object (e.g., `"hero.headline"`)
2. Update the value in BOTH `en` and `ur` blocks
3. The HTML uses `data-i18n="hero.headline"` attributes to map text to elements

### To add new text:
1. Add the key+value to both `en` and `ur` in the `i18n` object
2. Add `data-i18n="your.key"` to the HTML element

## Updating Images

All images are in the `/images/` folder.

### Current Images

| File | Purpose | Dimensions |
|------|---------|-----------|
| `logo.png` | Brand logo (nav + footer) | 528 x 65 px |
| `teacher.jpg` | Teacher portrait (About section) | 600 x 600 px |
| `teacher-sm.jpg` | Teacher portrait (mobile, unused currently) | 300 x 300 px |
| `favicon-32.png` | Browser tab icon | 32 x 32 px |
| `favicon-192.png` | Android/PWA icon | 192 x 192 px |
| `apple-touch-icon.png` | iOS home screen icon | 180 x 180 px |

### To replace the teacher photo:
1. Resize your new image to 600x600 px (square, JPEG, <50KB ideal)
2. Name it `teacher.jpg`
3. Replace `images/teacher.jpg` in the repo
4. Commit and push

### To add a hero background image:
1. Add your image as `images/hero-bg.jpg` (recommended: 1920x1080, dark/moody, <200KB)
2. In `index.html`, find the `.hero-bg` CSS block
3. Uncomment the `background-image` line:
   ```css
   background-image:url('images/hero-bg.jpg');
   background-size:cover;
   background-position:center;
   ```
4. Commit and push

### To replace the logo:
1. Prepare a PNG with transparent background
2. Auto-crop to content bounds (no excess whitespace)
3. Name it `logo.png` and replace in `images/`
4. The CSS auto-sizes it (32px height mobile, 36px desktop)

### To replace favicons:
1. Start with a square image (512x512+ recommended)
2. Resize to 3 versions:
   - `favicon-32.png` (32x32)
   - `favicon-192.png` (192x192)
   - `apple-touch-icon.png` (180x180)
3. Replace files in `images/`

## Updating Styles

All CSS is inline in `index.html` inside the `<style>` tag. Key design tokens are CSS custom properties in `:root`:

```css
:root {
  --bg: #0A0A0A;          /* Page background */
  --surface: #111111;      /* Card/section background */
  --text: #F5F1EA;         /* Primary text */
  --text-muted: #9A9A9A;   /* Secondary text */
  --accent: #C9A961;       /* Gold accent (buttons, links) */
  --accent-hover: #D9B970; /* Gold hover state */
  --border: rgba(255,255,255,.08);  /* Subtle borders */
}
```

To change the color scheme, update these variables — everything else inherits from them.

## Updating the WhatsApp Number

Search for `923184001193` in `index.html` — it appears in:
1. The form submission JavaScript (builds the `wa.me/` URL)
2. The footer WhatsApp link
3. The "contact directly" link near the form

Replace all occurrences with the new number (use international format without `+`, e.g., `923001234567`).

## Updating the Contact Email

Search for `contact@unlearntoreturn.com` — it appears in:
1. The "contact directly" email link
2. The footer
3. The `i18n` object (both `en` and `ur` blocks)

Replace all occurrences. Also update the Hostinger email forwarding if the underlying email changes.
