# Afnnan Portfolio

A self-contained personal portfolio for Mohamed Afnnan Veettilayil, published with GitHub Pages at <https://mohamedafnnan.github.io/portfolio/>.

## Structure

- `index.html` — the complete interactive site, including styles, scripts, embedded fonts, project modals, the rover experience, the OT-SLA simulation, and the DHT11 OT Sentinel teardown log.
- `resume.pdf` — downloadable résumé.
- `assets/` — project media used by the site.
  - `tracercon-build.jpg` — TracerCon robot/build photo.
  - `tracercon-team.jpeg` — TracerCon team photo, shown in Wins.
  - `assets/certificates/` — certificate PDFs linked from the circular Doc Archive.
  - `cnc-plotter.mp4`, `cnc-plotter-build.jpg` — CNC plotter media and project log.
  - `oled-display.mp4`, `line-follower.mp4`, `venom-voiceover.mp4` — project and creative media.

## Project notes

The **DHT11 OT Sentinel** log documents the physical two-node prototype: one ESP32-WROOM sensor node with a DHT11 and one ESP32-WROOM monitor node with an SSD1306 OLED. The report-backed teardown explains the UDP link, TCP/USB terminal, pin assignments, simulated tampering alert, and the prototype’s security limits. It is opened from the project card with **View full project log**, alongside the CNC Plotter log.

The TracerCon team photograph is intentionally placed in **Wins**, while the robot/build photo remains in **Projects**.

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
