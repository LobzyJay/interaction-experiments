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

The studies page (`index.html`) is a gallery. Each study is a **click-to-load `<iframe>`** pointing at the live deploy — they share the `lobzyjay.github.io` origin, so framing just works, and nothing loads until you click (six full sites won't boot at once). Apex Footer (study 01) is the one self-built page in this repo (`/apex-footer`); the rest embed their source projects directly.

## Running locally

```bash
cd interaction-experiments
python3 -m http.server 8000
# open http://localhost:8000
```

## Adding a study

Add a `<section class="study">` to `index.html` with a `data-src` (live URL or local path) and a row to the table above. No build step.
