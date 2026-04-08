# 🛰️ Sentinel-2 Satellite Image Processing Pipeline

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Rasterio](https://img.shields.io/badge/Rasterio-GIS_Processing-4CAF50)
![Copernicus](https://img.shields.io/badge/Data-Copernicus_Ecosystem-0033A0)

> **An end-to-end Python pipeline for transforming RAW satellite imagery from the Copernicus Data Space Ecosystem into analysis-ready products for environmental monitoring, agriculture, and disaster management.**

---

## 🎯 Executive Summary

This project implements a comprehensive workflow for processing raw Sentinel-2 satellite data. Utilizing Python and Google Colab, the pipeline handles everything from multi-spectral band ingestion (JP2 format) to advanced radiometric corrections, geometric transformations, and the computation of vital environmental indices. 

---

## 🚀 Core Capabilities

- 📥 **Data Acquisition & Setup:** Processing multi-spectral bands in JP2 (JPEG2000) format extracted directly from the Copernicus platform.
- 👁️ **Visualization & Inspection:** Generating grayscale maps and True-Color (RGB) composites using `rasterio` and `matplotlib`.
- 🛠️ **Quality Control & Metadata Validation:** Rigorous checks on spatial resolution, Coordinate Reference Systems (CRS), and raw data consistency.
- 🚨 **Error Identification & Correction:** - Handling `nodata` values and out-of-bounds pixels.
  - Mitigating sensor anomalies and geometric distortions.
- 🌍 **Geospatial Processing:** Georeferencing and CRS reprojection for accurate spatial alignment.
- 🌿 **Spectral Indices Calculation:** Advanced map algebra to compute:
  - **NDVI** (Normalized Difference Vegetation Index)
  - **RVI** (Ratio Vegetation Index)
  - **SAVI** (Soil Adjusted Vegetation Index)
  - **TVI** (Transformed Vegetation Index)
  - **BAI** (Burned Area Index)
- 🎨 **Image Transformations & Enhancements:**
  - Histogram generation and equalization.
  - Linear contrast stretching and tail clipping.
  - Spatial filtering (Smoothing, Sharpening, Sobel edge detection).
  - Image scaling and pixel masking.

---

## 📂 Project Structure

    sentinel2_image_processing/
    ├── notebooks/
    │   └── 01_sentinel2_processing_pipeline.ipynb  # Main Google Colab workflow
    ├── data/
    │   └── raw/                                    # Placeholder for JP2 Copernicus files
    ├── assets/
    │   └── rgb_composite_example.png               # Example output
    └── README.md

---

## ⚙️ Getting Started

### Prerequisites
Since this pipeline is designed to run on **Google Colab**, no local installation is strictly required. However, you will need to download the raw satellite imagery.

### 1. Data Acquisition
To work with the pipeline, you must first obtain the RAW Sentinel-2 imagery:
1. Create a free account on the [Copernicus Data Space Ecosystem](https://dataspace.copernicus.eu/).
2. Define your Region of Interest (ROI) and search for Sentinel-2 L1C or L2A products.
3. Download the `.zip` file containing the `.jp2` multi-spectral bands.
4. Upload the necessary bands (e.g., B02, B03, B04 for RGB, B08 for NIR) to your Google Drive or Colab session.

### 2. Running the Pipeline
Open the notebook in Google Colab and install the required geospatial dependencies:
```python
!pip install rasterio numpy pandas matplotlib
```

Run the cells sequentially to load the bands, apply the corrections, and compute the vegetation indices.

---

## 🧠 Tech Stack

- **Environment:** Google Colab / Jupyter Notebooks
- **Programming Language:** Python 3
- **Geospatial & Image Processing:** `rasterio`
- **Data Manipulation:** `numpy`, `pandas`
- **Data Visualization:** `matplotlib`

---

## 📌 Author

**Francisco Javier Gómez Pulido** *Data Scientist & Machine Learning Engineer*

- 📧 Email: [frangomezpulido2002@gmail.com](mailto:frangomezpulido2002@gmail.com)
- 💼 LinkedIn: [linkedin.com/in/frangomezpulido](https://www.linkedin.com/in/frangomezpulido)
- 🐙 GitHub: [github.com/fragompul](https://github.com/fragompul)

---
*If you found this Earth Observation project useful, please consider leaving a ⭐ on the repository!*
