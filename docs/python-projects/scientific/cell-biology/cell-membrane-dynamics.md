# cell_membrane_dynamics

A Python-based application for analyzing PIEZO1 protein distribution and membrane dynamics using TIRF microscopy data.

**[View on GitHub →](https://github.com/gddickinson/cell_membrane_dynamics)**

---

## Overview

**Languages:** Python

## Documentation

# PIEZO1 Membrane Dynamics Tracker

A Python-based application for analyzing PIEZO1 protein distribution and membrane dynamics using TIRF microscopy data.

<!-- Image not available: Application Screenshot -->

## Overview

This tool enables simultaneous analysis of membrane dynamics, curvature, and PIEZO1 protein distribution along cell edges using Total Internal Reflection Fluorescence (TIRF) microscopy data. It processes two types of image sequences:

1. Binary segmented images showing cell position (cell mask)
2. Fluorescence recordings of PIEZO1 protein distribution

The application provides a powerful interface for investigating the relationship between membrane movement, curvature, and protein localization.

## Features

### Dynamics Analysis
- Tracks membrane movement between consecutive frames
- Classifies movement as expanding, retracting, flowing, or stationary
- Calculates velocity vectors and movement magnitudes
- Visualizes movement patterns with color-coded vectors

### Curvature Analysis
- Calculates local membrane curvature using circular arc fitting
- Maps curvature along the entire cell edge
- Correlates curvature with membrane dynamics and protein intensity
- Supports multiple curvature calculation methods

### Temporal Analysis
- Processes entire time-series sequences
- Creates kymographs to track specific membrane regions over time
- Analyzes correlation coefficients across frames
- Tracks movement class distributions throughout sequences

### Visualization Options
- Multi-tab interface with specialized views
- Real-time visualization updates when changing parameters
- Color-coding for different movement types and curvature values
- Export options for data and figures

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/piezo1-dynamics-tracker.git
cd piezo1-dynamics-tracker
```

2. Create and activate a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts

*[View full README on GitHub]*

