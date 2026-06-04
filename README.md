# Interaction Experiments

The interactions worth pulling out of my shipped work — a **main page** that indexes them, and a single **player page** that opens any one on its own, live (`player.html?study=<id>`). Hover, scroll, and drag the real thing.

**Live:** https://lobzyjay.github.io/interaction-experiments/

## Studies

| # | Study | Interaction | Source |
|---|-------|-------------|--------|
| 01 | **Apex Footer** | Blob tags float in one-by-one + un-strike on hover; scroll-in intro; cursor-tracking hand | self-built (`/apex-footer`) |
| 02 | **STSL — Hero Atmosphere** | Canvas Braille forcefield, cursor-aware | Systemspec `/design#sub-hero` |
| 03 | **STSL — Footer Atmosphere** | Same engine, espresso surface, reactive sweep | Systemspec `/design#sub-footer` |
| 04 | **STSL — Speedometer Scroll** | Scroll-driven speedometer needle | artbyade STSL case study |
| 05 | **AGMB — Building Trace Viz** | Self-drawing canvas line-trace + parallax | agmb-website `/agmb-apply` |
| 06 | **Voltex — Hero** | Three.js WebGL hero + HUD + Lenis | Voltex |
| 07 | **Pacific Blue — Wind Turbine** | Three.js GLB, scroll-driven camera orbit | Pacific-blue |

## How it works

- **`index.html`** — the main page: a neutral card list of studies. Each opens the player.
- **`player.html?study=<id>`** — a single blank "player" page that hosts one interaction in a framed stage (modeled on the Systemspec `/design` demo blocks). The interaction title is the only red accent (`#e40202`, sampled from [artbyade.com](https://artbyade.com)). Same-origin studies deep-link to a section via `#hash`; the rest embed their live deploy.
- **`/apex-footer`** — the one self-built interaction in this repo.

Study configs live in the `STUDIES` map inside `player.html`.

## Adding a study

Add an entry to `STUDIES` in `player.html` (`title`, `label`, `caption`, `src`, `srcnote`) and a card to `index.html` linking to `player.html?study=<id>`. No build step.
