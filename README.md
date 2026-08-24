# PlantHyper: Hybrid MLP Inversion for Hyperspectral Biophysical Trait Retrieval

This repository contains the official code, dataset processing scripts, benchmark evaluation metrics, and figure generation pipelines for our submission to *Electronic Letters on Computer Vision and Image Analysis* (ELCVIA).

## 📌 Repository Overview

The code provided here enables full end-to-end reproducibility of the figures, tables, and spatial retrieval maps presented in Section 4 of the manuscript:

* **Model Architecture**: Multi-Layer Perceptron (MLP) hybrid inversion with standard feature scaling and PCA bottleneck reduction ($n=15$).
* **Target Traits**: Leaf Area Index ($\text{LAI}$), Canopy Chlorophyll Content ($\text{C}_{ab}$), Equivalent Water Thickness ($\text{C}_w$), and Canopy Dry Matter ($\text{C}_m$).
* **Spatial Processing**: EnMAP Level-2A BOA reflectance raster ingestion, vegetation masking ($\text{NDVI} \ge 0.30$), spatial feature rendering, and publication-ready cartographic export.

---

## 📁 Repository Structure

```text
├── main.py                                      # Master script for tables & 600 DPI figure generation
├── insitu_data.csv                              # Validation ground data (n = 112 sample points)
├── data/
│   └── ENMAP01-____L2A-SPECTRAL_IMAGE.bsq       # EnMAP BOA spectral image (subset sample)
├── outputs/
│   ├── Table_4_Algorithmic_Performance.csv      # Comparative metrics (SVR vs. RFR vs. PlantHyper)
│   ├── Table_5_Residual_Analysis.csv           # Detailed residual & error driver breakdown
│   ├── Figure_4_1_LAI_Scatter.pdf               # LAI validation scatter plot (Vector & PNG)
│   ├── Figure_4_2_Cab_Scatter.pdf               # Cab validation scatter plot (Vector & PNG)
│   ├── Figure_4_3_Pandamatenga_Spatial_Workflow.pdf
│   └── Figure_4_3_PlantHyper_Retrieved_Biophysical_Trait_Maps_ELCVIA.pdf
├── requirements.txt                             # Dependencies manifest
└── README.md                                    # Repository documentation
