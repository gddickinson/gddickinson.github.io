# Synapse

A FLIKA plugin for 3D cluster analysis of superresolution microscopy data, with a focus on synaptic protein organization.

**[View on GitHub →](https://github.com/gddickinson/Synapse)**

---

## Overview

**Languages:** Unknown

## Documentation

# Synapse3D

A FLIKA plugin for 3D cluster analysis of superresolution microscopy data, with a focus on synaptic protein organization.

## Overview

Synapse3D provides tools for analyzing the spatial organization and clustering of synaptic proteins using superresolution microscopy data. The plugin enables:

- 3D visualization and analysis of protein localizations
- DBSCAN-based cluster detection in 3D
- Analysis of spatial relationships between protein clusters
- Quantification of cluster properties (volume, density, etc.)
- Statistical analysis of cluster distributions
- Batch processing capabilities

## Features

- **3D Data Visualization**: Interactive 3D visualization of protein localizations and clusters
- **Cluster Detection**: DBSCAN-based clustering algorithm optimized for 3D protein distribution analysis
- **Dual Channel Analysis**: Compare and analyze relationships between two protein channels
- **ROI Analysis**: Define and analyze regions of interest in 2D and 3D
- **Statistical Tools**: Built-in tools for analyzing cluster distributions and spatial relationships
- **Batch Processing**: Process multiple datasets with consistent parameters
- **Data Export**: Export analysis results in CSV format for further processing

## Installation

### Requirements

- FLIKA (http://flika-org.github.io/)
- Python 3.x
- PyQt5
- numpy
- scipy
- scikit-learn
- pandas
- pyqtgraph

### Dependencies

The following Python packages are required:

```
numpy
scipy
pandas
scikit-learn
PyQt5
pyqtgraph
```

### Installing the Plugin

1. Install FLIKA following the instructions at http://flika-org.github.io/
2. Clone this repository:
```bash
git clone https://github.com/username/Synapse3D.git
```
3. Add the plugin directory to your FLIKA plugins folder

## Usage

### Basic Workflow

1. Launch FLIKA and enable the Synapse3D plugin
2. Load your localization data (supported format: .txt files with x,y,z coordinates)
3. Select analysis parameters:
   - Clustering distance (eps)
   - Mini

*[View full README on GitHub]*

