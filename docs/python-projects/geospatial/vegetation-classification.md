# vegetation_classification

This repository contains Google Earth Engine (GEE) scripts used for the 2018 riparian vegetation mapping project of the Lower Colorado River. The project was conducted by Sound Science, LLC and used machine learning classifiers to correlate spectral characteristics of remote imagery with vegetation 

**[View on GitHub →](https://github.com/gddickinson/vegetation_classification)**

---

## Overview

**Languages:** Python, JavaScript

## Documentation

# Lower Colorado River Vegetation Mapping

This repository contains Google Earth Engine (GEE) scripts used for the 2018 riparian vegetation mapping project of the Lower Colorado River. The project was conducted by Sound Science, LLC and used machine learning classifiers to correlate spectral characteristics of remote imagery with vegetation and land types.

## Project Overview

The objective of this project was to map the vegetation and land types of the riparian region around the Lower Colorado River using remote sensing techniques. The mapping process consisted of two main components:

1. **Field Survey Data Collection**: Data was collected from 200 randomly located sites throughout the study area.
2. **Image Classification**: Using Google Earth Engine to classify vegetation/land types based on spectral signatures from various satellite and aerial imagery sources.

## Data Sources

The classification used multiple imagery and data sources:
- **Sentinel-2** satellite imagery (10m resolution)
- **National Agriculture Imagery Program (NAIP)** aerial imagery
- **LIDAR** canopy height model
- **Field survey data** collected from 200 sites

## Classification Methodology

The scripts implement two main machine learning approaches:
1. **Support Vector Machine (SVM)** classifier
2. **Random Forest** classifier

The classification distinguishes between eight different land cover classes:
1. Cottonwood/Willow
2. Tamarisk
3. Mesquite
4. Marsh/Herbaceous
5. Other (sparsely vegetated)
6. Bare Ground
7. Water
8. Other (densely vegetated)

## Repository Contents

### Training Data Preparation
- `09_03_2018 trainingPolygons *.js` - Series of scripts defining training polygons for different vegetation classes
- `upload_FusionTable.js` - Script for uploading feature collections to Earth Engine

### Classification Processing
- `11_02_2018_1Step_FINAL_MSCP_Corrections.js` - Random Forest classification implementation
- `11_02_2018_1_Step_FINAL_MSCP_Corrections_SVM.js` - SVM classifica

*[View full README on GitHub]*

