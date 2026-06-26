# SebastianBrightly Website Snapshot

This repository contains a static snapshot of the SebastianBrightly website, exported from a WordPress-powered site and structured for straightforward hosting on GitHub Pages or any static web server.

## Overview

- Static HTML pages for the main site and service pages
- Theme assets (CSS, JavaScript, images, fonts) under `wp-content/`
- SEO and feed artifacts (sitemaps, RSS/Atom files)
- Preserved URL-style folder structure (for example: `services/index.html`)

## What This Repo Is

This project is useful as:

- A deployable static copy of a business website
- A baseline for performance cleanup and modernization
- A content/reference archive of site pages and assets

## Tech Snapshot

- Exported WordPress page output (HTML)
- Corpiva theme assets
- Frontend libraries bundled in theme/vendor files (AOS, Owl Carousel, Fancybox, etc.)

## Project Structure

```text
.
|- index.html
|- sitemap.xml
|- services/
|  |- index.html
|- blog/
|  |- index.html
|- wp-content/
|  |- themes/corpiva/
|  |- plugins/
|  |- uploads/
|- wp-includes/
```

## Run Locally

Because this is a static site, you can preview it with any local web server.

### Option 1: VS Code Live Server

1. Open the repo in VS Code.
2. Run a Live Server extension on the workspace root.
3. Open `index.html` in the browser.

### Option 2: Python HTTP Server

Run from the repository root:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Notes

- Some pages still reference original absolute URLs and WordPress endpoints.
- Contact forms and dynamic WordPress features will not function without backend services.
- This repository is focused on static presentation and content structure.

## Suggested Next Improvements

- Replace absolute production links with relative/local equivalents
- Optimize large images and remove unused assets
- Add a lightweight build step for minification and link checks
- Add CI for HTML/link validation

## License

No license file is currently included. Add a license if you plan to distribute or accept external contributions.
