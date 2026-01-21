# ✋ Gesture Controlled 3D Particle Morpher

An interactive **gesture‑controlled 3D particle system** built with **Three.js** and **MediaPipe Hands**. This project uses your **webcam** to track hand movements and gestures, allowing you to rotate, morph, and explode thousands of particles in real time.

---

## 🚀 Features

* 🖐 **Real‑time Hand Tracking** using MediaPipe Hands
* 🌐 **WebGL Rendering** with Three.js
* 🔄 **Smooth Shape Morphing** between:

  * Sphere
  * Heart
  * Saturn (planet + ring)
  * Flower
  * Cube
* 👌 **Pinch Gesture Detection** (Thumb + Index)

  * Controls particle expansion / explosion
* 🎨 **Dynamic Colors** based on shape type
* 🌀 **Smooth Interpolation (LERP)** for fluid animations
* ⚡ **Single‑file Project** (just one `index.html`)

---

## 🧠 How It Works

### Architecture

* **HTML**

  * `<video>` element captures webcam input (hidden/minimized)
  * `<div>` container renders the Three.js scene
  * UI buttons switch particle shapes

* **CSS**

  * Fullscreen canvas layout
  * Glass‑style UI overlay
  * Responsive and minimal design

* **JavaScript**

  * Three.js handles rendering and particles
  * MediaPipe Hands performs real‑time hand landmark detection

---

## 🔬 Core Concepts

### Particle System

* Uses `THREE.BufferGeometry`
* 15,000 particles rendered using `THREE.Points`
* Two buffers are maintained:

  * **Current Positions** – where particles are now
  * **Target Positions** – where particles should morph to

Particles smoothly interpolate (LERP) toward target positions every frame.

---

### Shape Generation (Math‑Driven)

* **Sphere** – Uniform spherical distribution
* **Heart** – Parametric heart equations
* **Saturn** – Combination of a sphere and a tilted ring
* **Flower** – Polar rose equation
* **Cube** – Randomized volumetric cube

Each shape also defines its own color palette.

---

### Gesture Controls

* **Hand Position**

  * Uses the middle‑finger knuckle landmark
  * Rotates the entire particle system

* **Pinch Detection**

  * Measures distance between:

    * Thumb tip (Landmark 4)
    * Index finger tip (Landmark 8)
  * Smaller distance = stronger pinch
  * Stronger pinch = more particle expansion

---

## 🎮 Controls

### Gestures

| Action        | Effect                     |
| ------------- | -------------------------- |
| Move hand     | Rotate particles           |
| Pinch fingers | Expand / explode particles |

### UI Buttons

* Click buttons at the bottom to switch shapes instantly

---

## 🛠️ Installation & Usage

### Requirements

* Modern browser (Chrome / Edge / Firefox)
* Webcam
* Internet connection (for CDN libraries)

### Run Locally

1. Copy the code into a file named:

   ```
   index.html
   ```
2. Open the file in a browser
3. Allow **camera access** when prompted
4. Show your hand to the camera and interact 🎉

> ⚠️ Tip: For best results, use good lighting and keep your hand clearly visible.

---

## 📦 Libraries Used

* **Three.js** – 3D rendering engine
* **MediaPipe Hands** – Real‑time hand tracking
* **WebGL** – GPU‑accelerated graphics

All libraries are loaded via CDN (no build tools required).

---

## 🔮 Future Improvements

* Multiple hand support
* Gesture‑based shape switching
* Audio‑reactive particles
* Mobile optimization
* GPU shaders for advanced effects

---

## 👨‍💻 Author

**Sreyas Nair**
Developer | Web | Creative Coding | Experiments

---

## 📄 License

This project is open‑source and free to use for learning and experimentation.

---

✨ *Move your hand. Shape the universe.*
