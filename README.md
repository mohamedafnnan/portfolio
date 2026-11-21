# Afnnan Portfolio

Personal portfolio for **Mohamed Afnnan Veettilayil**: practical engineering systems, robotics, creative work, field notes, and technical storytelling.

Live site: **<https://mohamedafnnan.github.io/portfolio/>**

## Site and repository layout

This is a static GitHub Pages portfolio with no build step. **`index.html`** is the repository-root entry point and contains the complete interactive page, styles, scripts, bundled template, and interactive experiences. **`resume.pdf`** remains at the repository root because the page downloads it directly as `resume.pdf`.

Runtime media is grouped under `assets/` by type:

- `assets/book-covers/` — reading-library covers and source notes.
- `assets/certificates/` — certificate PDFs and the certificate sprite.
- `assets/illustrations/` — the ASCII hero portrait and `ascii-art-source.txt`.
- `assets/images/` — project photography and portfolio images.
- `assets/posters/` — poster artwork.
- `assets/videos/` — project and creative-work video assets.

`docs/reference/teardown-skill.md` is retained technical reference material and is not a runtime site asset. The deployment workflow remains at `.github/workflows/pages.yml` and uploads the repository root to GitHub Pages.

## Local preview

Clone the repository and serve it as a static site:

```bash
git clone https://github.com/mohamedafnnan/portfolio.git
cd portfolio
python3 -m http.server 8000
```

Open <http://localhost:8000> in a browser. Because the site is static, no package installation or compilation is required.

## Deployment

The repository deploys automatically through GitHub Actions and GitHub Pages whenever changes are pushed to `main`. The workflow uploads the repository root as a static Pages artifact and publishes it at the live-site URL above.
