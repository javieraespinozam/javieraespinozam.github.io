# Hydrogen–Impurity Mixture under Rapid Compression

**Author:** Javiera Paz Espinoza Morales  
**Institution:** Universidad Técnica Federico Santa María – Department of Mechanical Engineering  
**Email:** jpem@bu.edu  
**LinkedIn:** [linkedin.com/in/jpespinozam](https://www.linkedin.com/in/jpespinozam/)

---

## Overview

This repository contains the computational framework and validation results from my undergraduate thesis:
**“Computational study of hydrogen mixtures with impurities under rapid compression.”**  
The project models the thermal and dynamic behavior of hydrogen–based gas mixtures during rapid compression using **Computational Fluid Dynamics (CFD)** in *ANSYS Fluent*.

The study contributes to understanding the influence of micro-scale solid impurities on temperature distribution and auto-ignition within hydrogen mixtures — a key consideration in next-generation clean-combustion systems.

---

## Objectives

- Validate a CFD model of hydrogen compression using the experimental data of **Mittal et al. (2008)**.  
- Simulate a **Rapid Compression Machine (RCM)** under transient, axisymmetric conditions.  
- Analyze the impact of a **microscopic solid impurity** on local heat transfer and temperature evolution.  
- Quantify the influence of impurity temperature on the auto-ignition process.

---

## Methodology

- **Software:** ANSYS Fluent 2023R1  
- **Modeling type:** 2D axisymmetric transient CFD  
- **Turbulence models:** Laminar and *k–ω SST*  
- **Mesh motion:** Dynamic layering method  
- **Species transport:** Enabled (H₂/N₂/Ar mixtures, non-reactive)  
- **Validation case:** Mittal et al., *Combustion and Flame*, 155(3), 417-428, 2008  

---

## Results Summary

- Pressure–temperature curves were validated against Mittal et al., with average error < 3%.  
- The inclusion of a solid impurity (Cu or Al particle) generated localized high-temperature gradients.  
- Cases with elevated impurity temperature (400 K) showed measurable acceleration of the ignition delay.  
- The model demonstrated the viability of using Fluent’s dynamic mesh and species transport for early ignition studies.


## Citation

If you use or reference this work, please cite:

> Espinoza Morales, J. P. (2025). *Estudio computacional de mezclas de hidrógeno con impurezas bajo compresión rápida.*  
> Universidad Técnica Federico Santa María, Departamento de Ingeniería Mecánica, Valparaíso, Chile.

---

## Keywords

Hydrogen combustion · CFD · ANSYS Fluent · Rapid Compression Machine · Heat transfer · Auto-ignition · Dynamic mesh

---

