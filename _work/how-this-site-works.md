---
layout: single
title: "Jekyll Site Maintenance Guide"
excerpt: "Step-by-step guide for creating posts, pages, and managing content on a Jekyll/Minimal Mistakes personal site."
author_profile: true
toc: true
toc_label: "Contents"
toc_sticky: true
---

This guide covers creating and managing content on this Jekyll site, which uses the Minimal Mistakes theme. Whether you're adding a new blog post, updating navigation, or troubleshooting build errors, you'll find the steps here.

## Creating Content with Octopress

[Octopress](https://github.com/octopress/octopress) is a Ruby gem that scaffolds Jekyll content with proper file naming and front matter. Install it with `gem install octopress`.

### New Post

```bash
octopress new post "Your Post Title" --dir posts
```

**What it does:** Creates a new file in `_posts/` with the current date and slugified title.

**Output:** `_posts/2025-01-29-your-post-title.md`

**Verify:** Check that the file exists with `ls _posts/`.

### New Page

```bash
octopress new page page-name/
```

**Output:** `page-name/index.md`

### New Draft

```bash
octopress new draft "Draft Title"
```

**Output:** `_drafts/draft-title.md` (no date prefix needed for drafts)

## Working with Drafts

Store unpublished posts in `_drafts/`. Drafts don't require a date in the filename.

Preview drafts locally:

```bash
npm run serve -- --drafts
```

When ready to publish, move the file to `_posts/` and add the date prefix:

```bash
mv _drafts/my-draft.md _posts/2025-01-29-my-draft.md
```

## Front Matter

Every content file needs YAML front matter at the top. Here's a complete post example:

```yaml
---
layout: single
title: "Post Title"
date: 2025-01-29
excerpt: "A brief description for previews and SEO."
categories: [analysis]
tags: [data, visualization]
author_profile: true
toc: true
---
```

**Required fields:** `layout`, `title`

**Recommended fields:** `date`, `excerpt`, `categories`, `tags`

### Feature Images

Add header images to posts and pages:

```yaml
---
header:
  image: /assets/images/cover.png
  teaser: /assets/images/cover-thumbnail.png
  caption: "Photo credit: [Source](https://example.com)"
---
```

### Table of Contents

Enable an auto-generated table of contents for long posts:

```yaml
---
toc: true
toc_label: "On This Page"
toc_sticky: true
---
```

### Schema.org Structured Data

For enhanced SEO, add structured data:

```yaml
---
schema_type: tech-article
schema_about_page:
  type: "Person"
  name: "Name"
  url: "https://example.com"
---
```

## Managing Navigation

Edit `_data/navigation.yml` to add or remove menu items:

```yaml
main:
  - title: "Blog"
    url: /posts/
  - title: "Projects"
    url: /projects/
  - title: "About"
    url: /about/
```

**Verify:** Run `npm run serve` and check the navigation bar.

## Managing Images

Store images in `assets/images/`:

```
assets/images/
├── cover.png           # Header images
├── avatar.jpg          # Profile photo
└── posts/              # Post-specific images
    └── 2025-01-29/
```

**Naming convention:** Use lowercase, hyphens instead of spaces.

**Optimization:** Keep images under 500KB. Use WebP format when possible.

**Reference in posts:**

```markdown
![Alt text](/assets/images/posts/2025-01-29/example.png)
```

## Content Collections

| Collection | Location | Purpose |
|------------|----------|---------|
| Posts | `_posts/` | Blog posts (requires `YYYY-MM-DD-title.md` format) |
| Drafts | `_drafts/` | Unpublished posts (no date prefix) |
| Projects | `_projects/` | Portfolio items |
| Reports | `_reports/` | Technical reports |
| Work | `_work/` | Work-in-progress |

## Local Development

```bash
# Install dependencies (first time only)
bundle install
npm install

# Serve locally with live reload
npm run serve
# Site available at http://localhost:4000

# Serve with drafts visible
npm run serve -- --drafts

# Build for production
npm run build
# Output in _site/
```

## Customization

Colors and fonts are defined in `_sass/_variables.scss`:

| Setting | Value |
|---------|-------|
| Body font | PT Serif |
| Heading font | PT Sans Narrow |
| Accent color | Academic red (`#8b2635`) |

## Testing Before Deploy

Always run the full test suite before pushing:

```bash
npm run test:all
```

This runs build validation, unit tests, end-to-end tests, and performance audits.

## Deployment

The site deploys automatically via GitHub Pages when you push to the `main` branch. GitHub runs `jekyll build` and serves the `_site/` output.

**Verify deployment:** Check [johnskelton.com](https://www.johnskelton.com) after pushing.

## Troubleshooting

| Error | Cause | Fix |
|-------|-------|-----|
| "Liquid syntax error" | Unescaped double braces in content | Wrap in raw/endraw tags |
| "Invalid date" in filename | Wrong filename format | Use `YYYY-MM-DD-title.md` exactly |
| Styles not updating | Cached assets | Delete `_site/` and rebuild: `rm -rf _site && npm run build` |
| "Could not find gem" | Missing Ruby dependencies | Run `bundle install` |
| Port 4000 in use | Another server running | Kill it: `lsof -ti:4000 | xargs kill` |
| Post not appearing | Future date or draft | Check date is today or earlier; ensure file is in `_posts/` |

## Additional Resources

- [Theme Setup Guide - sumedhmjoshi.com](https://www.sumedhmjoshi.com/theme-setup/) - Detailed Minimal Mistakes documentation
- [Minimal Mistakes Documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) - Official theme docs
- [Jekyll Documentation](https://jekyllrb.com/docs/) - Core Jekyll reference
