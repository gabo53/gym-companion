# Gym Companion

Offline-first PWA for a 7-day recomposition plan: workout logger with progressive overload, rest timer,
weekly weigh-in + Ozempic dose log with pace badges, daily meal/water checklist, JSON backup.

Live: https://gabo53.github.io/gym-companion/

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML + CSS + JS, routine and instructions embedded) |
| `sw.js` | Service worker: offline app shell + cached exercise media |
| `manifest.webmanifest`, `icons/` | "Add to Home screen" support |
| `data/routine.json` | The built-in routine (same data embedded in `index.html`; importable from Data tab) |
| `equipment-picker.html` | Earlier equipment-selector tool (reads `exercises.json`) |
| `exercises.json` | Full exercise dataset (not used by the app at runtime) |
| `docs/siteground-cors.htaccess.txt` | CORS headers for the media host |

## Deploy
Settings → Pages → Deploy from a branch → `main` / `(root)`.

## Media
Images/GIFs are loaded from `https://gym-media.zazdelivery.com/{images|videos}/…` and are © Gym visual
(https://gymvisual.com/). They are not stored in this repo. Personal use only unless you hold a licence.

## Data
Everything is stored on the device (IndexedDB). Use **Data → Export JSON** regularly.
Exercise data: hasaneyldrm/exercises-dataset (MIT).
