# SarkariExamAll

A production-ready Jekyll site for publishing Sarkari job alerts, admit cards, results, answer keys, syllabus updates, admissions, and scholarship notices.

---

## Overview

This project is structured as a content-driven Jekyll website with:

- category archive pages generated automatically
- author pages and search support
- SEO and sitemap support
- Google integration support from a single config file
- newsletter and ad placeholder support

Primary site categories:

- `latest-jobs`
- `admit-card`
- `results`
- `answer-key`
- `syllabus`
- `admission`
- `scholarships`

---

## Project Structure

```text
.
├── _config.yml
├── _data/
│   ├── authors.yml
│   ├── integrations.yml
│   ├── navigation.yml
│   └── settings.yml
├── _includes/
├── _layouts/
├── _pages/
├── _posts/
├── _sass/
├── assets/
├── author/
├── blog/
├── index.html
├── search.json
└── FOLLOW_IT_SETUP.md
```

---

## Local Setup

### Prerequisites

- Ruby 3.0+
- Bundler

### Install

```bash
bundle install
```

### Run Locally

```bash
bundle exec jekyll serve --livereload
```

Local URL:

```text
http://localhost:4000
```

### Production Build

```bash
bundle exec jekyll build
```

---

## Content Management

### Add a New Post

Create a file in `_posts/` using the format:

```text
YYYY-MM-DD-your-post-slug.md
```

Example:

```markdown
---
layout: post
title: "SSC CHSL Recruitment 2025: Notification, Eligibility and Apply Online"
description: "Check SSC CHSL 2025 notification, age limit, eligibility, fee, and important dates."
date: 2025-05-01
last_modified_at: 2025-05-02
categories: [latest-jobs]
tags: [ssc-chsl, recruitment, govt-jobs]
author: editorial
image: https://example.com/image.jpg
image_alt: "SSC CHSL recruitment graphic"
featured: false
toc: true
---

Post content goes here.
```

### Recommended Front Matter

| Field | Purpose |
|---|---|
| `title` | Post title |
| `description` | SEO description and card text |
| `date` | Publish date |
| `last_modified_at` | Update date |
| `categories` | Main category array |
| `tags` | Search/filter tags |
| `author` | Author key from `_data/authors.yml` |
| `image` | Featured image URL |
| `image_alt` | Image alt text |
| `featured` | Show on hero section if `true` |
| `toc` | Show table of contents if `true` |

### Category Pages

Category archive pages are generated automatically by `jekyll-paginate-v2`.

Examples:

- `/category/latest-jobs/`
- `/category/admit-card/`
- `/category/results/`

To edit category descriptions or homepage featured categories, update `_config.yml`.

### Authors

Author data lives in `_data/authors.yml`.

Author archive pages live in `author/`.

Use the author key in post front matter:

```yaml
author: editorial
```

---

## Key Configuration Files

### `_config.yml`

Controls:

- site title, tagline, and description
- canonical domain URL
- permalink structure
- category descriptions
- featured homepage categories
- plugin behavior

Important values already set for this project:

```yaml
title: "SarkariExamAll"
url: "https://www.sarkariexamall.com"
```

### `_data/navigation.yml`

Controls header and footer links.

### `_data/settings.yml`

Controls site-wide display toggles such as:

- newsletter visibility
- breadcrumbs
- share buttons
- related posts
- ad placeholders

### `_data/integrations.yml`

Controls Google service IDs and enable/disable flags.

---

## Search

The site includes client-side search.

- page URL: `/search/`
- data source: `search.json`
- script: `assets/js/search.js`

Search content is generated automatically during build.

---

## Newsletter

Newsletter forms are prepared for Follow.it integration.

See `FOLLOW_IT_SETUP.md` for setup.

The main newsletter-related templates are:

- `_includes/newsletter.html`
- `_includes/sidebar.html`
- `_includes/subscribe_inline.html`

---

## Google Integrations

All Google-related settings are controlled from `_data/integrations.yml`.

Supported integrations include:

- Google Analytics 4
- Google Tag Manager
- Google AdSense
- Search engine verification tags

This keeps tracking and monetization setup in one place.

---

## Ads

Ad placeholders are enabled through `_data/settings.yml`.

To later add real AdSense units, replace placeholder blocks in templates with actual ad code.

Also update `ads.txt` with your real publisher ID when AdSense is approved.

---

## Deployment

### Build Command

```bash
bundle exec jekyll build
```

### Output Directory

```text
_site
```

### Suggested Production Environment Variable

```text
JEKYLL_ENV=production
```

This project can be deployed on:

- Cloudflare Pages
- GitHub Pages
- any static hosting platform that supports Jekyll build output

---

## Site Notes

- Main domain configured as `www.sarkariexamall.com`
- Homepage and demo content have been converted to a Sarkari exam niche
- Sample posts are placeholders and should be replaced with real official updates
- Contact emails and social handles are still placeholders unless updated separately

---

## Verification

Last verified local build command:

```bash
bundle exec jekyll build
```

Build status: successful
