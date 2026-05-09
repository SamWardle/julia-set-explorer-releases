# Julia Set Explorer

A real-time, GPU-accelerated interactive Julia set fractal renderer with 26 colour palettes, 6 animation curves, screenshots, and video recording.

> **No installation required.** Just open `index.html` in any modern browser.
> 
---

## Quick start

1. **Download** the latest release zip from the [Releases](../../releases) page
2. **Unzip** anywhere
3. **Open** `index.html` in Chrome, Firefox, Edge, or Safari 15+

That's it — no Python, no installs, no setup.

---

## Features

- **Real-time GPU rendering** — WebGL 2 fragment shader runs entirely on your GPU
- **26 colour palettes** — cycling, linear-sweep, and dark-background styles; cycle with `C` / `X`
- **Two colouring modes** — repeating bands (cycle) or single gradient sweep (linear), toggle with `G`
- **Variable exponent** — explore z^n + c for n = 2–10 with `[` / `]`
- **9 built-in presets** — press `1`–`9` to jump to classic, lightning, rabbit island, and more
- **6 animation curves** — Circle, Ellipse, Figure-8, Spiral, Lissajous, Cardioid
- **Zoom & pan** — scroll wheel to zoom (cursor-centred), left-click drag to pan
- **Touch support** — pinch to zoom, drag to pan on phones and tablets
- **Screenshot export** — saves PNG at current window resolution (`S`)
- **Video recording** — records WebM or MP4 at up to 60 fps directly in the browser (`V`)
- **Adaptive iterations** — auto-tunes quality to the current Julia set (`I`)
- **On-screen controls** — toggle the reference panel with `H`

---

## Controls

| Key / Input | Action |
|---|---|
| `H` | Toggle controls panel |
| `1` – `9` | Load preset |
| Arrow keys | Nudge Julia parameter `c` |
| Ctrl + arrows | Fine nudge |
| Shift + arrows | Coarse nudge |
| `[` / `]` | Decrease / increase exponent (2–10) |
| `=` / `−` | More / fewer iterations (±50) |
| `I` | Toggle adaptive auto-iterations |
| `C` / `X` | Next / previous colour palette |
| `G` | Toggle gradient / cycle colouring mode |
| `A` or `Space` | Toggle animation |
| `M` | Cycle animation mode |
| `,` / `.` | Animation speed down / up |
| `R` | Reset view |
| `S` | Save PNG screenshot |
| `V` | Start / stop video recording |
| Scroll wheel | Zoom (centred on cursor) |
| Left-click drag | Pan |
| Pinch | Zoom (touch) |

---

## Output files

- Screenshots download as `julia_c{re}_{im}_{timestamp}.png`
- Videos download as `julia_c{re}_{im}_{timestamp}.webm` (or `.mp4` in Chrome/Edge)

---

## Palette reference

All 26 palettes in both linear and cycle modes:

![palette preview](palette_preview.png)

### Categories

| Index | Category | Best used with |
|---|---|---|
| 0 – 12 | Cycling-first | Cycle mode (`G`) |
| 13 – 20 | Linear-sweep | Gradient mode (`G`) |
| 21 – 25 | Dark-background | Either mode, high-contrast detail |

---

## Browser requirements

WebGL 2 is required. All of the following work:

- **Chrome / Chromium** 58+ (recommended for MP4 recording)
- **Firefox** 51+
- **Edge** 79+
- **Safari** 15+ (WebM recording)

---

## For developers: Python desktop version

A standalone Python version (`julia.py`) is included for local development and 4K screenshot export.

**Requirements:**
```
pip install glfw moderngl Pillow numpy imageio[ffmpeg]
```

**Run:**
```bash
python julia.py
```

The Python version adds:
- 4K (3840×2160) offscreen screenshot export
- H.264 MP4 video via ffmpeg
- Controls overlay drawn with PIL

**Palette preview utility:**
```bash
python palette_preview.py
```
Regenerates `palette_preview.png` showing all 26 palettes.

---

## Licence

MIT
