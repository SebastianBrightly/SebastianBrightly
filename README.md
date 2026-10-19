# Sebastian Brightly

A lightweight personal profile and resume supplement, published as a static
site with GitHub Pages.

## Site

The entire site is `index.html`. It uses plain HTML and CSS, with no build
tools, external assets, or server-side dependencies.

## Preview locally

Open `index.html` in a browser, or run a local static server:

```powershell
python -m http.server 8080
```

Then visit <http://localhost:8080>.

## Publish

The GitHub Actions workflow in `.github/workflows/static.yml` deploys the
repository to GitHub Pages whenever changes are pushed to `main`. In the
repository settings, enable Pages and select **GitHub Actions** as the build
and deployment source.

Update the profile, email address, and LinkedIn URL in `index.html` to keep
the public contact details current.
