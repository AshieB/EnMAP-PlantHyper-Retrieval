# PlantHyper: Spaceborne EnMAP Biophysical Trait Retrieval Pipeline

This repository contains the official Python implementation of the **PlantHyper** deep hybrid MLP architecture for estimating crop biophysical parameters from spaceborne EnMAP hyperspectral imagery. The pipeline extracts spectral signatures at in-situ ground-truth locations, trains baseline machine learning regressors alongside PlantHyper, and exports pixel-wise continuous raster maps across agricultural study sites.

## Target Biophysical Variables

* **LAI:** Leaf Area Index ($\text{m}^2\ \text{m}^{-2}$)
* **Cab:** Leaf Chlorophyll Content ($\mu\text{g}\ \text{cm}^{-2}$)
* **Cm:** Leaf Dry Matter Content ($\text{g}\ \text{cm}^{-2}$)
* **Cw:** Canopy Equivalent Water Thickness ($\text{cm}$)

---

## Repository Structure

```text
├── data/
│   ├── ENMAP01-____L2A-...-SPECTRAL_IMAGE.bsq   # EnMAP L2A hyperspectral scene (not tracked in Git)
│   └── insitu_data.csv                          # In-situ ground truth validation measurements
├── outputs/                                     # Exported high-resolution figures and rasters
├── src/
│   └── main_pipeline.py                         # Spectral extraction, model training, and extrapolation script
├── .gitignore                                   # Excludes large imagery rasters and outputs
├── requirements.txt                             # Python package dependencies
└── README.md                                    # Project documentation
