<div align="center">

  <h1 style="font-size: 3rem; letter-spacing: 10px;">🔊 C Y M A T I C A</h1>
  
  <p>
    <strong>A Generative Audio Intelligence Engine running in the browser.</strong>
  </p>

  <p>
    <a href="#-features">Features</a> •
    <a href="#-how-it-works">How It Works</a> •
    <a href="#-quick-start">Quick Start</a> •
    <a href="#-technologies">Tech Stack</a>
  </p>

  ![Three.js](https://img.shields.io/badge/Three.js-WebGL-black?style=for-the-badge&logo=three.js)
  ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?style=for-the-badge&logo=javascript)

  <br />



</div>

<br />

## 📸 Screenshots

<img width="2560" height="1440" alt="{EFB941B7-77D8-4BE5-976C-420A1ACFCEAA}" src="https://github.com/user-attachments/assets/9ba1a17f-3f08-4ab3-a280-f6f797cbcd2a" />

<img width="2560" height="1440" alt="{31311E81-0470-4AC8-BF5F-0A6AE26B2A1E}" src="https://github.com/user-attachments/assets/facf07c4-15a0-4013-96ba-0e933b10175d" />

<img width="2560" height="1440" alt="{F53E0D27-D8C1-4A36-BDCB-2E7AC8AFC5DC}" src="https://github.com/user-attachments/assets/cbd1011c-9872-491a-b48f-e847345d1799" />

<img width="2560" height="1440" alt="{78762B01-E06D-414A-B903-B9E7CD22ED12}" src="https://github.com/user-attachments/assets/7cc07ab5-14aa-48a4-b0d8-e8400296b341" />

## 🔮 The Project

**Cymatica** is not just a standard spectrum analyzer; it is a synaesthetic experience. It leverages the Web Audio API to perform real-time Fast Fourier Transform (FFT) analysis, extracting frequency data to drive a procedural 3D world.

The core visual is a **GLSL Vertex Shader** that physically displaces the geometry of a mesh based on the bass response, while high-frequency data drives the color palette and particle acceleration of the surrounding starfield.

## ⚡ Features

*   **Real-Time Audio Analysis:** Breaks audio into Bass (Kick), Mids (Synth/Vocals), and Highs (Treble) for distinct visual triggers.
*   **Procedural Shaders:** Custom GLSL code handles vertex displacement using Perlin Noise algorithms directly on the GPU.
*   **Post-Processing Pipeline:** Features Unreal Engine-style Bloom and Glow effects for a neon-cyberpunk aesthetic.
*   **Reactive Particle System:** A surrounding debris field that expands and shifts color based on track intensity.
*   **Zero Dependencies:** Runs entirely client-side in a single HTML file via CDN imports.

## 🧠 How It Works

1.  **Audio Ingestion:** The browser creates an `AudioContext` and routes the file stream through an `AnalyserNode`.
2.  **Frequency Binning:** The `getByteFrequencyData` method fills a `Uint8Array` with 4096 frequency bins.
3.  **Signal Processing:** 
    *   *Low Range (20-150Hz):* Drives the "spikes" and physical distortion of the core sphere.
    *   *High Range (2k-15kHz):* Drives the chromatic aberration and particle speed.
4.  **Render Loop:** Three.js updates the scene, passes uniform data to the shaders, and the `EffectComposer` applies the bloom pass before drawing to the canvas.

## 🚀 Quick Start

This project requires no build steps, no Node.js, and no installation.

1.  **Clone the repository** (or download the source):
    ```bash
    git clone https://github.com/aayushmanmk/cymatica.git
    ```
2.  **Open the file:**
    Simply double-click `cymatica.html` to open it in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  **Initialize:**
    Click the **"Initialize System"** button and select an audio file (MP3, WAV, FLAC).

> **Note:** For the best experience, use a track with a strong beat or heavy dynamic range. Also there are two versions, one with the seekbar and the one without the seekbar.

## 💻 Technologies

*   **[Three.js](https://threejs.org/)**: 3D Rendering Engine.
*   **WebGL 2.0**: Low-level graphics API.
*   **GLSL**: OpenGL Shading Language for custom materials.
*   **Web Audio API**: For high-fidelity audio processing.


<div align="center">
  <br />
  <p><i>Crafted with code and frequencies.</i></p>
</div>
