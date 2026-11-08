# NeuroAR — Interactive Web-Based Augmented Reality for Neuroanatomy

**NeuroAR** is a WebAR application designed to visualize and interact with 3D neuroanatomical modelp directly through a web browser.

The project integrates **Unity WebGL** and **MindAR.js** to provide an augmented reality experience in which users can visualize a 3D anatomical model by pointing their device's camera at a printed image marker.

The application runs on mobile browsers without requiring users to install a dedicated mobile application.

## Project Overview

NeuroAR aims to explore the use of web-based augmented reality as an interactive educational tool for biomedical engineering and neuroanatomy.

By combining image tracking with real-time 3D visualization, the application allows users to examine anatomical structures in an augmented environment.

## Features

- **Image Target Tracking:** Detects and tracks a predefined image marker using MindAR.js.
- **3D Anatomical Visualization:** Displays neuroanatomical models rendered through Unity WebGL.
- **Interactive Model Rotation:** Allows users to rotate the 3D model using touch gestures.
- **Pinch-to-Zoom:** Supports two-finger pinch gestures to adjust model scale.
- **Anatomical Controls:** Provides interface buttons to interact with the displayed anatomical structures.
- **Reset Functionality:** Restores the model to its initial transformation.
- **Browser-Based Experience:** Runs through a web link without requiring a native mobile application.

## Technology Stack

| Technology | Purpose |
|---|---|
| Unity | 3D scene development and model interaction |
| Unity WebGL | Browser-based Unity deployment |
| MindAR.js | Image target detection and tracking |
| A-Frame | Web-based AR scene and camera integration |
| JavaScript | Communication between MindAR.js and Unity |
| HTML5 / CSS3 | Web interface and application layout |

## System Architecture

The application uses a hybrid architecture in which MindAR.js handles image tracking while Unity WebGL renders and manages the 3D anatomical content.

The main workflow is:

1. The browser requests access to the device camera.
2. MindAR.js detects the predefined image target.
3. The tracking system estimates the target's position and orientation.
4. JavaScript transfers tracking information to the Unity WebGL instance.
5. Unity updates the anatomical model according to the received tracking data.
6. Users interact with the model through touch gestures and interface controls.


## Project Structure

```text
NeuroAR/
├── assets/
│   ├── QRMarcador.jpeg
│   └── targets.mind
│
├── UnityBuild/
│   ├── Build/
│   │   ├── mindar-test.data
│   │   ├── mindar-test.framework.js
│   │   ├── mindar-test.loader.js
│   │   └── mindar-test.wasm
│   │
│   ├── StreamingAssets/
│   └── TemplateData/
│
├── index.html
├── README.md
└── .gitignore
```

## Running Locally

To run NeuroAR locally:

1. Clone the repository:

```bash
git clone https://github.com/Miyael-7/NeuroAR.git
```

2. Navigate to the project directory:

```bash
cd NeuroAR
```

3. Start a local HTTP server:

```bash
python -m http.server 8000
```

4. Open the application in your browser:

```text
http://localhost:8000
```

**Important:** Camera access requires a secure browser context. Localhost is supported for development. For access from other devices, use an HTTPS deployment.

## Deployment

The project is intended to be hosted using **GitHub Pages**, providing a public HTTPS URL.

**Live application:** Pending deployment.

## Project Goals

NeuroAR explores the integration of augmented reality, interactive 3D visualization, and biomedical engineering education.

The project demonstrates how browser-based technologies can be combined with real-time 3D engines to create accessible educational experiences.

## Acknowledgments

This project uses the following technologies and tools:

- [Unity](https://unity.com/)
- [MindAR.js](https://hiukim.github.io/mind-ar-js-doc/)
- [A-Frame](https://aframe.io/)

---

**Project:** NeuroAR  
**Development:** Biomedical Engineering / WebAR  
**Repository:** [Miyael-7/NeuroAR](https://github.com/Miyael-7/NeuroAR)
