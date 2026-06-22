# CubeTimer

A speed cubing timer with an interactive 3D Rubik's cube visualization, built with Three.js.

```
Hold Space → Release → Solve → Press Space
```

## Live Demo

**https://tabiqzargar.github.io/Cube/**

*Serve locally with any HTTP server — see Setup below.*

## Features

- **3D Cube** — Interactive Rubik's cube rendered with Three.js. WCA-standard sticker colors. Drag to orbit; auto-rotates when idle
- **Scramble Animation** — Generates 20-move WCA-style scrambles. Each move animates as a visible face rotation on the 3D cube
- **Speed Timer** — Standard hold-release timing: hold spacebar (timer turns ready), release to start, press again to stop
- **Statistics** — Live Ao5, Ao12, best/worst times, solve count, and a scrollable time tag list
- **Best/Worst Highlighting** — Best solve highlighted in green, worst in red
- **Responsive** — Works on desktop, tablet, and mobile with dedicated breakpoints and landscape support
- **Monochrome Theme** — Clean black-and-grey design with subtle animated background gradients and glow effects

## Setup

```bash
# Clone or download the project, then serve the directory:
python -m http.server 8080
```

Open **http://localhost:8080** in a browser.

*An HTTP server is required because Three.js is loaded via ES module imports (`importmap`), which need CORS-compatible serving.*

### Requirements

- A modern browser (Chrome, Firefox, Edge, Safari) with WebGL support
- No build tools or package managers needed

## Usage

| Action | Input |
|---|---|
| Ready timer | Hold `Space` |
| Start timer | Release `Space` |
| Stop / record | Press `Space` |
| Orbit camera | Drag on the 3D cube |
| New scramble | Click **New Scramble** button |
| Touch timer | Tap anywhere outside the cube |

The timer flow:

1. **Idle** — scramble displayed, waiting for input
2. **Hold** `Space` — timer glows, shows "Release to start"
3. **Release** — counting begins
4. **Press** `Space` — time recorded, stats updated
5. Auto-resets after 2 seconds with a fresh scramble

## Technology

- [Three.js](https://threejs.org/) r160 — 3D rendering via ES module CDN
- Pure CSS — no frameworks, glass-morphism effects, animated gradients, conic-gradient ring
- Vanilla JavaScript — timer logic, scramble generator, face rotation animation engine

## Project Structure

```
cube/
├── index.html    # Single-page application (HTML + CSS + JS)
└── README.md     # This file
```

The entire application is a single HTML file with embedded styles and scripts.

## Color Reference

| Element | Color |
|---|---|
| Background | `#08080e` |
| Timer (idle) | `#ddd` |
| Timer (ready) | `#ccc` |
| Timer (running) | `#f0f0f0` |
| Timer (stopped) | `#aaa` |
| Best solve | `#9ece6a` (green) |
| Worst solve | `#f7768e` (red) |
| Cube stickers | White, Yellow, Red, Orange, Green, Blue (WCA) |

## License

MIT
