# Computational Astronomy Projects — UTFSM

This repository includes two observational astrophysics reports developed for the course **AST-205 — Computational Astronomy** at *Universidad Técnica Federico Santa María* under the guidance of **Dr. Odette Toloza Castillo (2022)**.  
Both projects apply practical data-reduction and analysis techniques using professional astronomical software tools.

---

## 1. Spectral Analysis of Gacrux using IRAF

### Overview
This project presents the computational reduction and analysis of the **visible-light spectrum of Gacrux (Gamma Crucis)**, one of the main stars of the **Southern Cross (Crux)** constellation.  
Data were obtained from the **AstroQuinta Observatory** and processed using **Python (Jupyter Notebook)** and **IRAF**.

### Objectives
- Extract the stellar spectrum of Gacrux and calibrate it using IRAF.  
- Perform bias, dark, and flat-field corrections.  
- Generate a wavelength transformation using a **RELCO (Ar-Ne)** calibration lamp.  
- Identify absorption lines to determine spectral type and temperature.

### Methodology
- Preprocessing and visualization in **Python 3.7 / Jupyter Notebook**.  
- CCD noise correction using *MasterBias* and *MasterDark* images.  
- Spectral extraction with IRAF’s `apall` function and background subtraction.  
- Wavelength calibration using RELCO emission lines (RMS ≈ 0.26).

### Results
- **Star:** Gacrux (Gamma Crucis) — Spectral Type **M3.5 III (Red Giant)**  
- **Estimated Temperature:** < 3700 K  
- Identified absorption lines of Fe, TiO, and O₂.  
- Confirmed expected molecular bands for cool red giants.  
- Demonstrated IRAF’s continued reliability for academic spectroscopy.

### Tools and Software
- **IRAF**, **Python (Matplotlib, NumPy)**  
- **AstroQuinta Observatory datasets**

### References
1. Toloza, O. *Espectros Cruz del Sur*, UTFSM, 2022.  
2. Lewis et al. *DER SNR Algorithm*, STScI, 2022.  
3. Barton, M. *Signal-to-Noise Ratio*, Lifewire, 2022.  
4. Walker, R. *RELCO Calibration Lines*, Ursus Major, 2022.  
5. STScI. *NICMOS Instrument Overview*, NASA Hubble, 2022.

### File
