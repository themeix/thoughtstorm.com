# ThoughtStorm Strategic Capital – Jekyll & Tailwind CSS v4 Static Website

A high-performance, maintainable static website migrated from WordPress to **Jekyll** and **Tailwind CSS v4**, deployed automatically to **GitHub Pages** via **GitHub Actions**.

---

## Content Management & Editing Guide

All website content is organized directly in human-readable Markdown and YAML files. You do not need any CMS (such as WordPress or Decap CMS). Content can be edited using any text editor, VS Code, or directly in the browser on GitHub.com.

### 1. Site Metadata, Contact Info & Global Settings
**File:** `_data/settings.yml`

This file controls the global settings used across the site:
- **Title, Tagline & Description:** Used in the header, meta tags, and SEO cards.
- **Contact Details:** Email (`rick@thoughtstorm.com`), phone number, and mailing address.
- **Social Links:** Twitter / X profile URL.
- **Footer Text:** Copyright notice, tagline, and bottom credit line.

*Example:*
```yaml
title: "ThoughtStorm Strategic Capital"
tagline: "Increasing returns on invested capital"
email: "rick@thoughtstorm.com"
phone: "+1 (555) 000-0000"
twitter_url: "https://twitter.com/rickcolosimo"
copyright_year: "2026"
```

---

### 2. Header & Footer Navigation Menus
**File:** `_data/navigation.yml`

#### A. Main Header Menu (`main`)
Controls the top navigation bar links and hover dropdowns:
- Each item has `title` and `url`.
- To create a dropdown menu, add a `sub` list under the parent item:

```yaml
main:
  - title: "Home"
    url: "/"
  - title: "Strategy"
    url: "/strategy/"
    sub:
      - title: "Investment Due Diligence"
        url: "/strategy/investment-due-diligence/"
      - title: "Business Audit"
        url: "/strategy/business-audit/"
  - title: "M & A"
    url: "/mergers-acquisitions/"
    sub:
      - title: "Interim Management"
        url: "/interim-management/"
  - title: "Approach"
    url: "/approach/"
  - title: "Tools"
    url: "/tools/"
    sub:
      - title: "Simple Valuation Model"
        url: "/tools/simple-valuation-model/"
  - title: "About"
    url: "/about/"
    sub:
      - title: "Our Team"
        url: "/about/our-team/"
      - title: "Contact Us"
        url: "/about/contact-us/"
```

#### B. Footer Directory Columns (`footer_col1` through `footer_col4`)
Controls the 4 columns in the footer directory:
```yaml
footer_col1:
  title: "Services"
  links:
    - title: "Due Diligence"
      url: "/strategy/investment-due-diligence/"
    - title: "Business Audit"
      url: "/strategy/business-audit/"
```

---

### 3. Creating & Editing Blog Articles
**Directory:** `_posts/`

Each article is a Markdown file following the naming convention:
`YYYY-MM-DD-article-slug.md` (e.g. `2026-10-25-exit-readiness.md`).

#### Front Matter & Article Template:
```markdown
---
layout: post
title: "Exit Readiness in Uncertain Markets"
date: 2026-10-25 10:00:00 -0400
author: "Rick Colosimo"
permalink: /exit-readiness-in-uncertain-markets/
categories:
  - strategy
tags:
  - deals
  - finance
excerpt: "A concise executive summary of the post shown in feeds and search."
---

Your article body text goes here. Use standard Markdown for formatting:

## Major Section Heading

Write paragraphs naturally with a blank line between each paragraph.

- Bullet item one
- Bullet item two
- Bullet item three

> Blockquotes can be used for key takeaways or notable quotes.

For external links: [Visit Resource](https://example.com)
```

---

### 4. Creating & Editing Static Pages
**Directory:** `_pages/`

Static pages (such as Strategy, Approach, About, Our Team, Tools) live in `_pages/`.

#### Page Template:
```markdown
---
layout: page
title: "Approach"
permalink: /approach/
---

Page content written in Markdown or standard HTML.
```

---

### 5. Media & Image Uploads
**Directory:** `assets/uploads/`

- Save images in `assets/uploads/` (or organized by year/month subdirectories like `assets/uploads/2026/10/`).
- Embed an image inside any Markdown post or page:
  ```markdown
  ![Chart Description]({{ '/assets/uploads/2026/10/valuation-chart.png' | relative_url }})
  ```
- Or using root-relative path:
  ```markdown
  ![Chart Description](/assets/uploads/2026/10/valuation-chart.png)
  ```

---

### 6. Managing Categories, Tags & Archives

- **Categories:** Pages in `category/` (e.g. `category/strategy/index.html`) display all posts belonging to that category.
- **Tags:** Pages in `tag/` (e.g. `tag/deals/index.html`) display posts containing that tag.
- **Month Archives:** Monthly archive files live in `archives/` (e.g. `archives/2008-01.html`). They map directly to `permalink: /2008/01/` to serve past archives without cluttering the project root.

---

## Local Development & Testing

### Prerequisites
- **Ruby** (v3.1+) & Bundler
- **Node.js** (v18+) & npm

### Setup & Run Commands

1. **Install dependencies:**
   ```bash
   npm install
   bundle install
   ```

2. **Compile Tailwind CSS v4:**
   ```bash
   npm run build:css
   ```

3. **Start local development server:**
   ```bash
   bundle exec jekyll serve
   ```
   Open `http://localhost:4000` in your browser.

4. **Production Build Test:**
   ```bash
   npm run build:css
   bundle exec jekyll build
   ```

---

## Deployment to GitHub Pages

Deployment is **100% automated** using GitHub Actions (`.github/workflows/pages.yml`).

Whenever you commit and push changes to the `main` branch, the workflow will automatically:
1. Check out the repository.
2. Install Node.js and compile Tailwind CSS v4.
3. Install Ruby gems and build the Jekyll site.
4. Deploy the production files to GitHub Pages.

### How to Publish Changes:
```bash
git add .
git commit -m "Add new post on exit readiness"
git push origin main
```
The site updates automatically in ~30 seconds.

---

## Custom Domain Configuration

The custom domain `thoughtstorm.com` is defined in the `CNAME` file:
```
thoughtstorm.com
```

DNS settings pointing to GitHub Pages:
- **Apex domain (`thoughtstorm.com`):**
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- **`www` subdomain (`www.thoughtstorm.com`):**
  - CNAME record pointing to `themeix.github.io`
