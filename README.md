# Stovepipe Interactive Website

The landing page for Stovepipe Interactive. It's a plain HTML and CSS site with no build step and no dependencies.

## Files

| Path | What it is |
| --- | --- |
| `site-content/` | Everything that gets published. The files below all live here. |
| `index.html` | The page: the logo and one line of contact text |
| `styles.css` | All styling, including colors and dark mode |
| `stovepipelogo_transbacking.png` | The logo, a PNG with transparency. It scales to fill the window at any aspect ratio. Replace this file to change the logo. |
| `fonts/` | The Londrina Solid font (`.ttf`) and its OFL license |
| `docs/` | Project documentation (not part of the published site) |

## Preview locally

Open `site-content/index.html` in a browser, or run a local server from the `site-content` folder:

```sh
cd site-content
python3 -m http.server
```

Then go to http://localhost:8000.

## Making changes

- **Logo:** replace `site-content/stovepipelogo_transbacking.png`. Use the largest transparent PNG you have, since it gets scaled up to fill the window.
- **Text and contact email:** edit the `<p class="contact">` line in `site-content/index.html`.
- **Colors:** change the tokens at the top of `site-content/styles.css`. Dark mode colors are in the `prefers-color-scheme: dark` block just below.

## Deployment

The site is a static folder, so any static host works. Publish only the `site-content/` folder, not the repo root.

A GitHub Pages workflow is in `.github/workflows/pages.yml`. To turn it on, go to the repo's Settings > Pages and set Source to "GitHub Actions". After that, every push to `main` publishes `site-content/`.

## Documentation

- [Documentation plan](docs/documentation-plan.md)
