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

  <!-- REPLACE THE LINK BELOW WITH YOUR OWN SCREENSHOT AFTER YOU RUN THE PROJECT -->
  <img src="./screenshot.png" alt="Cymatica Visualizer Demo" width="100%" style="border-radius: 10px; box-shadow: 0 0 20px rgba(0,255,204,0.2);">

</div>

<br />

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
2.  **Frequency Binning:** The `getByteFrequencyData` method fills a `Uint8Array` with 2048 frequency bins.
3.  **Signal Processing:** 
    *   *Low Range (20-150Hz):* Drives the "spikes" and physical distortion of the core sphere.
    *   *High Range (2k-15kHz):* Drives the chromatic aberration and particle speed.
4.  **Render Loop:** Three.js updates the scene, passes uniform data to the shaders, and the `EffectComposer` applies the bloom pass before drawing to the canvas.

## 🚀 Quick Start

This project requires no build steps, no Node.js, and no installation.

1.  **Clone the repository** (or download the source):
    ```bash
    git clone https://github.com/your-username/cymatica.git
    ```
2.  **Open the file:**
    Simply double-click `cymatica.html` to open it in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  **Initialize:**
    Click the **"Initialize System"** button and select an audio file (MP3, WAV, FLAC).

> **Note:** For the best experience, use a track with a strong beat or heavy dynamic range.

## 💻 Technologies

*   **[Three.js](https://threejs.org/)**: 3D Rendering Engine.
*   **WebGL 2.0**: Low-level graphics API.
*   **GLSL**: OpenGL Shading Language for custom materials.
*   **Web Audio API**: For high-fidelity audio processing.

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request



<div align="center">
  <br />
  <p><i>Crafted with code and frequencies.</i></p>
</div>
