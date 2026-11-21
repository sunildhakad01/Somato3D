# Somato3D ⚕

[![Three.js](https://img.shields.io/badge/Three.js-r187-black?style=for-the-badge&logo=three.dot.js)](https://threejs.org/)
[![Vite](https://img.shields.io/badge/Vite-8.x-646CFF?style=for-the-badge&logo=vite)](https://vite.dev/)
[![WebGL 2.0](https://img.shields.io/badge/WebGL-2.0-990000?style=for-the-badge&logo=webgl)](https://www.khronos.org/webgl/)
[![Model License](https://img.shields.io/badge/Model_License-CC_BY--SA_4.0-lightgrey?style=for-the-badge)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Author](https://img.shields.io/badge/Author-Sunil_Dhakad-blue?style=for-the-badge&logo=github)](https://github.com/sunildhakad01)

> **Somato3D** is an interactive, browser-based 3D human anatomy atlas and biomechanics explorer. Engineered on clinical scan-derived volumetric models, it provides medical students, kinesiology researchers, fitness professionals, and educators with real-time anatomical dissection, 3D tomographic slicing, kinetic exercise-muscle mapping, and workout fatigue analytics.

---

![Somato3D - Complete Anatomy Model](docs/screenshots/all-layers.png)

---

## 🌟 Highlights & Key Features

### 🩻 Clinical-Grade 3D Anatomy Atlas
- **2,500+ Named Anatomical Structures**: Derived from the high-resolution [BodyParts3D](https://dbarchive.biosciencedbc.jp/en/bodyparts3d/) scan dataset via [Z-Anatomy](https://github.com/Z-Anatomy/Models-of-human-anatomy).
- **True Anatomical Symmetry & Differentiation**: Distinguishes left and right contralateral pairs (e.g., *Left short head of biceps brachii* vs. *Right short head*).
- **Curated Clinical Metadata**: Detailed anatomical descriptions, physiological classifications, actions, origins, insertions, and innervating nerves for major muscular structures.

### 🧬 7 Independent Biological Layers
Toggle, isolate, and modulate individual layer opacities via dedicated slider channels:
1. **Integumentary System (Skin)**
2. **Muscular System** (Superficial, deep, and core musculature)
3. **Arterial Vasculature**
4. **Venous Vasculature**
5. **Nervous System** (Central, peripheral, and cranial nerve pathways)
6. **Visceral Organs** (Thoracic, abdominal, and pelvic cavities)
7. **Skeletal System** (Axial and appendicular skeleton)

*Includes one-click anatomical presets: **All Layers**, **Skin**, **Muscles**, **Skeleton**, **Circulation**, **Nervous**, **Organs**, and **X-ray**.*

### 🏋️ Integrated Biomechanics & Exercise Engine
- **876+ Exercise Database**: Curated catalog covering barbell, dumbbell, cable, machine, and bodyweight movements.
- **Dynamic 3D Muscle Activation**: Selecting an exercise immediately renders **Primary Movers** in vivid red-orange and **Secondary Synergists** in yellow, muting unrelated anatomy to neutral gray.
- **Depth Peeling for Obscured Muscles**: Automatically peels back superficial tissues when target muscles (e.g. *erector spinae*, *psoas major*) lie beneath outer layers.
- **Visual Guides**: High-resolution start/end demonstration animations and step-by-step biomechanical execution instructions.

### 📊 Workout Builder & Volumetric Heatmap
- **Session Planning**: Build targeted workout routines with custom sets, repetitions, and exercise ordering.
- **Full-Body Recruitment Heatmap**: Calculates cumulative volumetric workload per muscle group, visualizing fatigue and stimulation on the 3D body from low (yellow) to maximum (deep crimson).
- **Untrained Muscle Detection**: Instantly highlights neglected muscle groups in blue and suggests exercises to balance the training program.

### 📐 Planar Tomography & Cross-Section Slicer
- Real-time planar clipping across standard clinical planes:
  - **Coronal Plane** (Frontal / Dorsal-Ventral)
  - **Sagittal Plane** (Lateral / Left-Right)
  - **Axial Plane** (Transverse / Superior-Inferior)
- Dynamic cut-depth position slider, plane flip toggle (`⇄ Flip`), and solid cap rendering for cut tissues.

### 💥 Exploded Dissection View
- Continuous radial expansion slider separating structures along normal anatomical vectors, maintaining full spatial picking, orientation, and focus in exploded state.

### 🎯 Interactive Quiz & Knowledge Assessment
- Test anatomical recall with targeted spatial challenges ("Find the *flexor carpi radialis*"), layer-specific queries, and exercise recruitment tests ("Which muscle is primarily worked by this movement?"). Includes contextual hints, skipping, streak tracking, and scoring.

### 🔗 Deep-Linking & Spatial State Serialization
- The entire state of Somato3D is synchronized with the URL hash in real time:
  - 3D camera vector & target coordinates
  - Visibility & alpha opacities of all 7 layers
  - Selected, hovered, and isolated structures
  - Tomographic cross-section axes and clipping depths
  - Active exercise or workout configuration
- Share exact anatomical views effortlessly with one click.

---

## 📸 Visual Walkthrough

### Anatomical Systems & Presets

| Integumentary (Skin) | Muscular System |
| :---: | :---: |
| ![Skin](docs/screenshots/skin.png) | ![Muscles](docs/screenshots/muscles.png) |
| **Skeletal Framework** | **Circulatory System** |
| ![Skeleton](docs/screenshots/skeleton.png) | ![Circulation](docs/screenshots/circulation.png) |
| **Nervous Pathways** | **X-Ray Diagnostic View** |
| ![Nervous](docs/screenshots/nervous.png) | ![X-ray](docs/screenshots/x-ray.png) |

### High-Fidelity Close-ups

| Visceral Organs | Deep Musculature |
| :---: | :---: |
| ![Organs](docs/screenshots/organs.png) | ![Muscles Close-up](docs/screenshots/muscles-closeup.png) |
| **Neurocranium & Cranial Nerves** | **Facial Anatomy** |
| ![Brain](docs/screenshots/brain.png) | ![Face](docs/screenshots/face.png) |

### Dynamic Biomechanics & Exercise Engine

| Exercise Directory | Targeted Semantic Search |
| :---: | :---: |
| ![Exercise List](docs/screenshots/exercises-list.png) | ![Exercise Search](docs/screenshots/exercises-search.png) |
| **Bench Press (Chest Primary, Shoulders & Triceps Secondary)** | **Deadlift (Superficial Layers Peeled to Reveal Erector Spinae)** |
| ![Bench Press](docs/screenshots/exercise-bench-press.png) | ![Deadlift](docs/screenshots/exercise-deadlift.png) |
| **Full Workout Volumetric Heatmap (Anterior)** | **Full Workout Volumetric Heatmap (Posterior)** |
| ![Workout Heatmap Front](docs/screenshots/workout-heatmap.png) | ![Workout Heatmap Back](docs/screenshots/workout-heatmap-back.png) |

### Tomography & Structural Dissection

| Sagittal Plane Cross-Section | Axial Plane Cross-Section |
| :---: | :---: |
| ![Sagittal Slice](docs/screenshots/slice-sagittal.png) | ![Axial Slice](docs/screenshots/slice-axial.png) |
| **Coronal Section (Muscles & Skeleton)** | **Kinematic Exploded View** |
| ![Coronal Slice](docs/screenshots/slice-coronal.png) | ![Exploded View](docs/screenshots/exploded.png) |

---

## 🕹 Navigation & Controls

| Action | Control / Shortcut | Description |
| :--- | :--- | :--- |
| **Orbit / Rotate** | `Left Click + Drag` | Rotates the 3D camera around current focal center |
| **Pan** | `Right Click + Drag` | Translates the camera plane |
| **Zoom** | `Mouse Wheel` / `Pinch` | Smooth distance dampening |
| **Identify Part** | `Mouse Hover` | Displays immediate tooltip with anatomical name |
| **Select Part** | `Left Click` | Opens comprehensive clinical inspector panel |
| **Focus Structure** | `Double Click` or `F` | Smoothly flies camera to center and zoom on structure |
| **Isolate Structure** | Click `Isolate` button | Hides all non-selected structures |
| **Exit Isolation** | `Esc` | Restores visibility and clears current selection |
| **Solo Layer** | `Double Click` layer name | Solos target layer and hides others |
| **View Presets** | `Front`, `Back`, `Left`, `Right`, `Reset` | Snaps camera to standard anatomical orientations |
| **Exercise Library**| `🏋 Exercises` Button | Toggles exercise library and workout analytics panel |
| **Cross-Section** | `Coronal`, `Sagittal`, `Axial` | Clips model along selected anatomical plane |
| **Explode Model** | `Exploded View` Slider | Radially expands parts from center of mass |
| **Copy State Link**| `🔗 Copy link to this view` | Copies full scene state URL to clipboard |

---

## 🛠 Tech Stack & Architecture

- **Rendering & 3D Engine**: [Three.js](https://threejs.org/) (r187) with WebGL 2.0
- **Spatial Acceleration**: [three-mesh-bvh](https://github.com/gkjohnson/three-mesh-bvh) for high-frequency BVH raycasting & hit-testing across batched meshes
- **Performance Geometry**: Three.js `BatchedMesh` architecture condensing ~2,500 distinct structures into ~40 GPU draw calls
- **Frontend Build Pipeline**: [Vite 8](https://vite.dev/) with native ES modules
- **Shading & Materials**: Physically Based Rendering (PBR) tissue shaders, custom stencil clipping caps, and Poly Haven HDR environment map
- **Model Pipeline**: Blender Python headless export, [glTF-Transform](https://gltf-transform.dev/), and [meshoptimizer](https://github.com/zeux/meshoptimizer) (compressing 7M polygons / 128 MB down to 1.8M polygons / 15 MB)

---

## 📁 Repository Structure

```
Somato3D/
├── index.html               # Master application shell & UI layout
├── public/
│   ├── data/
│   │   └── exercises.json   # 876 categorized biomechanical exercise entries
│   ├── env/
│   │   └── studio_small_09_1k.hdr  # Studio HDR illumination map
│   └── models/              # Optimized layer GLBs (~15 MB total)
│       ├── skin.glb
│       ├── muscles.glb
│       ├── arteries.glb
│       ├── veins.glb
│       ├── nerves.glb
│       ├── organs.glb
│       └── skeleton.glb
├── src/
│   ├── app.js               # Central reactive state engine
│   ├── main.js              # Entrypoint & module initialization
│   ├── scene.js             # WebGL renderer, camera controller, HDR pipeline
│   ├── style.css            # Responsive dark-theme UI styles
│   ├── body/
│   │   ├── loadBody.js      # Multi-layer GLB loader & BatchedMesh consolidation
│   │   └── materials.js     # Biomechanical PBR tissue shaders & stencil clipping
│   ├── data/
│   │   ├── structures.js    # Curated anatomical dictionary & alias mappings
│   │   ├── muscleInfo.js    # Origin, insertion, action & innervation catalog
│   │   ├── exercises.js     # Biomechanics exercise database interface
│   │   └── exerciseMuscles.js # Anatomical region ↔ muscle mapping tables
│   └── ui/                  # Modular UI controllers (picking, search, quiz, workouts)
├── tools/                   # Blender & gltf-transform model optimization scripts
└── docs/screenshots/        # Demonstration screenshots and figures
```

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (version 20.19.0 or higher recommended)
- `npm` (packaged with Node.js)

### Installation & Local Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sunildhakad01/Somato3D.git
   cd Somato3D
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Launch the development server**:
   ```bash
   npm run dev
   ```
   Open the displayed URL in your WebGL-compatible browser (typically `http://localhost:5173`).

4. **Build for production**:
   ```bash
   npm run build
   ```
   Production artifacts are generated in the `dist/` directory.

### Available Scripts

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts the local Vite dev server with fast hot module replacement |
| `npm run build` | Compiles and optimizes assets into `dist/` for production deployment |
| `npm run preview` | Locally serves the production build from `dist/` |
| `npm run models -- <rawDir>` | Optimizes raw Blender-exported GLTF layers using gltf-transform & meshoptimizer |
| `npm run fix-model` | Strips unnecessary surface artifacts and corrects normal orientation |
| `npm run exercises` | Synchronizes the latest exercise dataset from `free-exercise-db` |

---

## 🧬 3D Model Optimization Pipeline

To rebuild the compressed 3D layers from the original source files:
1. Obtain `Startup.blend` from the [Z-Anatomy repository](https://github.com/Z-Anatomy/Models-of-human-anatomy).
2. Run headless Blender layer classification and mesh export:
   ```bash
   blender -b --factory-startup Startup.blend --python tools/export_zanatomy.py -- path/to/raw
   ```
3. Run simplification and mesh compression:
   ```bash
   npm run models -- path/to/raw
   ```
4. Run normal corrections and geometry cleanup:
   ```bash
   npm run fix-model
   ```
*Detailed guidelines can be found in [`tools/README.md`](tools/README.md).*

---

## 📜 Credits & Attributions

- **3D Anatomical Models**: [Z-Anatomy](https://github.com/Z-Anatomy/Models-of-human-anatomy) by Gauthier Kervyn & Marcin Zielinski, licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Derived from **BodyParts3D** © The Database Center for Life Science (DBCLS), licensed under [CC BY-SA 2.1 Japan](https://creativecommons.org/licenses/by-sa/2.1/jp/).
- **Exercise & Biomechanics Database**: [free-exercise-db](https://github.com/yuhonas/free-exercise-db) by yuhonas, released into the public domain ([The Unlicense](https://unlicense.org/)).
- **HDR Environment Lighting**: [studio_small_09](https://polyhaven.com/a/studio_small_09) by Poly Haven, licensed under [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

See [`CREDITS.md`](CREDITS.md) for full licensing and citation details.

---

## 👨‍💻 Author

**Sunil Dhakad**
- GitHub: [@sunildhakad01](https://github.com/sunildhakad01)

---

## 📄 License

The software source code in this repository is provided under the [MIT License](LICENSE).
The anatomical 3D assets in `public/models/` are distributed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
