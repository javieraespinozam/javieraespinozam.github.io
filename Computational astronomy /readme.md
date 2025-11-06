# Spectral Analysis of Gacrux using IRAF

## Overview
This project documents the computational reduction and analysis of the **visible-light spectrum of Gacrux (Gamma Crucis)**, one of the principal stars of the **Southern Cross (Crux)** constellation.  
It was conducted as part of the **AST-205 — Computational Astronomy** course at *Universidad Técnica Federico Santa María* under the guidance of **Dr. Odette Toloza Castillo**.

The analysis combines data obtained from the **AstroQuinta Observatory** with the use of **Python (Jupyter Notebook)** for image preprocessing and **IRAF** for spectral extraction, normalization, and wavelength calibration.

---

## Objectives
- Extract and calibrate the stellar spectrum of Gacrux using astronomical image reduction techniques.  
- Apply **Bias**, **Dark**, and **Flat-field** corrections to CCD images.  
- Normalize the master flat and background using IRAF.  
- Generate a wavelength transformation function using a **RELCO (Ar-Ne)** calibration lamp.  
- Identify major **absorption lines** and estimate the physical characteristics of the star.

---

## Methodology

### 1. Image Reduction
- Used *MasterBias* and *MasterDark* frames to remove CCD noise.  
- The *MasterFlat* was discarded due to increased noise rather than correction.  
- All preprocessing steps were visualized and verified in **Python (matplotlib)**.

### 2. Spectral Extraction
- IRAF’s `apall` function was employed to extract the stellar spectrum and define the aperture.  
- Background subtraction ensured accurate ADU (Analog-to-Digital Unit) measurements.

### 3. Normalization and Calibration
- The master flat was normalized with a **9th-order Legendre fit** using the IRAF `response` function.  
- Wavelength calibration was obtained from RELCO emission lines, yielding a linear fit with **RMS = 0.26**, confirming accurate transformation.

### 4. Spectral Analysis
- Signal-to-Noise Ratio (SNR) evaluated across multiple pixel ranges: 15–30 on average.  
- The final spectrum (ADU vs. wavelength) revealed clear **absorption features** due to Fe, TiO, and O₂.  
- Hydrogen lines appeared weak, consistent with late-type red giant spectra.

---

## Results
- **Star:** Gacrux (Gamma Crucis) — Spectral Type **M3.5 III (Red Giant)**  
- **Estimated temperature:** below **3700 K**  
- **Spectral confirmation:** presence of molecular TiO bands and metallic absorption lines typical of cool stars.  
- The calibrated visible spectrum matches theoretical expectations for red giants.  
- IRAF, although legacy software, proved reliable for educational spectroscopic analysis.

---

## Tools and Software
- **IRAF (Image Reduction and Analysis Facility)**  
- **Python 3.7 / Jupyter Notebook**  
- **Matplotlib**, **NumPy**  
- **AstroQuinta Observatory datasets**

---

## References
1. Toloza, O. *Espectros Cruz del Sur.* UTFSM Open Mind, 2022.  
2. Lewis, J. et al. *DER SNR: A Simple General Spectroscopic Signal-to-Noise Measurement Algorithm.* STScI, 2022.  
3. Barton, M. *What Is Signal-to-Noise Ratio and Why Does It Matter?* Lifewire, 2022.  
4. Walker, R. *RELCO Calibration Lines.* Ursus Major, 2022.  
5. STScI. *NICMOS Instrument Overview.* NASA Hubble, 2022.

---

## Repository Structure

