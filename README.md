# PixelVeg — Plant Image Analyser
Plant Image Analyser. Upload a plant image to compute mean RGB values and five vegetation indices.


[![License: MIT](https://img.shields.io/badge/License-MIT-lightgreen.svg)](https://opensource.org/licenses/MIT)
[![DOI](https://doi.org/10.5281/zenodo.20179128)](https://doi.org/10.5281/zenodo.20179128)



---

## Overview

PixelVeg is a free, browser-based tool for non-invasive plant image analysis. Upload a plant photograph and the tool computes mean RGB pixel values across the entire image, then calculates five vegetation indices commonly used to estimate chlorophyll content and canopy health.

No installation, no programming knowledge, and no data upload to any server is required. All processing runs locally in the user's browser.

PixelVeg is part of the [BioCalcHub](https://biocalchub.com) project.

---

## Features

- Upload any plant photograph (JPG, PNG, WebP)
- Computes mean R, G, B values across all pixels
- Calculates five vegetation indices: ExG, GLI, VARI, GEI, RGR
- Exports results as CSV for use in spreadsheets or statistical software
- Formula reference panel with range and interpretation notes
- Runs entirely client-side — no server, no data collection

---

## Vegetation Indices

| Index | Full Name | Formula | Notes |
|-------|-----------|---------|-------|
| ExG | Excess Green Index | 2·g − r − b | Correlates with chlorophyll; range ≈ −1 to 1 |
| GLI | Green Leaf Index | (2·G − R − B) / (2·G + R + B) | Positive values indicate green biomass |
| VARI | Visible Atmospherically Resistant Index | (G − R) / (G + R − B) | Reduces lighting variation effects |
| GEI | Green Excess Index | g − (r + b) / 2 | Simple normalised version |
| RGR | Red / Green Ratio | R / G | Low = healthy green; high = stress or senescence |

**Normalisation:** lowercase r, g, b = raw values divided by 255 (range 0–1). Uppercase R, G, B = raw 0–255 values.

---

## Limitations

Users should be aware of the following before citing results:

- **Whole-image averaging:** PixelVeg computes indices from the mean colour of all pixels. Images containing soil, pots, sky, or other non-plant material will bias results. Background removal is not currently implemented.
- **Lighting sensitivity:** RGB-based indices are affected by illumination conditions. Controlled or consistent lighting improves reproducibility.
- **No spatial analysis:** The tool does not segment individual leaves or regions of interest.
- **Intended use:** PixelVeg is suitable for exploratory analysis and educational purposes. For publication-grade measurements, validate results against ground-truth data (e.g. spectrophotometric chlorophyll assays).

---

## Usage

Access the live tool at: **https://biocalchub.com/pixelveg/**

No installation required. Open in any modern browser.

### Local use

Download or clone this repository and open `index.html` directly in a browser. No build step or server required.

```bash
git clone https://github.com/BioCalcHub/pixelveg.git
cd pixelveg
# Open index.html in your browser
```

---

## Repository Structure

```
pixelveg/
├── index.html       # Main application
├── style.css        # Stylesheet
├── README.md        # This file
└── LICENSE          # CC BY 4.0
```

---

## Citation

If you use PixelVeg in your research, please cite it as follows.

### APA

> [Hlubina, P., Uvackova, L.] ([2026]). *PixelVeg: Plant Image Analyser* (Version [1.X.X]) [Software]. Zenodo. https://doi.org/10.5281/zenodo.20179128

### BibTeX

```bibtex
@software{pixelveg,
  author       = {[Hlubina, P., Uvackova, L.]},
  title        = {PixelVeg: Plant Image Analyser},
  year         = {[2026]},
  publisher    = {Zenodo},
  version      = {[1.0.0]},
  doi          = {10.5281/zenodo.20179128},
  url          = {https://doi.org/10.5281/zenodo.20179128}
}
```
---

## License

This work is licensed under the [MIT License](https://opensource.org/licenses/MIT).

You are free to share and adapt this material for any purpose, provided appropriate credit is given, a link to the license is included, and any changes are indicated.

---

## Part of BioCalcHub

PixelVeg is one of several plant analysis tools developed under the BioCalcHub project.

Website: [https://biocalchub.com](https://biocalchub.com)
