# Brightly IT Static Site

This repository now uses a quick-launch static homepage at `index.html` for immediate availability, while preserving the original WordPress export as a legacy snapshot.

## Current Status

- Live entry point: `index.html` (WordPress-independent)
- Legacy content retained: page folders plus `wp-content/` and `wp-includes/`
- Goal: keep the site usable now, then migrate legacy pages incrementally

## Why This Structure

- The original export depended on WordPress-generated URLs and runtime behavior
- A lightweight static front page avoids broken rendering from missing WP backend features
- Existing pages are still available for content reference and phased cleanup

## Project Layout

```text
.
|- index.html                  # quick-launch static homepage
|- services/
|- contact-us/
|- blog/
|- home/                       # legacy WordPress-exported route set
|- wp-content/                 # legacy theme, plugins, uploads
|- wp-includes/                # legacy WordPress core assets snapshot
|- sitemap.xml
```

## Run Locally

Use any static web server from the repository root.

### PowerShell (Python)

```powershell
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Migration Plan

1. Keep `index.html` as a stable static landing page.
2. Migrate one legacy route at a time to WordPress-independent HTML/CSS.
3. Replace absolute production-domain links with relative paths.
4. Remove unused legacy assets only after route verification.

## Notes

- Dynamic WordPress features (forms, admin AJAX, WP APIs) will not work without backend services.
- This repository is intended for static hosting and progressive cleanup.

## License

No license file is currently included.
