# Anjali Beauty Parlour — Website

A single-page site for Anjali Beauty Parlour (ladies-only salon), Chinthal, Balanagar, Hyderabad. Plain HTML/CSS/JS — no build step, so it deploys straight to GitHub Pages.

## Files
```
index.html    → all page content/sections
styles.css    → design system (colors, type, layout, animation)
script.js     → mobile nav toggle + footer year
images/       → your 6 salon photos
```

## 1. Put it on GitHub
```bash
cd anjali-website
git init
git add .
git commit -m "Anjali Beauty Parlour website"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## 2. Turn on GitHub Pages
1. On GitHub, open your repo → **Settings** → **Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Branch: `main`, folder: `/ (root)`. Save.
4. Wait ~1 minute, then your site is live at:
   `https://<your-username>.github.io/<repo-name>/`

If you want it at the root of `<your-username>.github.io` (no repo path), name the repository exactly `<your-username>.github.io`.

## 3. Before you publish — swap in bigger photos
The photos you shared were compressed to ~141px wide (thumbnail-sized), so they'll look soft when displayed large. The layout is built to hide this (small "polaroid" framing, film-strip gallery), but for the sharpest result:
- Re-export or re-photograph each image at least **1200px** on the long edge.
- Keep the same filenames in `/images` (`mural-peacock.jpg`, `bridal-banner.jpg`, `salon-station.jpg`, `wash-shelves.jpg`, `pedicure-spa.jpg`, `storefront-sign.jpg`) and they'll drop in with no code changes.

## 4. Easy edits
- **Services / prices** — edit the `<ul>` lists inside `#services` in `index.html`.
- **Hours / address / phone** — search `index.html` for the `#visit` and footer sections.
- **Colors** — all defined once at the top of `styles.css` under `:root` (`--teal`, `--rose`, `--gold`, `--ivory`, `--ink`).
- **Map** — the embedded map uses a text search query; once you have your exact Google Maps pin, replace the `src` in the `<iframe>` with the "Embed a map" link from Google Maps for pixel-accurate placement.

## Notes
- No backend, no API keys, no dependencies — 100% static, so GitHub Pages is a perfect free host.
- The site is responsive (phone → desktop) and respects `prefers-reduced-motion`.
- Google review count/rating in the hero is pulled from your screenshot (5.0★, 23 reviews) — update it in `index.html` if it changes.