# PlantHyper: Hybrid MLP Inversion for Hyperspectral Biophysical Trait Retrieval

This repository contains the official code, dataset processing scripts, benchmark evaluation metrics, and figure generation pipelines for our submission to *Electronic Letters on Computer Vision and Image Analysis* (ELCVIA).

## 📌 Repository Overview

The code provided here enables full end-to-end reproducibility of the figures, tables, and spatial retrieval maps presented in Section 4 of the manuscript:

* **Model Architecture**: Multi-Layer Perceptron (MLP) hybrid inversion with standard feature scaling and PCA bottleneck reduction ($n=15$).
* **Target Traits**: Leaf Area Index ($\text{LAI}$), Canopy Chlorophyll Content ($\text{C}_{ab}$), Equivalent Water Thickness ($\text{C}_w$), and Canopy Dry Matter ($\text{C}_m$).
* **Spatial Processing**: EnMAP Level-2A BOA reflectance raster ingestion, vegetation masking ($\text{NDVI} \ge 0.30$), spatial feature rendering, and publication-ready cartographic export.

---

## 📁 Repository Structure

## 📁 Repository Structure


EnMAP-PlantHyper-Retrieval/
├── data/                  # Field validation dataset
│   └── insitu_data.csv    # In situ canopy & leaf trait ground truth
├── outputs/               # Pipeline execution results
│   ├── figures/           # Generated validation plots & manuscript figures
│   └── trait_maps/        # Predicted biophysical parameter maps
├── src/                   # PlantHyper main pipeline modules
│   │   ├── pipeline.py        # Core PlantHyper inversion and workflow logic
│   ├── preprocessing.py   # Spectral calibration and in situ data alignment
│   └── evaluation.py     # Accuracy metrics (RMSE, R², MAE) computation
├── .gitignore             # Ignores large .bsq rasters and temporary files        
├── README.md              # Project overview, installation, and Zenodo DOI
└── requirements.txt       # Python package dependencies

## 📥 Data Download & Setup
The raw EnMAP hyperspectral dataset (`ENMAP01-____L2A-SPECTRAL_IMAGE.bsq`) is hosted on Zenodo:
[![DOI]( https://doi.org/10.5281/zenodo.22078009)

1. Download the `.bsq` file from the Zenodo link above.
2. Place it in the `data/` folder of this repository before running `main.py`.
