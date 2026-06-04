# 01 · Apex Footer

A faithful recreation of an "Apex" fintech footer (mobile + desktop), rebuilt from a Figma frame as a single self-contained page. The centerpiece is a cluster of organic color **blob tags** — built from the original Figma blob silhouettes used as CSS `mask-image`, so each blob is recolored via `background-color`.

**Live:** https://lobzyjay.github.io/interaction-experiments/apex-footer/

## Interactions

- **Staggered blob reveal** — on scroll-into-view the blobs float in one-by-one (`transition-delay` cascade) with a single-overshoot settle curve (`cubic-bezier(0.34, 1.45, 0.5, 1)`) so they feel buoyant, not stamped.
- **Hover: jiggle + un-strike** — each blob jiggles slightly and its strikethrough wipes off (`clip-path` in reading direction) to clean text. Gated behind `(hover: hover) and (pointer: fine)`.
- **Orchestrated intro** — heading reveals line-by-line via an overflow mask, the logo spins in, dividers scale in, and the brand / tagline / link columns stagger up in sequence.
- **Cursor-tracking hand** — the peace-hand beside the heading tilts and parallaxes toward the pointer with a spring-like lerp, easing back to rest when the cursor leaves the window.
- **Responsive** — mobile layout + 5 blobs below 769px; desktop layout + 13 blobs above.
- **Accessible** — full `prefers-reduced-motion` fallback (opacity-only, no jiggle); decorative marks are `aria-hidden`.

## Build notes

- Vanilla HTML/CSS/JS. Motion is `transform` / `opacity` / `clip-path` only.
- Fonts: Phudu (display) · Inter (body) · Manrope (labels), matched to the source frame.
- `assets/` holds the SVGs exported from Figma (hand, logo, divider, three blob silhouettes).

## Credit

Design reference: "30 day build challenge" Apex footer (Figma). This is a learning recreation of that visual + an interaction study layered on top.
