# burn_index

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**[View on GitHub →](https://github.com/gddickinson/burn_index)**

---

## Overview

**Languages:** JavaScript

## Documentation

# Sentinel-2 Burn Area Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A Google Earth Engine script for detecting and analyzing burn areas using multi-temporal Sentinel-2 imagery and the Normalized Burn Ratio (NBR).

## Overview

This tool uses Sentinel-2 satellite imagery to detect and quantify areas affected by wildfire. By calculating the Normalized Burn Ratio (NBR) and comparing it across different years, the script identifies burn scars, classifies burn severity, and exports vector polygons of the affected areas.

![Burn Area Analysis Example](https://via.placeholder.com/800x400?text=Burn+Area+Analysis+Example)

## Features

- Automated processing of Sentinel-2 imagery for specified time periods
- Calculation of Normalized Burn Ratio (NBR) for burn severity assessment
- Multi-temporal change detection to identify burn scars
- Classification of burn severity into different zones
- Vector polygon generation of burn areas for further GIS analysis
- Area calculations for burn extents and hotspots

## How It Works

The script implements the following workflow:

1. **Data Acquisition**: Filters Sentinel-2 imagery by date range, cloud cover, and geographic bounds
2. **Band Selection**: Extracts relevant spectral bands for NBR calculation (NIR and SWIR2)
3. **NBR Calculation**: Computes the normalized burn ratio using the formula: NBR = (NIR - SWIR2) / (NIR + SWIR2)
4. **Change Detection**: Calculates the difference in NBR between pre-fire and post-fire images
5. **Burn Severity Classification**: Applies thresholds to identify burn severity zones (low, moderate, high)
6. **Vectorization**: Converts raster burn classes to vector polygons
7. **Area Calculation**: Computes the area of burn scars in hectares

## Requirements

- Google Earth Engine account
- Basic understanding of remote sensing and burn indices
- Access to the Google Earth Engine Code Editor

## Usage

1. Open the script in the [Google 

*[View full README on GitHub]*

