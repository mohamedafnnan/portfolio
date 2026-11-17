# Afnnan Portfolio

Personal portfolio for **Mohamed Afnnan Veettilayil**: practical engineering systems, robotics, creative work, field notes, and technical storytelling.

Live site: **<https://mohamedafnnan.github.io/portfolio/>**

## What is included

The portfolio is a static GitHub Pages site with no build step. The main experience is delivered from `index.html` and includes:

- An interactive Three.js rover experience with missions, checkpoints, map, camera, sound, and mobile controls.
- The DHT11 OT Sentinel two-node environmental-monitor project log, covering the ESP32-WROOM sensor node, UDP measurements, SSD1306 monitor node, USB/TCP commands, and simulated tampering alert.
- Project cards and full logs for the CNC plotter, TracerCon line follower, OLED display animation, and other engineering work.
- A work timeline, wins archive, experience filters, creative work, field notes, certificates, résumé, and contact sections.
- Responsive navigation and compact mobile layouts for the website and interactive 3D sections.
- A clue-based Easter egg checklist that completes through interactions across the site.

## ASCII art

The hero portrait is built from the uploaded ASCII artwork. The PNG is embedded directly in the hero template so it remains reliable on GitHub Pages, including when the page is rendered through the portfolio's bundled template runtime. The original source files are also kept in the repository:

- `ascii-art.png` — rendered ASCII-art portrait.
- `ascii-art.txt` — character-based source artwork.

The hero uses full-image containment rather than aggressive cropping, so the complete portrait remains visible on desktop and mobile screens.

## Repository structure

- `index.html` — the complete interactive portfolio page, including its styles, scripts, bundled template, embedded hero artwork, and interactive experiences.
- `assets/` — project media and certificates used by the site.
- `resume.pdf` — downloadable résumé.
- `ascii-art.png` and `ascii-art.txt` — hero artwork source files.
- `180 students session img 1.jpeg`, `180 students session img 2.jpeg` — supporting portfolio photography.
- `teardown_SKILL.md` — technical illustration guidance retained with the project materials.
- `.github/workflows/pages.yml` — automatic GitHub Pages deployment on pushes to `main`.

Important media includes the TracerCon build and team photos, CNC plotter video and build image, OLED display video, line-follower video, Venom voice-over video, and certificate PDFs.

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
