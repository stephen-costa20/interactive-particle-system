<p align="center">
  <a href="https://github.com/stephen-costa20/interactive-particle-system/blob/main/LICENSE"><img src="https://img.shields.io/github/license/stephen-costa20/interactive-particle-system?style=for-the-badge" alt="License"></a>
  <a href="https://github.com/stephen-costa20/interactive-particle-system/commits/main"><img src="https://img.shields.io/github/last-commit/stephen-costa20/interactive-particle-system?style=for-the-badge" alt="Last Commit"></a>
  <img src="https://img.shields.io/badge/Built%20With-Three.js-blue?style=for-the-badge" alt="Built with Three.js">
</p>

# ⭐ Interactive Particle System

A single-file, interactive particle visualization built with **Three.js**, **MediaPipe Hands**, and **Tailwind CSS**. The scene renders a high-density particle field that can morph between preset shapes (Heart, Saturn, Flower, DNA Helix, Fireworks) and responds to **real-time hand gestures** using your webcam.

> Designed as a visual/interaction demo: a lightweight, framework-free “AI + GPU” experience you can run locally by opening one HTML file.



## Preview

![Preview](assets/preview.gif)



## Features

### Real-time Hand Tracking (Webcam)
- Uses **MediaPipe Hands** to track **one or two hands** from your webcam.
- Interaction modes:
  - **Two hands:** move hands apart/together to control **expansion**.
  - **One hand:** **pinch (thumb + index)** to influence the effect (mapped to expansion/scatter style control).

### Particle Morphing + Shape Templates
- Renders **thousands of particles** in a Three.js `Points` system.
- Smoothly morphs particle positions between shape presets:
  - ❤️ Heart
  - 🪐 Saturn / ringed sphere
  - 🌸 Flower
  - 🧬 DNA helix
  - 🎆 Fireworks burst
- Morph behavior is controlled by a configurable `morphSpeed` for satisfying “liquid” transitions.

### Gesture-Based Scene Control
- Hand position (centroid) influences **rotation**:
  - Move your hands left/right to rotate horizontally
  - Move up/down to tilt the form
- Expansion is smoothed with a “drag” factor so the motion feels stable instead of twitchy.

### Visual / UI Layer
- Tailwind-powered “glassmorphism” UI panel:
  - Base color picker (updates particles in real time)
  - Shape selection buttons
  - Live expansion readout
- Subtle scene fog and additive blending for a glowing particle aesthetic.

### Single-File / No Build Tools
- Everything lives in one HTML file: easy to share, demo, and iterate.
- Dependencies loaded via CDNs:
  - Tailwind CSS
  - Three.js
  - MediaPipe Hands + camera utils



## Tech Stack

- **Three.js** (WebGL rendering / particles)
- **MediaPipe Hands** (real-time hand tracking)
- **Tailwind CSS** (UI styling)
- **Vanilla JavaScript** (no frameworks)



## Running Locally

### Option A: Open the file directly (quickest)
1. Download or clone the repo
2. Open `index.html` in a modern browser (Chrome recommended)
3. Allow webcam permissions when prompted

### Option B: Run a tiny local server (recommended)
Some browsers restrict camera access on `file://` URLs. If your camera doesn’t start, run a local server:

#### Python
```bash
python -m http.server 8000
```

Then open:
```bash
http://localhost:8000
```
