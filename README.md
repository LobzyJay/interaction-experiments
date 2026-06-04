# Interaction Experiments

A growing collection of small, self-contained front-end interaction studies — each one a focused exploration of motion, state, and feel. Built to be opened in a browser with no build step.

Every experiment lives in its own folder and ships as a single page. The table below links to the **live demo** (GitHub Pages) and the **source**.

> Live demos are served from GitHub Pages at `https://lobzyjay.github.io/interaction-experiments/<experiment>/`. They go live once the repo is pushed and Pages is enabled (Settings → Pages → Deploy from `main` / root).

## Experiments

| # | Experiment | What it explores | Live | Source |
|---|------------|------------------|------|--------|
| 01 | **Apex Footer** | Staggered blob reveal with overshoot settle · hover jiggle + strikethrough wipe-off · orchestrated scroll-in intro (line-mask heading, spin-in logo, section stagger) · cursor-tracking hand | [▶ Demo](https://lobzyjay.github.io/interaction-experiments/apex-footer/) | [`/apex-footer`](./apex-footer) |

## Stack

Vanilla HTML / CSS / JS — no framework, no bundler. Motion is hardware-accelerated (transform / opacity / clip-path only), gated behind `prefers-reduced-motion` and `(hover: hover)` where appropriate.

## Running locally

```bash
# any static server works, e.g.
cd interaction-experiments
python3 -m http.server 8000
# then open http://localhost:8000  (landing page → pick an experiment)
```

## Adding a new experiment

1. Create a top-level folder (e.g. `magnetic-button/`) with an `index.html`.
2. Add a row to the table above and a card to the landing `index.html`.
3. Commit. Once pushed, it's live at `…/interaction-experiments/<folder>/`.
