# VCP-Lab Website

Jekyll-based academic lab website for the **Video Coding and Processing Lab** at Kyung Hee University.

Adapted from the [USLC-Lab template](https://uslc-lab.github.io) (which itself is based on [Allan Lab](https://www.allanlab.org)). Released under the MIT License.

---

## Quick Start (GitHub Pages)

### 1. Fork / create a repository
- Create a new GitHub repository named `your-username.github.io` (for a user site) or any name (for a project site).
- Upload or push all files from this folder into it.

### 2. Enable GitHub Pages
- Go to **Settings → Pages**
- Set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`
- Your site will be live at `https://your-username.github.io`

### 3. Update `_config.yml`
```yaml
url: "https://your-username.github.io"
baseurl: ""   # leave empty for user site; use "/repo-name" for project site
```

---

## Customization Guide

### Content files (edit these first)

| File | What it controls |
|------|-----------------|
| `_data/news.yml` | News items on the homepage |
| `_data/team.yml` | Lab members (name, role, photo) |
| `_data/publist.yml` | Publications list |
| `_config.yml` | Site title, URL, contact email |

### Adding photos
- Put team/professor photos in `images/team/` (e.g. `prof_choi.jpg`)
- Put slider/carousel photos in `images/slider/`
- Replace `carousel-placeholder` divs in `index.html` with `<img>` tags pointing to your photos

### Adding pages
Create a new `.html` file in `_pages/` with front matter:
```yaml
---
layout: default
title: Your Page Title
permalink: /your-page/
---
```
Then add a link to it in `_includes/navbar.html`.

### Changing colors
Edit the CSS variables at the top of `css/main.css`:
```css
:root {
  --navy:   #0d1b2a;   /* navbar, footer background */
  --blue:   #1a56a0;   /* links, accents */
  --accent: #e8392a;   /* red highlights */
}
```

---

## Local Development

```bash
# Install Ruby + Bundler first, then:
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```

---

## License
MIT License — free to use and modify for your own research group.
