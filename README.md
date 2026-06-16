# CubeTimer

A speed cubing timer with a 3D Rubik's cube visualization, built with Three.js.

## Features

- **3D Cube** — Interactive Rubik's cube with WCA-standard sticker colors. Drag to orbit, auto-rotates when idle
- **Scramble Animation** — Generates 20-move WCA-style scrambles and animates each face rotation on the 3D cube
- **Speed Timer** — Standard hold-release timing: hold spacebar, release to start, press to stop
- **Statistics** — Ao5, Ao12, best/worst times, and full time list with session count

## Usage

1. Serve the directory with any HTTP server (importmap requires CORS-compatible serving):

   ```bash
   python -m http.server 8080
   ```

2. Open `http://localhost:8080/timer.html` in a browser.

3. **Hold spacebar** — timer turns blue (ready)
   **Release** — timer starts counting
   **Press spacebar** — timer stops, solve recorded
   **New Scramble** button — generates a fresh scramble

## Controls

| Action | Input |
|---|---|
| Start/stop timer | Spacebar (hold → release → press) |
| Orbit camera | Mouse drag on the 3D cube |
| New scramble | Click "New Scramble" button |

## Dependencies

- [Three.js](https://threejs.org/) r160 — loaded from CDN via importmap
