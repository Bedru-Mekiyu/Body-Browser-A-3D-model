# Body Browser — 3D Human Body Anatomical Viewer

An interactive web application built with **WebGL** and **Three.js** that renders manipulable, multi-layered 3D anatomical models of the human body directly in the browser without requiring any external plugins.

[![3D WebGL](https://img.shields.io/badge/WebGL-3D-blue.svg)](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
[![Three.js](https://img.shields.io/badge/Three.js-r71-black.svg)](https://threejs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📋 Overview

**Body Browser** is a web-based anatomical exploration application designed to visualize interactive 3D human body models. Users can manipulate, rotate, and inspect complex anatomical layers—from outer skin down to inner muscular and structural layers—providing an engaging tool for learning and anatomical study.

### Demo Video
📹 [Watch Project Demo Video](https://drive.google.com/file/d/0B23R5d_bodtaSjZuMlNDWjV6bGc/view?usp=sharing)

---

## ✨ Key Features

- **Interactive 3D Controls:** Full 360-degree rotation, panning, and zoom capabilities using intuitive orbit controls.
- **Layer & Skin Selection:** Dynamic control panel (`dat.gui`) allowing users to view or toggle individual anatomical layers and skins.
- **Plugin-Free WebGL Rendering:** Harnesses browser-native WebGL technology for hardware-accelerated 3D graphics.
- **Lightweight Mesh Loading:** Utilizes compressed JSON mesh configurations and character skinning loaders for smooth rendering.

---

## 🛠️ Technology Stack

- **Graphics & Rendering:** WebGL, Three.js
- **UI & Controls:** `dat.gui`, Three.js OrbitControls
- **Frontend Core:** JavaScript (ES5), HTML5, CSS
- **Data & Models:** JSON mesh structure (`UCS_config.json`), skinned mesh loaders

---

## 📂 Project Structure

```text
├── index.html                  # Main application entry point
├── js/
│   ├── script.js              # Application logic, WebGL scene setup, & render loop
│   ├── UCSCharacter.js        # Character model loader & skinning engine
│   ├── controls/              # Camera navigation scripts (OrbitControls, etc.)
│   └── libs/                  # Supporting libraries (dat.gui, system, tween)
├── models/
│   └── skinned/               # 3D model assets and skin JSON configuration
├── build/                     # Three.js library builds
├── robots.txt                 # Web crawler rules
└── sitemap.xml                # Site map configuration
```

---

## 🚀 Getting Started

Because the application loads model configuration and assets via `XMLHttpRequest` (XHR), it must be served through a local HTTP server rather than opened directly from the file system (`file://`).

### Option 1: Python HTTP Server (Recommended)

1. Clone the repository:
   ```bash
   git clone https://github.com/Bedru-Mekiyu/Body-Browser-A-3D-model.git
   cd Body-Browser-A-3D-model
   ```

2. Start a local server:
   ```bash
   # Python 3.x
   python3 -m http.server 8000
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:8000
   ```

### Option 2: Node.js / `serve`

```bash
npx serve .
```

---

## 🧪 Development & Testing

- Validate HTML markup and structure using standard HTML linter tools.
- Verify browser compatibility across modern WebGL-compliant web browsers (Chrome, Firefox, Safari, Edge).

---

## 📄 License

This project is available under the open source licensing terms set by the project author.
