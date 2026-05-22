# Blog Guide — How to Add Posts

## Quick Steps (3 minutes)

### 1. Write your post as a Markdown file

Create a `.md` file in `blog/posts/`. Example: `blog/posts/my-new-post.md`

```markdown
# Your Post Title

Your first paragraph here. This is the introduction.

## A Subheading

More content. You can use **bold**, *italic*, and [links](https://example.com).

> This is a quote block — great for Quran/Hadith references.

- Bullet point one
- Bullet point two

---

*A closing thought in italics.*
```

### 2. Add it to `blog/posts.json`

Open `blog/posts.json` and add your post to the array:

```json
[
  {
    "slug": "my-new-post",
    "title": "My New Post Title",
    "titleUr": "میری نئی پوسٹ کا عنوان",
    "date": "2026-06-01",
    "excerpt": "A brief 1-2 sentence summary shown on the blog listing.",
    "excerptUr": "بلاگ لسٹنگ پر دکھایا گیا مختصر خلاصہ۔",
    "author": "Unlearn to Return",
    "lang": "en"
  },
  ...existing posts...
]
```

**Important:** The `slug` must match the filename (without `.md`).

### 3. Push to GitHub

```bash
git add blog/posts/my-new-post.md blog/posts.json
git commit -m "blog: add new post - My New Post Title"
git push origin main
```

The post will be live at `unlearntoreturn.com/blog/post.html?slug=my-new-post` within 60 seconds.

## File Structure

```
blog/
├── index.html        # Blog listing page (don't edit unless changing layout)
├── post.html         # Single post reader (don't edit unless changing layout)
├── posts.json        # Post manifest — add entries here for each new post
└── posts/
    ├── why-we-unlearn.md    # Sample post
    └── your-new-post.md     # Your posts go here
```

## posts.json Fields

| Field | Required | Description |
|-------|----------|-------------|
| `slug` | Yes | URL-safe name, must match filename (e.g., `"my-post"` → `my-post.md`) |
| `title` | Yes | English title |
| `titleUr` | No | Urdu title (shown when site is in Urdu mode) |
| `date` | Yes | Publication date in `YYYY-MM-DD` format |
| `excerpt` | Yes | English summary (1-2 sentences, shown on listing page) |
| `excerptUr` | No | Urdu summary |
| `author` | Yes | Author name |
| `lang` | No | Primary language (`"en"` or `"ur"`, defaults to `"en"`) |

## Markdown Formatting Reference

| What you write | What it becomes |
|---------------|-----------------|
| `# Heading` | Large heading |
| `## Subheading` | Section heading (appears in gold) |
| `**bold text**` | **bold text** |
| `*italic text*` | *italic text* |
| `[link text](url)` | Clickable link |
| `> quote text` | Quote block (great for ayat/hadith) |
| `- item` | Bullet list |
| `1. item` | Numbered list |
| `---` | Horizontal divider |
| `![alt](image-url)` | Image |

## Tips

- **Post order:** Posts are automatically sorted by date (newest first)
- **Bilingual:** Add `titleUr` and `excerptUr` for Urdu translations on the listing page. The post content itself is in one language.
- **Images in posts:** Put images in `blog/images/` and reference them as `![description](images/photo.jpg)`
- **Drafts:** Don't add the entry to `posts.json` until you're ready to publish
- **Deleting a post:** Remove its entry from `posts.json` and optionally delete the `.md` file
