# Computational Astronomy Projects — Universidad Técnica Federico Santa María

This repository includes two observational astrophysics reports developed for the course **AST-205 — Computational Astronomy** under the guidance of **Dr. Odette Toloza Castillo (2022)**.  
Both projects apply practical data reduction and analysis techniques using professional astronomical software tools — **IRAF** and **APT (Aperture Photometry Tool)** — with data obtained from public observatories and databases such as **AstroQuinta** and **SDSS SkyServer**.

---

## 1. Spectral Analysis of Gacrux using IRAF

### Overview
This project presents the computational reduction and analysis of the **visible-light spectrum of Gacrux (Gamma Crucis)**, one of the main stars of the **Southern Cross (Crux)** constellation.  
The data were obtained from the **AstroQuinta Observatory** and processed using **Python (Jupyter Notebook)** for image preprocessing and **IRAF** for spectral extraction, normalization, and wavelength calibration.

### Objectives
- Extract and calibrate the stellar spectrum of Gacrux using IRAF.  
- Apply **Bias**, **Dark**, and **Flat-field** corrections to CCD images.  
- Generate a wavelength transformation using a **RELCO (Ar-Ne)** calibration lamp.  
- Identify absorption lines and estimate the physical properties of the star.

### Methodology
1. **Image Reduction**  
   - Used *MasterBias* and *MasterDark* frames to correct CCD noise.  
   - The *MasterFlat* was discarded after testing due to increased noise.  
   - Visual inspection and verification were done in Python with `matplotlib`.

2. **Spectral Extraction**  
   - Employed IRAF’s `apall` function to define apertures and extract the stellar signal.  
   - Background subtraction was performed to reduce sky noise.

3. **Normalization and Calibration**  
   - Normalized the *MasterFlat* using a 9th-order Legendre polynomial via IRAF’s `response` function.  
   - Created a wavelength transformation based on RELCO emission lines.  
   - Achieved a calibration RMS of 0.26, validating the accuracy of the wavelength fit.

4. **Spectral Analysis**  
   - Evaluated SNR across multiple pixel ranges (average SNR ≈ 15–30).  
   - Generated the final ADU–wavelength spectrum revealing characteristic absorption lines.

### Results
- **Star:** Gacrux (Gamma Crucis)  
- **Spectral Type:** M3.5 III (Red Giant)  
- **Estimated Temperature:** below 3700 K  
- **Detected lines:** Fe, TiO, and O₂ absorption features.  
- **Conclusion:** The results align with theoretical expectations for red giants and demonstrate IRAF’s effectiveness for academic spectroscopy despite its legacy status.

### Tools and Software
- **IRAF (Image Reduction and Analysis Facility)**  
- **Python 3.7 / Jupyter Notebook**  
- **Matplotlib**, **NumPy**  
- **AstroQuinta Observatory datasets**

### References
1. Toloza, O. *Espectros Cruz del Sur.* UTFSM Open Mind, 2022.  
2. Lewis, J. et al. *DER SNR: A Simple General Spectroscopic Signal-to-Noise Measurement Algorithm.* STScI, 2022.  
3. Barton, M. *What Is Signal-to-Noise Ratio and Why Does It Matter?* Lifewire, 2022.  
4. Walker, R. *RELCO Calibration Lines.* Ursus Major, 2022.  
5. STScI. *NICMOS Instrument Overview.* NASA Hubble, 2022.

### File

---

## 2. Aperture Photometry Analysis using APT

### Overview
This project applies **aperture photometry** to two celestial objects — a **star** and an **elliptical galaxy** — using the **Aperture Photometry Tool (APT)**.  
The aim was to measure and validate the apparent magnitudes of both objects and compare them to catalog values from the **SDSS SkyServer** database.  

This report demonstrates the process of defining apertures, background annuli, and analyzing growth curves, while evaluating measurement precision and noise.

### Objects Analyzed
- **Star:** SDSS J115906.26-003932.4  
  - Position: (179.776°, -0.659°)  
  - Velocity: 191.4 km/s  
- **Galaxy:** 6dFGS gJ113953.5-033106  
  - Velocity: 18,930 km/s  

### Methodology
1. Downloaded **FITS** images with the *g-band filter* from the SDSS SkyServer.  
2. Loaded each object into **APT** and centered apertures using the *Aperture Slice* diagnostic tool.  
3. Defined aperture and annulus radii ensuring isolation of the source and background.  
4. Measured fluxes, computed magnitudes, and compared against SkyServer catalog values.  
5. Analyzed **curve of growth** and **signal-to-noise ratio (S/N)** for both cases.

### Results

#### A. Star (Point Source)
- **Measured Magnitude:** 17.4416  
- **SkyServer Magnitude:** 17.4208  
- **Error:** 0.12%  
- **Signal-to-Noise Ratio:** ≈ 400  
- Correct centering confirmed by radial profile (FWHM ≈ 3 px).  
- Demonstrated high accuracy for isolated, non-saturated stellar objects.

#### B. Galaxy (Extended Object)
- **Measured Magnitude:** 15.953 (catalog 14.909)  
- **Error:** ≈ 6–7%  
- Larger uncertainty due to irregular luminosity distribution and extended shape.  
- Recommended to use alternative software or larger apertures for extended sources.

### Conclusions
- **APT** delivers precise photometric results for **point sources** but limited accuracy for **extended objects** like galaxies.  
- Photometric precision is highly sensitive to aperture size, centering, and background definition.  
- The project highlights the critical relationship between instrument calibration and measurement accuracy in astronomical photometry.  
- Future work may include integrating Python-based automation or alternate methods for galaxy photometry.

### Tools and Software
- **Aperture Photometry Tool (APT)**  
- **SDSS SkyServer FITS datasets**  
- **Python** (for S/N and visualization calculations)

### References
1. Barton, M. *Signal-to-Noise Ratio and Its Importance.* Lifewire, 2022.  
2. Rebull, L. *NITARP Tutorial: APT Overview.* YouTube, 2022.
