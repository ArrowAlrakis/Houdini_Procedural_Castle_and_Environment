# Houdini Procedural Castle and Environment

**Author**: Arrow Lyu  
**Software**: Houdini  
**Project Type**: Procedural Modeling / Environment Generation  
**File**: `Procedural_Castle_v12.hipnc` 

---

##  Overview

This project presents a fully procedural castle and surrounding environment system created in Houdini. Inspired by the real Bodiam Castle in England, it focuses on modularity, parameterization, and scalability, making it highly adaptable for use in game development, level design, or simulation environments.

Through a combination of attribute-driven design, parameter exposure, and custom VEX expressions, the entire scene — from castle towers and walls to terrain, vegetation, and rocks — can be generated, modified, and optimized non-destructively.

[Castle Preview](./Preview.jpg)

[Project Breakdown and User Guide](./Breakdown_and_User_Guide.pdf)

▶ Watch the procedural castle demo video: [Download .mp4](./Procedural_Castle_Demo.mp4)

---

##  Features

###  Castle Generation (Modular & Procedural)

- Parametric control over:
  - Wall width, depth, and height
  - Tower radius, level height, and number of windows
  - Keep dimensions, gate arches, and bridge size
- Procedural window placement using `copy to points`, orienting with quaternions and normals.
- All elements are interconnected through attributes and updated dynamically with expressions.
- Easy customization via a top-level controller node.

###  Terrain and Environment

- Terrain built with layered `heightfields` using:
  - Noise, distort, erosion
  - Heightfield mask by feature
  - Painted masks for vegetation and erosion zones
- Procedural **vegetation instancing** using `copy to points`, camera culling, and randomized bush models.
- **Rock generation** from noise-distorted spheres with VDB remesh for stylized forms.

---

##  Procedural Logic

Key elements in this system rely on:

- **Attribute linking**: Each castle part shares or references other attributes (e.g., `@width`, `@depth`, `@height`) so that global changes ripple across the system.
- **VEX & HScript expressions**: Used to drive positioning, orientation, spacing, and copying logic.
- **For-each loops**: Applied in vegetation instancing to assign random models to points.
- **Quaternions (`@orient`) and Normals**: Ensure correct orientation for elements like windows and towers on curved surfaces.

---

##  User Guide

This system is designed with usability in mind. Users can customize the castle and terrain via exposed parameters in the top-level node UI. These controls ensure customizing different castles and environment variations without touching the node graphs.

[Project Breakdown and User Guide](./Breakdown_and_User_Guide.pdf)

---

##  Demo 

▶ Watch the procedural castle demo video: [Download .mp4](./Procedural_Castle_Demo.mp4)

---

##  Files Included

- `Breakdown_and_User_Guide.pdf` – User guide and project breakdown
- `Procedural_Castle_v12.hipnc` – The Houdini project file of the procedural castle
- `Procedural_Castle_with_Animation_v12.hipnc` – The Houdini project file of the procedural castle with animation
- `Preview.jpg` – Preview render of one example of the castle and the environment
- `Procedural_Castle_Demo.mp4` – Demo video of the castle

---

##  Applications

- Game Level Design
- Environment Prototyping
- Real-time Scene Generation
- Educational Reference for Procedural Systems


