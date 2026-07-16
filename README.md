# SkyDash

A clean, mobile-first weather dashboard. Type a city, get the current temperature and a five-day forecast strip — powered by [Open-Meteo](https://open-meteo.com/), which is completely keyless: no account, no API key, no tracking.

## How it works

- You type a city name; SkyDash resolves it to coordinates with Open-Meteo's geocoding API (`https://geocoding-api.open-meteo.com/v1/search?name=<city>`).
- It then fetches current conditions plus a 5-day forecast from `https://api.open-meteo.com/v1/forecast`.
- Weather codes are mapped to emoji glyphs inline — no icon fonts, no CDNs, no external JS.
- Your last city is remembered in `localStorage`, so the forecast is waiting for you next launch.

Everything lives in a single `index.html` with inline CSS and JS. The repo root is exactly what GitHub Pages serves.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app — markup, styles, logic |
| `manifest.json` | Shoebox bundle manifest (name, version, entry, icon, repo) |
| `icon.png` | 512×512 app icon |
| `.github/workflows/pages.yml` | Deploys the repo root to GitHub Pages on push to `main` |

## Ideas to make it yours

- Add a °C / °F toggle.
- Show wind speed or humidity from the same forecast call.
- Swap the emoji map for your own glyph set.
- Extend the strip to 7 days (`forecast_days=7`).

## Add to Shoebox
Have the [Shoebox host](https://github.com/shoebox-apps/shoebox) installed? Scan this with your **phone's camera or Google Lens** — Shoebox opens with this app pre-filled, ready to add. No typing, no app store. (Your phone's camera does the scanning; Shoebox never asks for a camera permission.)

![Add to Shoebox](add-qr.png)

Or paste the base URL into Shoebox's **+ → Add**: `https://shoebox-apps.github.io/app-skydash/`

Fork it. Change one thing. Push. Watch your phone.
