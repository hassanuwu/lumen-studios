# Lumen Studio

**Website for Lumen Studio, an AI video ad studio for beauty, wellness and fitness brands.*

Designed and directed by **Muhammad Hassan**. Built with AI-assisted development (Claude).

---

## What it is

A single-page, single-file website with no frameworks and no build step. It is plain HTML, CSS and JavaScript, so it loads fast and deploys anywhere as one `index.html`.

## Engineering highlights

- **Animated outline that travels between sections.** One SVG overlay traces a frame around each section using `pathLength` and dash offsets. The frame then collapses into glass "balls" that glide to the next section and merge through an SVG goo filter (blur plus a color-matrix threshold). The positions are measured live with `getBoundingClientRect`, so the frame follows cards as they move.
- **Scroll-driven, reversible animation.** `IntersectionObserver` with hysteresis (enter at 25%, exit at 8%) plays section animations forward on the way down and backward on the way up. Looping widgets restart on re-entry, and their timers are cleared on exit.
- **Performance tuning.** The site uses native scrolling with no scroll-jacking. The overlay sits in page coordinates and only redraws when the scroll position changes. The site renders at 75% scale on desktops, and the overlay applies the inverse zoom so its lines stay matched to screen pixels.
- **3D CSS.** Phone mockups enter with 3D rotation. The animation uses the individual `translate` and `rotate` properties, so it doesn't fight existing transforms.
- **Interactive pieces.** These include an "idea slot machine" (three reels that ease to a random result), a DM-style contact chat, a notification stack, an editing-timeline "how it works" section, and a live Pakistan-time clock.
- **Accessible and responsive.** The site respects `prefers-reduced-motion`, supports light and dark themes through CSS custom properties, uses keyboard-visible focus states and ARIA labels, and has a mobile layout.
- **Self-contained assets.** Product illustrations are hand-built inline SVG with gradients and highlights, and photos are embedded, so there are no external image requests.

## Tech

HTML5 · CSS3 (custom properties, `color-mix`, grid, 3D transforms) · Vanilla JavaScript · SVG (filters, path animation) · Deployed on Vercel

## Run locally

Open `index.html` in a browser, or use the VS Code **Live Server** extension.

---

© 2026 Lumen Studio · Made with care in Pakistan
