# 🌌 AFEED: The Operating System for Science

Welcome to the official documentation for **AFEED**, a comprehensive, browser-based operating system dedicated to scientific exploration. Unlike standard educational websites, AFEED is structured as an integrated environment where students, educators, and science enthusiasts can interact with textbook concepts through high-fidelity, real-time mathematical and physical simulations.

This manual provides an in-depth breakdown of the platform's architecture, its core environments, and a detailed usage guide for every simulation included in the suite.

---

## 🏛️ Platform Architecture & Environments

The AFEED ecosystem is divided into three primary environments. To begin your experience, you will interact with these core portal files:

### 1. The Main Dashboard (`index.html`)
This is the heart of the "Operating System." It acts as your desktop environment.
*   **What it is:** A dynamic curriculum browser featuring a 3D-hover interface with dark/light mode environments (Neon Indigo/Warm Orange spotlights).
*   **How to use it:** Open `index.html` in any web browser. Use the top navigation tabs to switch between scientific disciplines (Physics, Chemistry, Math, ICT). Use the search bar to filter specific topics. Click on any illuminated "Chapter Card" to expand it and launch the associated simulations.

### 2. The Study Command Center (`study-center.html`)
*   **What it is:** A built-in productivity and focus environment designed to parallel your simulation work.
*   **How to use it:** Launch this file alongside your simulations. It provides tools for time management, syllabus tracking, and maintaining focus during deep-study sessions.

### 3. Afeed Studio Portal (`Afeed_studio_portal.html`)
*   **What it is:** The administrative or creative entry point for configuring simulation parameters or accessing advanced tools within the AFEED ecosystem.

---

## 🏛️ System Architecture & UI Design

AFEED is engineered as a highly accessible, standalone web application. It does not require a complex backend infrastructure to run its core simulations, relying instead on client-side native web technologies to deliver a real-time, low-latency experience.

### Technical Architecture
*   **Core Stack:** HTML5, Vanilla JavaScript, and Tailwind CSS.
*   **Study Command Center Architecture:** Unlike the static simulations, `study-center.html` is built as a client-side **React.js Application** injected into a single HTML file via CDN. It securely synchronizes user data (progress, scores, statuses) through a serverless backend powered by **Google Apps Script**.
*   **Deployment:** Can be run completely offline via direct file execution, or hosted on any static file server (including GitHub Pages or a simple Express.js static server).

### Unified UI/UX Elements
Across all pages, AFEED maintains a strict, premium visual identity designed to reduce cognitive load during study sessions:

1.  **Dual Environment Modes:**
    *   **Dark Mode (Neon Indigo):** Optimized for low-light environments, featuring deep slate backgrounds, indigo accent gradients, and neon spotlights.
    *   **Light Mode (Warm Orange):** A high-contrast daytime mode using clean off-white canvases and warm amber/orange gradients.
2.  **Glassmorphism & Depth:** Control panels and navigation elements utilize `backdrop-filter` blurs (glassmorphism) layered over animated background canvases.
3.  **3D Hover Engine:** Interactive elements (like Chapter Cards) utilize a bespoke CSS/JS 3D transform engine that tracks mouse position to cast dynamic shadows and radial spotlights.
4.  **Typography:** 
    *   *Inter* for clean, modern interface text.
    *   *Noto Sans Bengali* for seamless bilingual support.
    *   *JetBrains Mono* for mathematical readouts and data displays.
5.  **Simulation Canvases:** Each physics simulation reserves the maximum possible screen real estate for the HTML5 `<canvas>` rendering context, floating the control sliders in draggable or fixed translucent sidebars.

---

## 🧪 Comprehensive Simulation Manual

Every simulation in AFEED is a standalone interactive application. Here is exactly what they do and how to operate them to maximize your learning.

### 🌊 Mechanics & Oscillations

#### Simple Harmonic Motion Simulation (`Simple harmonic motion Simulation.html`)
*   **Core Concept:** Visualizes the physics of a mass-spring system undergoing simple harmonic motion (SHM).
*   **What you will see:** A visual representation of an oscillating mass alongside real-time kinematic graphs tracking Displacement ($x$), Velocity ($v$), and Acceleration ($a$) over time.
*   **Step-by-Step Usage:**
    1. Locate the control panel.
    2. Adjust the **Spring Constant ($k$)** to make the spring stiffer or looser.
    3. Adjust the **Mass ($m$)** of the block.
    4. Set the **Initial Amplitude**.
    5. Press **Play**. Observe the graphs: notice how velocity reaches its absolute maximum precisely when displacement is zero, and how acceleration is always opposite to displacement.

#### SHM Pendulum Simulation (`SHM Pendulum Simulation.html`)
*   **Core Concept:** Explores harmonic motion through the classic simple pendulum, focusing heavily on the Law of Conservation of Energy.
*   **What you will see:** A swinging pendulum bob and dynamic bar charts/line graphs representing Kinetic Energy (KE), Potential Energy (PE), and Total Energy (TE).
*   **Step-by-Step Usage:**
    1. Click and drag the pendulum bob to set your initial release angle.
    2. Use the sliders to change the **Length** of the string and the **Mass** of the bob.
    3. Change the **Gravity** environment (e.g., Earth, Moon, Jupiter) to see how local $g$ affects the period.
    4. Watch the energy graphs: as the pendulum reaches the bottom, PE drops to zero and KE maxes out. Total Energy remains a flat, constant line.

### 🔭 Optics & Light

