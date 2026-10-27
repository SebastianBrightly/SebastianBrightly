# Sebastian Brightly

A lightweight personal profile and resume supplement, published as a static
site with GitHub Pages.

## Site

The site uses plain HTML and CSS, with no build tools or server-side
dependencies:

- `index.html`: main profile page
- `contact.html`: web contact form (FormSubmit)
- `thanks.html`: success page after form submission
- `assets/`: local image assets

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

### Custom domain

This site uses `https://brightlyit.com/` as its canonical address. In the
repository's **Settings → Pages**, set `brightlyit.com` as the custom domain
and wait for GitHub to verify the domain and provision its HTTPS certificate.
Enable **Enforce HTTPS** when it becomes available.

At the DNS provider, point the apex (`@`) to GitHub Pages with these A records:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

The matching AAAA records are optional and support IPv6:

```text
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

The root `CNAME` file contains `brightlyit.com`. For this repository's custom
GitHub Actions workflow, GitHub ignores that file, so also enter
`brightlyit.com` in **Settings → Pages → Custom domain** and save it. The file
is useful if you later publish from a branch instead. For
`www.brightlyit.com`, use a CNAME DNS record pointing to
`SebastianBrightly.github.io`.

Update profile text and contact details in `index.html` and `contact.html` to
keep the public information current. If you change the inbox destination, also
update the FormSubmit endpoint (`form action`) in `contact.html`.
