# ⚡ NEON PULSE — Audio Visualizer

A beat-synced, fullscreen, neon-cyberpunk audio visualizer for your PC — in a **single HTML file** with zero dependencies. Featuring the legendary pixel dance crew: **Artis 🐕, Giedrė, Agnė, Karolina, Emilija, Martynas, Augustas, Ignas, Dovydas and Paulius**, all dancing in sync with the beat.

## 🚀 How to run

1. Open `index.html` in **Chrome or Edge** (just double-click it — no server needed).
2. Click **▶ Capture PC Audio**.
3. In the picker, choose **Entire Screen** (or a browser tab) and tick **“Also share system audio”**.
4. Play music from anywhere on your PC. Press **F** for fullscreen. Enjoy.

No audio handy? Hit **✨ Demo Mode** to see everything running on a synthetic 128 BPM groove, or **🎤 Use Microphone** (works with Stereo Mix / VB-Cable too).

## 🎛 Modes

| Key | Mode | What it does |
|-----|-----------|--------------|
| 1 | BARS | Classic spectrum bars with falling peak caps, reflections and a perspective floor grid |
| 2 | RADIAL | Rotating circular spectrum with an inner waveform ring |
| 3 | WAVEFORM | Triple-layer glowing oscilloscope |
| 4 | PARTICLES | Swirling particle storm around a pulsing bass core |
| 5 | TUNNEL | Infinite neon polygon tunnel flying at you |

## ⌨️ Controls

- **1–5** — switch mode · **M** — cycle modes · **A** — auto-cycle every 30 s
- **F** — fullscreen · **H** — hide UI · **C** — settings panel
- **D** — toggle dancers · **T** — cycle color theme
- Mouse idle 3 s — cursor and UI fade away for a clean look

## ⚙️ Customization (press C)

Themes (Cyberpunk, Synthwave, Matrix, Inferno, Ice, Rainbow), glow intensity, motion trails, particle count, beat sensitivity, screen shake, beat flash, shockwaves, floor grid, scanlines, dancer size, name tags, spotlights. All settings persist in `localStorage`.

## 🕺 The crew

Every dancer is a procedurally generated pixel-art sprite with their own hair, outfit, accent color, spotlight and unique 8-step dance routine — they jump, raise arms and crouch exactly on detected beats. Artis the dog wags his tail to the rhythm and jumps on the drop.

## 🔧 Tech notes

- Web Audio API `AnalyserNode` (FFT 2048) over a `getDisplayMedia` / `getUserMedia` stream.
- Adaptive beat detection: bass-band energy vs. rolling average with sensitivity control; live BPM estimate shown in the HUD.
- Pure Canvas 2D rendering with additive blending, glow, trails and screen shake — no libraries.