#### Double-Slit Experiment Simulation (`Double-Slit Experiment Simulation.html`)
*   **Core Concept:** A digital recreation of Thomas Young’s experiment demonstrating the wave nature of light and quantum interference.
*   **What you will see:** A laser source hitting a barrier with two slits, expanding as wavefronts, and projecting an interference pattern (bright and dark fringes) on a back screen.
*   **Step-by-Step Usage:**
    1. Use the **Wavelength** slider to change the color of the light (e.g., from red $700nm$ to blue $400nm$).
    2. Adjust the **Slit Separation ($d$)**. Bringing them closer together spreads the interference fringes further apart.
    3. Adjust the **Screen Distance ($L$)**.
    4. Observe the intensity graph on the screen to understand constructive interference (bright bands) and destructive interference (dark bands).

#### Lens Visual Simulation (`Lens visual Simulation.html`)
*   **Core Concept:** Geometric optics and ray tracing for convex (converging) and concave (diverging) lenses.
*   **What you will see:** An optical axis, a lens, an object (usually an arrow), and the three principal light rays used to determine image formation.
*   **Step-by-Step Usage:**
    1. Select your lens type (Convex or Concave).
    2. Drag the object along the principal axis.
    3. Adjust the **Focal Length ($f$)** of the lens.
    4. Watch the principal rays (the parallel ray, the focal ray, and the central ray) automatically recalculate. 
    5. Note when the image crosses from being **Real and Inverted** to **Virtual and Upright** (specifically when the object crosses the focal point of a convex lens).

#### Deviation Angle of Prism Simulation (`Deviation Angle of Prism Simulation.html`)
*   **Core Concept:** Explores Snell's Law and chromatic dispersion through a triangular glass block.
*   **What you will see:** A laser beam entering a prism, refracting twice, and exiting at a deviated angle.
*   **Step-by-Step Usage:**
    1. Adjust the **Incident Angle** of the incoming laser.
    2. Modify the **Prism Angle** (the apex angle).
    3. Change the **Refractive Index** (e.g., from air $1.0$ to glass $1.5$ to diamond $2.4$).
    4. Track the **Angle of Deviation** output. Try to find the exact angle of incidence that produces the "Minimum Deviation" for a given refractive index.

### 🎶 Wave Physics & Acoustics

#### Superposition of Wave Simulation (`Superposition of wave Simulation.html`)
*   **Core Concept:** The principle that when two or more waves overlap in space, the resultant wave is the algebraic sum of the individual waves.
*   **What you will see:** Multiple independent wave graphs and a final "Resultant Wave" graph.
*   **Step-by-Step Usage:**
    1. Add a wave profile using the controls.
    2. Set its **Amplitude**, **Frequency**, and **Phase Shift**.
    3. Add a second wave. 
    4. Observe how peaks aligning with peaks create massive resultant amplitudes, while peaks aligning with troughs flatten the resultant wave to zero.

#### Beat Understanding (`Beat Understanding.html`)
*   **Core Concept:** The acoustic phenomenon of "beats" created when two sound waves of slightly different frequencies interfere, causing a pulsating volume.
*   **What you will see:** Two high-frequency sound waves and their combined resulting waveform, which features a distinct envelope (the beat).
*   **Step-by-Step Usage:**
    1. Input **Frequency 1** (e.g., $440 Hz$).
    2. Input **Frequency 2** (e.g., $444 Hz$).
    3. The simulation calculates the resultant wave. You will visually see the amplitude swelling and shrinking 4 times per second (a beat frequency of $4 Hz$).

### 📐 Advanced Mathematics

#### Vector Calculus Simulation (`Vector Calculus Simulation.html`)
*   **Core Concept:** Visualizing 2D/3D vectors and complex field operations that are normally difficult to conceptualize on paper.
*   **What you will see:** A coordinate plane with manipulatable vector arrows and mathematical readouts.
*   **Step-by-Step Usage:**
    1. Input vector coordinates (e.g., $\vec{A} = 3\hat{i} + 4\hat{j}$, $\vec{B} = -1\hat{i} + 2\hat{j}$).
    2. Select operations like **Addition**, **Subtraction**, **Dot Product** (yielding a scalar), or **Cross Product** (yielding an orthogonal vector).
    3. For advanced fields, visualize gradient slopes or the rotational curl of a vector field mapped directly onto the grid.

### ⚛️ Chemistry

#### Super Periodic Table (`Super Periodic Table.html`)
*   **Core Concept:** A digital, data-rich replacement for the standard paper periodic table.
*   **What you will see:** The standard periodic grid, color-coded by element families, with deep-dive informational panels.
*   **Step-by-Step Usage:**
    1. Hover over any element to see its quick stats (Atomic Number, Symbol, Weight).
    2. Click an element to open its detailed profile, including its full electron configuration, electronegativity, oxidation states, and discovery history.
    3. Use the top filters to isolate specific groups (e.g., "Show only Halogens" or "Highlight the d-block").

---

## 💻 How to Run the Environment Locally

Because AFEED is built entirely on native Web Technologies (HTML, CSS, JavaScript), running it is completely frictionless.

**Option 1: Direct File Execution (Zero Setup)**
1. Clone or download the ZIP of this repository.
2. Extract the folder.
3. Double-click `index.html` to open it in your default web browser. 

**Option 2: Local Development Server (Recommended)**
For the best experience (preventing CORS issues on certain browsers), run it through the provided Node server:
1. Ensure you have [Node.js](https://nodejs.org/) installed.
2. Open your terminal in the AFEED directory.
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the server:
   ```bash
   npm run dev
   ```
5. Open your browser and navigate to `http://localhost:3000`.

---

## 📜 License & Copyright

**MIT License**
Copyright (c) 2026 Md. Fahmid Hossain Afeed.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software... [Standard MIT terms apply].
