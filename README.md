# Fifty Pucks — 2025–26 NHL Playoff Pool

A single-file, self-contained leaderboard and analytics dashboard for the 50-puck NHL playoff pool.

**Live:** _add your GitHub Pages URL here after deploy_

## What's in it

- **Standings** — live leaderboard, expandable rows showing roster contribution, daily deltas
- **Analytics** — KPIs across the top (pool total, leader gap, pucks alive, pts/puck, wildcard share), stacked contribution chart, points-per-puck ranking, score-over-time, most-owned skaters, alive-vs-eliminated breakdown, NHL team exposure heatmap
- **Team Detail** — per-entry roster breakdown with full player stats, forwards vs defense, puck allocation
- **Compare** — head-to-head between any two entries, with bars showing relative size on every metric plus a shared/unique players breakdown
- **Players, NHL Stats, Projections, Rules** — supporting views

## Running locally

It's one HTML file. Open it in a browser:

```sh
open index.html
```

Or serve it:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying to GitHub Pages

1. Push this folder to a GitHub repo (e.g. as the root, or inside `docs/`).
2. Go to **Settings → Pages**.
3. Source: select your branch (`main`) and folder (`/` or `/docs`).
4. Wait ~1 minute; the site goes live at `https://<username>.github.io/<repo>/`.

The dashboard is entirely client-side — no backend, no build step, no dependencies beyond a CDN load of Chart.js and Google Fonts.

## Customization

Open the **Tweaks** panel (available when the file is hosted through the design tool) to change:

- Accent color (gold, ice, emerald, crimson, violet)
- Theme (Broadcast / Editorial)
- Live ticker on/off + speed

When deployed standalone, edit the `TWEAK_DEFAULTS` block at the top of the `<script>` in `index.html` to lock in your preferred defaults.

## Data

Entry and player data is embedded in the HTML (`window.PUCKS`). To update scores, edit that block — or wire up your own data source and rebuild.
