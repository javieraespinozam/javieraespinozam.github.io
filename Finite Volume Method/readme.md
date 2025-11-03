# Finite Volume Method for 2D Advection–Diffusion Heat Transfer

**Author:** Javiera Espinoza M.  
**Email:** jpem@bu.edu  
**LinkedIn:** [linkedin.com/in/jpespinozam](https://www.linkedin.com/in/jpespinozam/)  
**Course:** IP468 – Computational Fluid Dynamics  
**Instructor:** PhD Romain Gers  
**Institution:** Universidad Técnica Federico Santa María  
**Date:** November 22, 2023  

---

## Overview

This project develops a **Finite Volume Method (FVM)** simulation to model **heat transfer by advection and diffusion** in a two-dimensional (2D) laminar plane flow.  
The problem analyzes the heating of a flat flow where one wall is maintained at a constant high temperature, evaluating **temperature transport**, **stability**, and **convergence** under both **regular and irregular mesh configurations**.

The implementation is fully developed in **Python (NumPy, Matplotlib, and Google Colab)** and includes **validation routines** for 1D advection and diffusion phenomena.

---

## Objectives

- Formulate the 2D advection–diffusion heat equation using the **finite volume integral approach**.  
- Implement explicit numerical schemes with:
  - **Upwind (UDS)** for advection  
  - **Central Difference Scheme (CDS)** for diffusion  
- Compare results obtained using **regular** vs **non-uniform (irregular)** grids.  
- Analyze **numerical stability**, **Courant–Friedrichs–Lewy (CFL)** and **Fourier** conditions.  
- Validate the simulation against analytical 1D advection–diffusion solutions.

---

## Mathematical Model

The governing equation for temperature transport is:

\[
\frac{\partial T}{\partial t} + \nabla(\vec{u}T - D\nabla T) = 0
\]

where  
- \( T \): temperature [°C]  
- \( \vec{u} \): velocity vector [m/s]  
- \( D \): thermal diffusivity [m²/s]  

Boundary and initial conditions were imposed as follows:
- **Hot wall (AB)** at constant \( T_1 = 500–1500°C \)
- **Fluid domain** initialized at \( T_2 = 50°C \)
- **Symmetry** along the central axis  
- **No-flux condition** at the outlet wall  

---

## Computational Setup

| Parameter | Symbol | Value |
|------------|---------|-------|
| Channel length | \( L_x \) | 1.0 m |
| Channel height | \( L_y \) | 0.5 m |
| Diffusivity | \( D \) | \( 5×10^{-5} \, m²/s \) |
| Inlet velocity | \( u_0 \) | 0.001 m/s |
| Grid (regular) | \( 25 × 30 \) cells |
| Grid (irregular) | variable spacing (1.1× growth in x, 1.05× in y) |
| Simulation time | 1000 s |

---

## Numerical Schemes

### Regular Mesh
- Uniform grid spacing.
- Explicit scheme with **UDS–CDS** coupling.
- Stable under \( CFL ≤ 1 \).

### Irregular Mesh
- Geometrically stretched grid near the heated wall.  
- Captures finer temperature gradients.  
- Reduces numerical diffusion and improves accuracy.

---

## Validation

The code includes 1D test cases for:
- **Pure Advection:** Comparison of CFL-dependent accuracy.  
- **Pure Diffusion (x and y):** Analytical validation using the Fourier stability criterion \( r ≤ 0.5 \).  

---

## Results

- The **irregular grid** achieved faster convergence and better resolution of boundary-layer effects.  
- In both grids, **diffusion dominated over advection**, as confirmed by the **Péclet number (Pe ≈ 0.1–0.15)**.  
- Regular meshes exhibited artificial flattening due to coarse discretization.  
- Computed convergence times:
  - Regular grid: *Advection–Diffusion* → 2577 s  
  - Irregular grid: *Advection–Diffusion* → 1917 s  
- With higher temperature gradients (T₁ = 1500°C), convergence slowed due to nonlinear diffusion.

---

## Implementation

The simulation was written in **Python** using:
- `numpy` for numerical arrays and mesh operations  
- `matplotlib` for visualization  
- `math` for analytical function support  
- `imageio` for animation (optional visualization)

Google Colab was used as the execution environment.  

Example code snippet:
```python
T, t = temp(T, ny, v0, nx, ly, y, D, x, t2, t1, dt, t, diferencia)
plt.pcolormesh(x, y, T, cmap='plasma', shading='gouraud')
plt.title('2D Temperature Field')
plt.colorbar(label='Temperature [°C]')

