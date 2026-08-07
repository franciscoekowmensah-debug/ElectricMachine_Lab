# ⚡ 3D Synchronous Machine Laboratory Simulation

An interactive, immersive 3D/VR engineering workspace built from scratch to bridge the gap between abstract mathematical motor equations and tactile engineering implementation. This application deploys seamlessly to modern web browsers via Unity's WebGL/Web 6 pipeline and features full world-space control rigs.

🚀 **[[LIVE_GITHUB_PAGE LINK]](https://franciscoekowmensah-debug.github.io/ElectricMachine_Lab/)**

---

## 🔬 Core Learning Objectives & Design Layout

* **The Core Task:** Students step into a 3D workspace to interact with a synchronized industrial motor/generator (comprising the stator housing, copper windings, rotor assembly, salient magnetic poles, and bearing end shields).
* **The Engineering Challenge:** Students dynamically alter real-time operational variables and instantly analyze the physical and analytical behavioral shifts along a normalized performance envelope.
* **The "Adaptive" Logic:** If operational conditions drift unsafe (e.g., under-voltage, missing excitation current, or massive load saturation points), an integrated AI Tutor panel dynamically blocks execution and surfaces guided, interactive tips.

---

## 🛠️ Simulation Architecture & Physics Engine

* **Front-End Casing & Graphics:** High-quality modular assets optimized with low-poly layouts to achieve rapid loading performance profiles over standard web frequencies. 
* **Mathematical Computation Engine:** Robust C# pipelines calculating real-time electrical machine formulas ($P = \omega T$, Synchronous Speed $N_s = \frac{120f}{P}$, torque capability boundaries, and alternating magnetic field profiles).
* **Interactive Dashboard:** Dual world-space tracking canvases mounted flat against the laboratory wall:
  1. **Control Tablet:** Housing physical slider elements for Line Frequency ($Hz$), Field Excitation ($A$), and Supply Voltage ($V$).
  2. **AI Tutor Display:** Pushing real-time analytical text descriptions, voltage warnings, and engine fault tracking diagnostics.

---

## 🛑 Real-Time Fault Simulation Matrix

The mathematical core actively monitors student inputs and instantly enforces physical boundary constraints:
* **Under-Voltage Fault (< 50V):** The electrical pressure drops too low to safely drive magnetizing currents through the stator core.
* **Excitation Saturation (< 1.0A):** The rotor lacks sufficient magnetic field alignment capability to lock steps into the rotating magnetic field (RMF).
* **Pull-Out / Stall Condition:** When applied mechanical load torque overpowers the current available peak breakdown torque envelope, the magnetic coupling snaps and the actual rotor RPM crashes to 0 instantly.
* **Field-Weakening Physics:** Operating the system past nominal base frequency (50Hz) triggers a quadratic drop in torque capabilities, simulating real-world machine constraints.

---

## 💾 Local Development & Deployment Workflow

### Prerequisites
* Unity 6 (or modern Web compilation support)
* TextMeshPro package dependencies

### Build Configuration Instructions
1. Switch your active Build Profile platform to **Web / WebGL**.
2. Navigate to **Player Settings > Publishing Settings** and toggle **Compression Format** to **Disabled** *(enables standard static file servers to host `.wasm` binaries without server-side compression configurations)*.
3. Build the files directly into a production directory folder named `docs`.
4. Push the `docs` package to GitHub and enable **GitHub Pages** targeting the `/root` directory of your main branch.
