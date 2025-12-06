# CYMATICA | Generative Audio Engine

<div align="center">
  <p><strong>A Dual-Core, Real-Time Audio Visualization Intelligence.</strong></p>
  <p>
    <a href="#-features">Features</a> •
    <a href="#-how-it-works">How It Works</a> •
    <a href="#-quick-start">Quick Start</a> •
    <a href="#-technologies">Technologies</a>
  </p>
</div>

---

## 📸 Screenshots

<img width="2560" height="1440" alt="{EFB941B7-77D8-4BE5-976C-420A1ACFCEAA}" src="https://github.com/user-attachments/assets/9ba1a17f-3f08-4ab3-a280-f6f797cbcd2a" />

<img width="2560" height="1440" alt="{31311E81-0470-4AC8-BF5F-0A6AE26B2A1E}" src="https://github.com/user-attachments/assets/facf07c4-15a0-4013-96ba-0e933b10175d" />

<img width="2560" height="1440" alt="{F53E0D27-D8C1-4A36-BDCB-2E7AC8AFC5DC}" src="https://github.com/user-attachments/assets/cbd1011c-9872-491a-b48f-e847345d1799" />

<img width="2560" height="1440" alt="{78762B01-E06D-414A-B903-B9E7CD22ED12}" src="https://github.com/user-attachments/assets/7cc07ab5-14aa-48a4-b0d8-e8400296b341" />


## 🔮 The Project

**Cymatica** is not just a standard spectrum analyzer; it is a synaesthetic experience. It leverages the Web Audio API to perform real-time **Dual-Core FFT analysis**, extracting frequency data to drive a procedural 3D world.

The core visual is a **GLSL Vertex Shader** that physically displaces the geometry of a mesh based on the bass response, while high-frequency data drives the color palette and particle acceleration of the surrounding starfield.

## ⚡ Features

*   **Dual-Core Audio Engine:** Utilizes parallel processing to achieve both instant rhythmic response and high-fidelity texture analysis simultaneously.
*   **Zero-Latency Physics:** A dedicated high-speed processor captures drum hits instantly, ensuring the visuals never lag behind the beat.
*   **Procedural Shaders:** Custom GLSL code handles vertex displacement using Perlin Noise algorithms directly on the GPU.
*   **Post-Processing Pipeline:** Features Unreal Engine-style Bloom and Glow effects for a neon-cyberpunk aesthetic.
*   **Reactive Particle System:** A surrounding debris field that expands and shifts color based on track intensity.
*   **Zero Dependencies:** Runs entirely client-side in a single HTML file via CDN imports.

## 🧠 How It Works

Unlike traditional visualizers that trade speed for detail, Cymatica runs two analysis engines in parallel:

1.  **Audio Ingestion:** The browser creates an `AudioContext` and splits the source stream into two parallel `AnalyserNodes`.
2.  **Parallel Signal Processing:** 
    *   **Rhythm Core (512 FFT):** Analyzes audio in tiny chunks (~10ms) to detect immediate transients (Kicks/Snares). This data drives the *physical scale* and "punch" of the sphere.
    *   **Texture Core (32,768 FFT):** Analyzes audio in massive chunks (~700ms) to capture high-resolution frequency data. This drives the *surface distortion*, liquid waves, and color shifting.
3.  **Visual Synthesis:** The data from both cores is normalized and passed into the GLSL shader as uniforms (`uBass` vs `uHighs`).
4.  **Render Loop:** Three.js updates the scene and the `EffectComposer` applies the bloom pass before drawing to the canvas.

## 🚀 Quick Start

This project requires no build steps, no Node.js, and no installation.

1.  **Clone the repository** (or download the source):
    ```bash
    git clone https://github.com/aayushmanmk/cymatica.git
    ```
2.  **Open the file:**
    Simply double-click one of the HTML files to open it in any modern web browser (Chrome, Firefox, Edge, Safari).
    *   `Cymatica.html` - The pure visualizer experience.
    *   `Cymatica With Seekbar.html` - Includes UI controls for playback and seeking.
3.  **Initialize:**
    Click the **"Initialize System"** button and select an audio file (MP3, WAV, FLAC).

> **Note:** For the best experience, use a high-quality FLAC or WAV file with a strong beat. The engine is optimized to visualize the contrast between deep sub-bass and crisp high-hats.

## 💻 Technologies

*   **[Three.js](https://threejs.org/)**: 3D Rendering Engine.
*   **WebGL 2.0**: Low-level graphics API.
*   **GLSL**: OpenGL Shading Language for custom materials.
*   **Web Audio API**: For high-fidelity, dual-channel audio processing.

<div align="center">
  <br />
  <p><i>Crafted with code and frequencies.</i></p>
  <p>Code by <a href="https://github.com/aayushmanmk">aayushmanmk</a></p>
</div>



