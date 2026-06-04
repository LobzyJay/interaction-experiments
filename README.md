# Interaction Experiments

The interactions worth pulling out of my shipped work — a **main page** that indexes them, and a single **player page** that opens any one on its own (`player.html?study=<id>`), landing straight on the interaction. Hover, scroll, and drag the real thing.

**Live:** https://lobzyjay.github.io/interaction-experiments/

## Studies

| # | Study | Interaction | Source |
|---|-------|-------------|--------|
| 01 | **Footer Interaction** | Blob tags float in + un-strike on hover (tap on touch); cursor-tracking hand | self-built (`/apex-footer`) |
| 02 | **Hero Atmosphere** | Canvas Braille forcefield — dots flee the cursor | extracted (`/atmosphere-hero`) |
| 03 | **Footer Atmosphere** | Same engine + diagonal wave, espresso surface | extracted (`/atmosphere-footer`) |
| 04 | **Speedometer Mouse Interaction** | Drag the day-scrubber → cost bars + gauge | extracted (`/speedometer`) |
| 05 | **Dithered Tile Viz** | Bayer-dithered silhouettes, cursor displaces the dots | extracted (`/dithered-viz`) |
| 06 | **Wind Turbine** | Three.js GLB turbine, scroll-driven camera orbit | live embed (Pacific-blue) |

## How it works

- **`index.html`** — neutral card list; red is only the hover state on a study title.
- **`player.html?study=<id>`** — a uniform "player" frame. Each study's interactive element is shown scaled-to-contain and centered (never upscaled, never cut). The title is white.
- **Extracted studies** (`/atmosphere-hero`, `/atmosphere-footer`, `/speedometer`, `/dithered-viz`) are self-contained pages — the real markup/physics lifted verbatim from the source repos — so they load instantly and open straight on the interaction. The player crops their `.demo-stage`.
- **Live embed** (Wind Turbine) iframes its deploy in scroll-mode, locked to the turbine section with the site chrome hidden; scroll the stage to drive the orbit.
- **Touch**: finger drags over a crop demo synthesize cursor moves into the demo, so the cursor-driven ones are playable on phones.

Study configs live in the `STUDIES` map inside `player.html`.
