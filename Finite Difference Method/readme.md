# Finite Difference Methods for 1D Wave and Convection Equations

**Author:** Javiera Espinoza M.  
**Email:** jpem@bu.edu  
**LinkedIn:** [linkedin.com/in/jpespinozam](https://www.linkedin.com/in/jpespinozam/)  
**Course:** IP468 – Fundamentals of Computational Fluid Dynamics  
**Instructor:** PhD Romain Gers  
**Institution:** Universidad Técnica Federico Santa María  
**Date:** October 23, 2023  

---

## Overview

This project implements and analyzes **Finite Difference Methods (FDM)** applied to one-dimensional (1D) convection and wave equations.  
It evaluates the performance, accuracy, and stability of both **explicit and implicit schemes** for modeling acoustic wave propagation.

The objective is to understand the numerical behavior of discrete approximations for the **1D wave equation** and identify the trade-offs between **dispersion, dissipation,** and **stability** under different Courant–Friedrichs–Lewy (CFL) numbers.

---

## Objectives

- Formulate and solve 1D convection and wave equations using finite difference approximations.  
- Compare **explicit** vs **implicit** schemes regarding stability and precision.  
- Validate numerical models against analytical solutions.  
- Develop computational models to visualize the effect of the CFL condition.

---

## Numerical Methods Implemented

### Explicit Schemes
- **Backward (Upwind):** Conditionally stable, low dissipation.  
- **Centered:** Unconditionally unstable for positive velocity.  
- **Forward:** Unconditionally unstable.  
- **Lax–Friedrichs:** Stable but dissipative.  
- **Lax–Wendroff:** Second-order accurate, dispersive.  
- **Leap–Frog:** Second-order accurate, prone to oscillations.

### Implicit Schemes
- **Implicit Euler (Backward in Time):** Stable, low-order accuracy.  
- **Crank–Nicolson:** Unconditionally stable, reduced dissipation.

---

## Analysis and Results

- The **Courant number (Cr)** controls the method’s stability: smaller values improve precision.  
- **Backward differencing** provides a good balance between accuracy and stability.  
- **Lax–Friedrichs** and **Lax–Wendroff** stabilize oscillations but introduce artificial damping or phase errors.  
- **Leap–Frog** and **4th-order schemes** show better accuracy at the cost of increased numerical noise.  
- Increasing the scheme order reduces truncation error and enhances solution fidelity.

---

## Implementation

Simulations were performed in **MATLAB/Octave**, using discretized forms of the 1D acoustic wave and convection equations.  
Each scheme was tested under various CFL numbers, and the corresponding figures and computational code are included in the annex section.

---

## Key Learnings

- Stability and precision depend strongly on time-step and spatial discretization.  
- The **CFL condition** is essential for determining valid time-step ranges.  
- Higher-order schemes improve accuracy but may require finer grids.  
- Balancing **computational cost** and **numerical fidelity** is key in CFD applications.

---

## Reference

Luis, R., Zenner, A., & José, V. (n.d.). *El método de diferencias finitas.*

---


