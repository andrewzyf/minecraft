# ⛏️ WebCraft — Minecraft in the Browser (Desktop Edition)

A high-performance, single-file voxel game engine inspired by Minecraft, built using pure **HTML5** and **Three.js**. This version features a stable game loop, refined DDA (Digital Differential Analyzer) raycasting, and optimized memory management for extended gameplay sessions.

---

## 🛠️ Key Fixes & Improvements
*   **Raycaster Stability:** Fixed the "look-axis" freeze bug where the game would crash when looking perfectly straight along a cardinal X/Z axis.
*   **Memory Management:** Implemented full `.dispose()` cleanup for all dynamic meshes, particles, and mob entities, preventing VRAM leaks during long sessions.
*   **Robust Inventory System:** Added overflow handling so items are never lost; if your inventory is full, dropped items will correctly spawn at the player's feet.
*   **Fluid Physics:** Items now behave correctly in water/lava, featuring proper buoyancy and drag mechanics rather than falling through the world.
*   **Audio Reliability:** Streamlined the `AudioContext` initiation to ensure procedural sounds trigger correctly after user interaction.
*   **Unified Lifecycle:** Cleaned up death/respawn logic to ensure inventory drops are handled consistently and securely.

---

## 🎮 Desktop Controls

| Key / Input | Action |
| :--- | :--- |
| **`W` / `A` / `S` / `D`** | Move Player |
| **`Mouse`** | Aim / Look (PointerLock) |
| **`Space`** | Jump / Fly (Creative) |
| **`Left-Click`** | Mine / Attack |
| **`Right-Click`** | Place Block / Use Item |
| **`E`** | Inventory |
| **`1` - `9`** | Select Hotbar Item |
| **`Q`** | Drop Held Item |
| **`F3`** | Debug HUD |
| **`Esc`** | Pause / Quit |

---

## 🚀 Deployment Instructions

This game is a single-file application. No build process or server-side dependencies are required.

1. **Save:** Save the provided code as `index.html`.
2. **Run:** Open the file in any modern web browser (Chrome, Firefox, or Edge recommended).
3. **Host:** You can host this file for free on GitHub Pages, Vercel, or Netlify by simply uploading `index.html` to a public repository.

---

## 📦 Core Architecture
*   **Three.js (r128):** Used as the primary WebGL rendering pipeline.
*   **Procedural Generation:** Uses FBM (Fractional Brownian Motion) combined with value noise to generate deterministic, infinite-style terrain from a single seed.
*   **Procedural Audio:** All sound effects are generated in real-time via the Web Audio API (no external `.mp3` or `.wav` files required).

---

## 📄 License
This project is open-source under the **MIT License**. Feel free to modify, expand, or build upon the engine.
