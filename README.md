# BukuKira – Akaun Bisnes Mudah (PWA)

Simple Malay bookkeeping app: record Duit Masuk / Duit Keluar and get automatic year-end
**Penyata Pendapatan** and **Kunci Kira-Kira**. Works offline once installed. All data stays on the user's phone (localStorage).

## Files

| File | Purpose |
|---|---|
| `index.html` | The app |
| `manifest.webmanifest` | Install info (name, icons, colours) |
| `sw.js` | Service worker (offline support) |
| `icons/` | App icons (192, 512, maskable, Apple touch icon, SVG) |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `bukukira`).
2. Upload **all** files and the `icons` folder to the repository root (keep `.nojekyll`).
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. After about a minute your app is live at `https://<username>.github.io/<repository>/`.

All paths are relative, so it works under a repository sub-folder without any changes.

## Install on a phone

- **Android (Chrome):** open the link → tap **Pasang** in the app header (or Chrome menu ⋮ → *Install app*).
- **iPhone / iPad (Safari):** open the link → Share → **Add to Home Screen**.

## Updating the app

After changing any file, edit `VERSION` at the top of `sw.js` (e.g. `bukukira-v2`) and commit.
Users receive the new version the next time they open the app online.

## Notes

- A PWA needs HTTPS. GitHub Pages provides it automatically.
- Data is stored per phone/browser. Clearing browser data or uninstalling removes it, so users should
  export CSV or connect Google Sheets for backups.
- First-time users start with sample data. Set `START_WITH_SAMPLE = false` in `index.html` to start with an empty book.
- Tailwind, Font Awesome, Google Fonts and html2pdf load from CDNs. The service worker caches them after the first
  online visit, so the app then works offline.
