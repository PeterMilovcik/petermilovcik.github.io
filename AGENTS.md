# Agents

## Project Overview

Personal portfolio website for Peter Miľovčík, hosted on GitHub Pages at `petermilovcik.github.io`.

## Tech Stack

- Static HTML/CSS — no build step, no bundler, no package manager
- [MDB (Material Design Bootstrap)](https://mdbootstrap.com/) 7.3.2 via CDN
- Font Awesome 6 via CDN
- Google Fonts (Roboto) via CDN

## Structure

- `index.html` — Single-page site with all content (carousel, about, projects, blogs, contact)
- `styles.css` — Custom styles layered on top of MDB
- `images/` — Event/conference photos (referenced from carousel in `index.html`)

## Development

- No build or test commands. Open `index.html` in a browser to preview.
- Changes pushed to `main` deploy automatically via GitHub Pages.

## Conventions

- All content lives in `index.html` as a single page with anchor-linked sections (`#about`, `#projects`, `#blogs`, `#contact`).
- Use MDB component classes and `data-mdb-*` attributes for interactive UI (carousel, ripple, etc.).
- External links use `target="_blank"` and `rel="nofollow"`.
- Carousel background images are set via inline `<style>` in the header using `.carousel-item:nth-child(n)` selectors.
- Keep the site lightweight — no JavaScript frameworks, no npm dependencies.

## Adding Content

- **New project**: Add a `<div>` inside `<div class="projects">` in the projects section.
- **New carousel slide**: Add a `.carousel-item` in the carousel inner, a corresponding `nth-child` CSS rule for the background image, and update carousel indicators.
- **New blog link**: Add a `<div>` inside `<div class="blogs">` in the blogs section.
- **New image**: Place in `images/` directory; reference via relative path `images/filename.ext`.
