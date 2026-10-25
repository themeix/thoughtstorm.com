# ThoughtStorm Strategic Capital – Jekyll & Tailwind CSS v4

A modern, high-performance static website migrated from WordPress to Jekyll and Tailwind CSS v4, optimized for GitHub Pages hosting with automated GitHub Actions CI/CD.

## Key Features

- **Jekyll 4.4 Static Generation:** Ultra-fast, secure, and maintainable static site generation.
- **Tailwind CSS v4:** Modern utility styling using `@tailwindcss/cli` and custom CSS theme tokens.
- **Identical Visual Design:** Faithfully recreates the original Beaver Builder layout, including:
  - Exact brand typography (`Lato` and `Lora`).
  - Brand color scheme (`#344263` slate gradient, `#23396c` primary blue, `#d5ae65` gold accent).
  - Starburst watermark contact section.
  - Interactive Simple Valuation Model tool.
  - Numbered pagination matching WordPress URL structure (`/page/:num/`, e.g., `/page/26/`).
  - Dynamic client-side search across all posts.
- **Content Management Without Decap CMS:**
  - Site settings and contact details in `_data/settings.yml`.
  - Header and footer menus in `_data/navigation.yml`.
  - Blog posts in `_posts/` formatted in Markdown.
  - Site pages in `_pages/` formatted in Markdown.
- **GitHub Actions Deployment:** Automated compilation of Tailwind CSS v4 and Jekyll deployment to GitHub Pages.

---

## Project Structure

```
thoughtstorm/
├── .github/
│   └── workflows/
│       └── pages.yml          # Automated CI/CD for GitHub Pages
├── _config.yml                # Jekyll site configuration
├── _data/
│   ├── settings.yml           # Global site metadata, contact info, copyright
│   ├── navigation.yml         # Main header navigation & 4-column footer links
│   ├── categories.yml         # Category archive data
│   └── tags.yml               # Tag archive data
├── _includes/
│   ├── head.html              # HTML head, fonts, SEO, meta tags
│   ├── header.html            # Top bar nav & brand logo with gold border
│   ├── navigation.html        # Responsive navigation with dropdowns
│   ├── footer.html            # 4 recent posts, starburst contact bar, directory
│   ├── post-card.html         # Post card component
│   ├── pagination.html        # Numbered pagination component
│   └── sidebar.html           # Search, recent posts, archives dropdown
├── _layouts/
│   ├── default.html           # Master layout with boxed container
│   ├── post.html              # Blog post layout with sidebar
│   ├── page.html              # Standard page layout with sidebar
│   └── archive.html           # Category and tag archive layout
├── _posts/                    # 102 migrated blog posts in Markdown
├── _pages/                    # 14 migrated pages in Markdown
├── assets/
│   ├── css/
│   │   ├── input.css          # Tailwind CSS v4 source file
│   │   └── main.css           # Compiled minified stylesheet
│   └── uploads/               # Migrated media, images, and tools
├── category/                  # Category archive pages
├── tag/                       # Tag archive pages
├── 404.html                   # Custom 404 error page
├── search.html                # Client-side search interface
├── search.json                # Search index generator
├── index.html                 # Paginated blog home page
├── CNAME                      # Custom domain (thoughtstorm.com)
├── robots.txt                 # Search engine directives
├── package.json               # Node.js dependencies (@tailwindcss/cli v4)
└── Gemfile                    # Ruby gems (Jekyll, paginate, sitemap, feed)
```

---

## Local Development

### Prerequisites

- **Ruby** (v3.1+) and Bundler
- **Node.js** (v18+) and npm

### Installation & Build

1. Install Ruby and Node dependencies:
   ```bash
   bundle install
   npm install
   ```

2. Compile Tailwind CSS v4:
   ```bash
   npm run build:css
   ```

3. Build and serve the Jekyll site locally:
   ```bash
   bundle exec jekyll serve
   ```
   Open `http://localhost:4000` in your browser.

---

## Content Editing Guide

### Updating Site Settings & Contact Details
Edit `_data/settings.yml`:
- Site title, description, and tagline
- Author and contact email (`rick@thoughtstorm.com`), phone, address
- Copyright notice and credits

### Updating Menus
Edit `_data/navigation.yml`:
- `main`: Controls the top header navigation and submenus.
- `footer_col1`, `footer_col2`, `footer_col3`, `footer_col4`: Controls the 4 directory columns in the footer.

### Adding or Editing Blog Posts
Create or edit Markdown files in `_posts/` with the filename convention `YYYY-MM-DD-post-slug.md`:
```markdown
---
layout: post
title: "Article Title"
date: "2026-10-25 10:00:00"
slug: article-title
permalink: /article-title/
categories:
  - Strategy
tags:
  - Valuation
  - Advisory
excerpt: "A brief summary of the article."
---

Article content in Markdown...
```

### Adding or Editing Pages
Create or edit Markdown files in `_pages/`:
```markdown
---
layout: page
title: "Page Title"
slug: page-title
permalink: /page-title/
---

Page content in Markdown or HTML...
```

---

## License

Copyright © 2008 – 2026 Rick Colosimo. All Rights Reserved.
