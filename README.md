# Stovepipe Interactive Website

The landing page for Stovepipe Interactive. It's a plain HTML and CSS site with no build step and no dependencies.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The page: the logo and one line of contact text |
| `styles.css` | All styling, including colors and dark mode |
| `stovepipelogo_transbacking.png` | The logo, a PNG with transparency. It scales to fill the window at any aspect ratio. Replace this file to change the logo. |
| `docs/` | Project documentation (not part of the published site) |

## Preview locally

Open `index.html` in a browser, or run a local server from the project folder:

```sh
python3 -m http.server
```

Then go to http://localhost:8000.

## Making changes

- **Logo:** replace `stovepipelogo_transbacking.png`. Use the largest transparent PNG you have, since it gets scaled up to fill the window.
- **Text and contact email:** edit the `<p class="contact">` line in `index.html`.
- **Colors:** change the tokens at the top of `styles.css`. Dark mode colors are in the `prefers-color-scheme: dark` block just below.

## Deployment

Not set up yet. Any static host works (GitHub Pages, Netlify and similar). Serve only `index.html`, `styles.css` and the logo PNG.

## Documentation

- [Documentation plan](docs/documentation-plan.md)
