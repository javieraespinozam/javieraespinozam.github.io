# Computational Fluid Dynamics — Finite Differences & Finite Volumes (UTFSM)

This repository includes two computational projects developed by **Javiera Espinoza Morales** for the course  
**IP468 — Fundamentals of Computational Fluid Dynamics**, supervised by **Ph.D. Romain Gers** at  
**Universidad Técnica Federico Santa María (UTFSM)**, 2023.

Both assignments implement numerical methods for **advection–diffusion and wave equations**, exploring  
stability, accuracy, and convergence in fluid systems through **finite difference (FDM)** and **finite volume (FVM)** schemes.

---

## 1. Finite Difference Method (FDM) — 1D Wave Equation

### Overview
The first project, titled **"Ecuación de Ondas en todos sus estados"**, investigates the **1D scalar wave equation** and the **advection equation** using the **finite difference method**.  
Multiple explicit and implicit numerical schemes are implemented to model the propagation of acoustic waves and analyze their stability under different Courant numbers (Cr).

### Governing Equation
\[
\frac{\partial^2 P}{\partial t^2} - c_0^2 \frac{\partial^2 P}{\partial x^2} = 0
\]
where \(P\) is the pressure fluctuation and \(c_0\) is the sound speed.

### Numerical Schemes Implemented
- **Explicit Euler (Backward, Centered, Forward differences)**
- **Lax–Friedrichs Scheme**
- **Lax–Wendroff Scheme**
- **Leap–Frog Method**
- **Crank–Nicolson Scheme (Implicit)**
- **Centered Space, Implicit Euler in Time**

### Key Analyses
- Stability via **Courant–Friedrichs–Lewy (CFL)** condition.  
- Dispersion and dissipation characterization.  
- Comparison between explicit and implicit discretization errors.  
- Modeling of **1D and 4th-order scalar wave equations**.

### Main Results
- Backward differencing proved the most stable explicit scheme for \(Cr = 0.5\).  
- Lax–Friedrichs introduced artificial diffusion to maintain stability.  
- Lax–Wendroff achieved higher accuracy but suffered dispersion at large time steps.  
- Leap–Frog showed high-frequency oscillations (dispersive).  
- Implicit methods ensured unconditional stability at higher computational cost.

### Tools
- **Python / NumPy / Matplotlib** for visualization and validation  
- Analytical comparison for sinusoidal wave propagation

---

## 2. Finite Volume Method (FVM) — Heating of a Flat Flow

### Overview
The second project, titled **"Calentamiento de un flujo plano"**, applies the **finite volume method (FVM)** to simulate the **advection–diffusion of temperature** in a 2D laminar channel.  
The goal is to model how heat is transported and diffused through a **heated wall section**, comparing **regular** and **irregular** computational meshes.

### Governing Equation
\[
\frac{\partial T}{\partial t} + \nabla \cdot (\mathbf{u} T - D \nabla T) = 0
\]
where \(T\) is temperature, \(\mathbf{u}\) the velocity field, and \(D\) the thermal diffusivity.

### Simulation Setup
- **Domain:** \(1\,\text{m} \times 0.5\,\text{m}\) rectangular channel  
- **Boundary Condition:** lower plate heated at constant \(T_1 = 500°C\); upper plate \(T_2 = 50°C\)  
- **Velocity Profile:** parabolic, \(u(y) = u_0(1 - ((y - l_y)^2 / l_y^2))\), with \(u_0 = 0.001\,\text{m/s}\)  
- **Mesh:** 25 × 30 control volumes (regular and irregular)  
- **Diffusivity:** \(D = 5\times10^{-5}\,\text{m}^2/\text{s}\)

### Methodology
- Time discretization: **explicit scheme**  
- Advection term: **Upwind (UDS)**  
- Diffusion term: **Central Difference Scheme (CDS)**  
- Simulation time: **1000 s**

### Results and Validation
- **Regular Mesh:** Convergence time ≈ 2577 s  
- **Irregular Mesh:** Convergence time ≈ 1917 s  
- Advection–Diffusion validated through 1D cases (pure advection and pure diffusion).  
- Calculated **Péclet numbers** confirmed diffusion-dominated regime (Pe ≈ 0.1–0.15).  
- The irregular mesh captured finer gradients near boundaries, improving physical realism.

### Conclusions
- Diffusion dominates the heat transport phenomenon.  
- Mesh refinement strongly affects accuracy near singularities.  
- Explicit methods require strict CFL/Fourier stability conditions.  
- The FVM framework allows flexible adaptation to both regular and non-uniform grids.

### Tools
- **Python (NumPy, Matplotlib)** for mesh generation and result visualization  
- Validation notebooks executed in **Google Colab**


