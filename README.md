<div align="center">

# ❖ C Y M A T I C A
### Generative Audio Intelligence Engine

![Three.js](https://img.shields.io/badge/Three.js-black?style=for-the-badge&logo=three.js&logoColor=white)
![WebGL](https://img.shields.io/badge/WebGL-2.0-00ffcc?style=for-the-badge&logo=webgl&logoColor=black)
![GLSL](https://img.shields.io/badge/GLSL-Shaders-ff00ff?style=for-the-badge&logo=opengl&logoColor=white)
[![Download](https://img.shields.io/badge/Download-Source_Code-red?style=for-the-badge&logo=github)](https://github.com/aayushmanmk/cymatica/archive/refs/heads/main.zip)

<p align="center">
  <br>
  <strong>A Synaesthetic Dual-Core Visualization System.</strong><br>
  Cymatica extracts audio data in real-time to drive a procedural, living 3D world.
  <br>
</p>

[✨ Features](#-features) •
[🧠 Architecture](#-architecture) •
[🚀 Quick Start](#-quick-start) •
[💾 Download](#-download)

</div>

---

## 📸 Visuals

<table align="center">
  <tr>
    <td align="center"><img src="https://github.com/user-attachments/assets/9ba1a17f-3f08-4ab3-a280-f6f797cbcd2a" width="100%" /></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/facf07c4-15a0-4013-96ba-0e933b10175d" width="100%" /></td>
  </tr>
  <tr>
    <td align="center"><img src="https://github.com/user-attachments/assets/cbd1011c-9872-491a-b48f-e847345d1799" width="100%" /></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/7cc07ab5-14aa-48a4-b0d8-e8400296b341" width="100%" /></td>
  </tr>
</table>

---

## 🔮 The Experience

**Cymatica** leverages the Web Audio API to perform real-time **Dual-Core FFT analysis**. The core visual is a GLSL Vertex Shader that physically displaces the geometry of a mesh based on the bass response, while high-frequency data drives the color palette and particle acceleration of the surrounding starfield.

## ⚡ Features

| Feature | Description |
| :--- | :--- |
| **🏎️ Dual-Core Engine** | Utilizes parallel processing to achieve both **instant rhythmic response** (Zero Latency) and **high-fidelity texture analysis** simultaneously. |
| **🌌 Procedural Shaders** | Custom GLSL code handles vertex displacement using Perlin Noise algorithms directly on the GPU. |
| **✨ Post-Processing** | Features Unreal Engine-style Bloom, Chromatic Aberration, and Glow effects for a neon-cyberpunk aesthetic. |
| **💥 Reactive Physics** | A surrounding debris field that expands, rotates, and shifts color based on track intensity. |
| **📦 Zero Dependencies** | Runs entirely client-side in a single HTML file via CDN imports. No Node.js required. |

---

## 🧠 Architecture

Unlike traditional visualizers that trade speed for detail, Cymatica runs two analysis engines in parallel.

graph LR
    A[Audio Source] --> B{Signal Splitter}
    B -->|Fast Path| C[Rhythm Core]
    B -->|Detail Path| D[Texture Core]
    
    C -->|FFT 512| E[Transient Data]
    D -->|FFT 32k| F[Harmonic Data]
    
    E -->|Drive| G[Physical Physics]
    F -->|Drive| H[Liquid Shader]
    
    G --> I[Composition]
    H --> I
    I --> J((Render Loop))

1.  **Rhythm Core (512 FFT):** Analyzes audio in tiny chunks (~10ms) to detect immediate transients (Kicks/Snares). Drives the *punch*.
2.  **Texture Core (32,768 FFT):** Analyzes audio in massive chunks (~700ms) to capture high-resolution frequency data. Drives the *distortion*.

---

## 🚀 Quick Start

This project requires **no build steps**, **no Node.js**, and **no installation**.

### 1. Download
[**Click here to download the source code (ZIP)**](https://github.com/aayushmanmk/cymatica/archive/refs/heads/main.zip) or clone via terminal:
```bash
git clone https://github.com/aayushmanmk/cymatica.git
```

### 2. Run
Simply double-click one of the HTML files to open it in any modern web browser (Chrome, Firefox, Edge, Safari).

*   `Cymatica.html` — The pure visualizer experience.
*   `Cymatica With Seekbar.html` — Includes UI controls for playback and seeking.

### 3. Initialize
Click the **"Initialize System"** button and upload an audio file.

> [!TIP]
> **Pro Tip:** For the best experience, use a high-quality **FLAC** or **WAV** file with a strong beat. The engine is optimized to visualize the contrast between deep sub-bass and crisp high-hats.

---

## 💻 Technologies

<div align="center">

| **Three.js** | **WebGL 2.0** | **GLSL** | **Web Audio API** |
| :---: | :---: | :---: | :---: |
| 3D Rendering Engine | Graphics API | Shader Language | Signal Processing |

</div>

<br />

<div align="center">
  <p><i>Crafted with code and frequencies.</i></p>
  <sub>Code by <a href="https://github.com/aayushmanmk">aayushmanmk</a></sub>
</div>
