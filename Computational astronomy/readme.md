
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
