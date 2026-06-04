# Interaction Experiments

The interactions worth pulling out of my shipped work — collected on one **studies page** that embeds each one **live** (iframed straight from its GitHub Pages deploy), not as screenshots. Hover, scroll, and drag them in place.

**Live studies page:** https://lobzyjay.github.io/interaction-experiments/

Highlight red (`#e40202`) is sampled from [artbyade.com](https://artbyade.com).

## Studies

| # | Study | Interaction | Live |
|---|-------|-------------|------|
| 01 | **Apex Footer** | Blob tags float in one-by-one + un-strike on hover; orchestrated scroll-in intro; cursor-tracking hand | [self-built](./apex-footer/) |
| 02 | **Systemspec — Reactive Atmosphere** | Canvas Braille dot-field with a cursor forcefield (push + spring-back); same engine on the parchment hero and the espresso footer | [open](https://lobzyjay.github.io/Systemspec-website-redesign/) |
| 03 | **AGMB — Scroll Reveals** | GSAP ScrollTrigger line-by-line heading cascades, bidirectional on scroll | [open](https://lobzyjay.github.io/agmb-website/) |
| 04 | **AGMB — Building Trace Viz** | Self-drawing canvas line-trace over a building photo, parallaxing slower than scroll | [open](https://lobzyjay.github.io/agmb-website/agmb-apply.html) |
| 05 | **Voltex — Hero** | Three.js WebGL hero scene + HUD + Lenis smooth scroll | [open](https://lobzyjay.github.io/Voltex/) |
| 06 | **Pacific Blue — Wind Turbine** | Three.js GLB turbine, scroll-driven camera orbit, sticky content phases | [open](https://lobzyjay.github.io/Pacific-blue/#gen-section) |

## How it works

The studies page (`index.html`) is a clean card list. Each study **opens its live deploy in a new tab** — no inline embeds, so nothing heavy loads until you choose to. Apex Footer (study 01) is the one self-built page in this repo (`/apex-footer`); the rest open their source projects directly on GitHub Pages.

## Running locally

```bash
cd interaction-experiments
python3 -m http.server 8000
# open http://localhost:8000
```

## Adding a study

Add an `<li><a class="study" href="…">` block to `index.html` (number, title, source, description, tags) and a row to the table above. No build step.
