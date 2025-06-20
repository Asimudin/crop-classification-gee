# 🌾 Crop Classification with Google Earth Engine

This project uses Sentinel-2 surface reflectance data and the Google Earth Engine Python API to classify agricultural land into three classes: **Corn**, **Soybeans**, and **Fallow/Other**. It leverages **monthly composites**, **vegetation indices (NDVI & EVI)**, and a **Random Forest classifier** for time-series-based crop mapping over an Iowa AOI.

---

## 📌 Project Objectives

- Build a robust crop classification pipeline using Sentinel-2 imagery.
- Use spectral bands and vegetation indices as features.
- Apply Random Forest for supervised classification.
- Evaluate model accuracy with an independent test set.
- Visualize results with custom legends and GEE-based map rendering.

---

## 🛰️ Data & Area of Interest

- **Satellite**: Sentinel-2 Surface Reflectance (S2_SR_HARMONIZED)
- **Bands Used**: B2 (Blue), B3 (Green), B4 (Red), B8 (NIR)
- **Indices**: NDVI, EVI
- **Location**: Iowa, USA
- **Year**: 2021
- **Months Considered**: April to September (growing season)

---

## 🧪 Methodology Overview

1. **AOI Definition**: Define a rectangular AOI over Iowa.
2. **Ground Truth Simulation**: Create labeled polygons for each crop class.
3. **Image Processing**:
   - Filter Sentinel-2 images by date and cloud cover.
   - Apply cloud masking.
   - Compute NDVI and EVI.
   - Create monthly median composites.
4. **Feature Stack Creation**: Stack selected bands and indices across months.
5. **Sampling & Splitting**: Sample points from the AOI and split into training/testing sets.
6. **Model Training**: Train a Random Forest classifier using 50 trees.
7. **Evaluation**: Compute accuracy and Kappa score using an independent test set.
8. **Visualization**: Render classification map and add a custom legend using `geemap`.

---

## 📊 Output

- 📍 Classified map showing Corn, Soybeans, and Fallow/Other
- ✅ Accuracy and Kappa coefficient from error matrix
- 🗺️ Interactive Earth Engine map with color-coded legend

---

## 🔧 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/crop-classification-gee.git
cd crop-classification-gee
