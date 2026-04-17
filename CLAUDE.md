# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static single-page portfolio/resume website for Jutamat Jarusirisakul (Junior Fullstack Developer). The entire site is a single [index.html](index.html) file — no build step, no package manager, no framework.

## Viewing the site

Open [index.html](index.html) directly in a browser, or serve it with any static file server:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Architecture

Single-file HTML with:
- **Tailwind CSS** loaded via CDN (`https://cdn.tailwindcss.com`) — utility classes only, no config file
- **Font Awesome 6.4** loaded via CDN — icon library used throughout
- **Google Fonts (Inter)** loaded via `@import` in the `<style>` block
- All custom CSS lives in a `<style>` block in `<head>` — custom classes: `.hero-gradient`, `.fade-in`, `.card-hover`, `.bounce`, `.screenshot-grid`, `.profile-image`, `.section-spacing`
- No JavaScript (aside from Tailwind's CDN script)

## Images

Screenshot images are stored in [imports/](imports/) and referenced with relative paths (e.g., `imports/login-page.png`). The git status shows the old `img1.png`–`img7.png` files were deleted and replaced with descriptively named files. When adding new screenshots, place them in `imports/` and use descriptive filenames.

## Page sections (in order)

1. Hero — profile photo, name, tagline, CTA buttons, social links
2. Technical Skills — 6 skill category cards
3. Featured Projects — Employee Management System, iSchool System (each with screenshots, tech stack, features, responsibilities, links)
4. Professional Experience — chronological work history
5. Education — bootcamp + university
6. Contact — email, phone, GitHub, LinkedIn

## Key note

`read.txt` in the repo root is an older version of the HTML (the previous state before screenshots were updated). It can be ignored or deleted.
