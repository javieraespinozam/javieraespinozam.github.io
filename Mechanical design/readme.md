# Gear Box Design — Technical Drawing

## Overview
This document presents a gearbox assembly designed and modeled in **Autodesk Inventor**, illustrating the mechanical layout, key dimensions, and assembly views for the transmission system.  
The PDF contains orthographic projections and section views used to validate clearances, gear alignment, and housing geometry.

## Contents
- Assembly Drawing: Exploded and assembled views of the gearbox  
- Component Dimensions: Detailed measurements for shafts, bearings, gears, and housing  
- Bill of Materials (BOM): Reference parts included in the mechanical system  
- Tolerances and Annotations: Machining and fit information aligned with standard manufacturing practices

## Design Objective
The gearbox is intended to **transmit mechanical power efficiently** between rotating shafts under variable load conditions.  
The design focuses on:
- Torque transmission efficiency  
- Compactness and ease of assembly  
- Material optimization for lightweight yet durable performance  
- Compatibility with standard gear module specifications

## Tools and Methods
- Software: Autodesk Inventor (modeling and drawing)
- File Format: PDF export of `.iam` / `.idw` mechanical assembly
- Analysis: Preliminary kinematic and structural verification using CAD parameters

## How to View
To explore the model interactively:
- Upload the `.iam` or `.ipt` files to [Autodesk Viewer](https://viewer.autodesk.com/)
- Or open with CAD-compatible software such as **Fusion 360**, **FreeCAD**, or **Solid Edge Viewer**


---

## 3. Aperture Photometry Analysis using APT

### Overview
This project uses the **Aperture Photometry Tool (APT)** to perform quantitative photometric measurements on two celestial objects — a **star** and an **elliptical galaxy** — comparing the measured magnitudes with catalog values from **SDSS SkyServer**.

### Objects
- **Star:** SDSS J115906.26-003932.4 — Velocity: 191.4 km/s  
- **Galaxy:** 6dFGS gJ113953.5-033106 — Velocity: 18,930 km/s  

### Results
#### Star (Point Source)
- **Measured Magnitude:** 17.4416  
- **SkyServer Magnitude:** 17.4208  
- **Error:** 0.12%  
- **S/N Ratio:** ≈ 400  
- FWHM ≈ 3 px confirms precise centering.

#### Galaxy (Extended Object)
- **Measured Magnitude:** 15.953  
- **Catalog Magnitude:** 14.909  
- **Error:** ≈ 6–7%  
- Reduced accuracy due to irregular luminosity and extended geometry.

### Conclusions
- **APT** delivers highly accurate results for point sources but less so for extended galaxies.  
- Highlights the impact of aperture size and centering on photometric accuracy.  
- Suggests Python integration for future automated photometric analysis.

### Tools
- **Aperture Photometry Tool (APT)**  
- **SDSS SkyServer FITS Data**

### File
