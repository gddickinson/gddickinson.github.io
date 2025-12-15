# geospatial_image_segmenter

A Python-based desktop application for segmenting and classifying geospatial imagery using machine learning. This tool provides an interactive interface for working with satellite imagery, aerial photography, and LIDAR data, allowing users to create training data, train models, and perform segmentat

---

## Overview

**Languages:** Python

## Documentation

# Geospatial Image Segmentation Tool

A Python-based desktop application for segmenting and classifying geospatial imagery using machine learning. This tool provides an interactive interface for working with satellite imagery, aerial photography, and LIDAR data, allowing users to create training data, train models, and perform segmentation/classification tasks.

## Features

- **Multi-layer Support**
  - Raster layers (GeoTIFF, etc.)
  - Vector layers (Shapefile, GeoJSON)
  - LIDAR point clouds (LAS/LAZ)
  - OpenStreetMap and other base maps

- **Interactive Training Data Creation**
  - Paint-based interface for pixel selection
  - Multiple label support with custom colors
  - Real-time visualization of training areas

- **Advanced Analysis**
  - Spectral index calculation (NDVI, NDWI, etc.)
  - Texture feature extraction
  - Terrain analysis for elevation data

- **Machine Learning Integration**
  - Random Forest classifier
  - Convolutional Neural Networks (CNN)
  - Custom feature extraction pipeline

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/geospatial-segmentation-tool.git
cd geospatial-segmentation-tool
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Dependencies

- Python 3.8+
- PyQt6
- NumPy
- Rasterio
- Geopandas
- Scikit-learn
- PyTorch (for CNN models)
- GDAL

## Usage

1. Launch the application:
```bash
python main.py
```

2. Import data:
   - Use File > Import to load raster, vector, or LIDAR data
   - Supported formats include GeoTIFF, Shapefile, LAS/LAZ

3. Create training data:
   - Enable training mode from the toolbar
   - Open the Label Manager
   - Create labels and assign colors
   - Hold Shift + Left Click to paint training areas

4. Train models:
   - Select desired model type (Random Forest/CNN)
   - Configure model parameter

*[View full README on GitHub]*

