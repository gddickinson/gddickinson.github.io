# cell_curvature_analyzer

A comprehensive GUI application for analyzing the relationship between cell-membrane curvature and PIEZO1 protein locations from fluorescence microscope recordings.

**[View on GitHub →](https://github.com/gddickinson/cell_curvature_analyzer)**

---

## Overview

**Languages:** Python

## Documentation

# Cell Curvature Analyzer

A comprehensive GUI application for analyzing the relationship between cell-membrane curvature and PIEZO1 protein locations from fluorescence microscope recordings.

<!-- Image not available: Application Screenshot -->

## Features

- **Interactive Visualization**: View original images, binary masks, and analysis overlays side-by-side
- **Curvature Analysis**: Calculate three types of curvature (sign, magnitude, and normalized)
- **Intensity Correlation**: Analyze the relationship between curvature and fluorescence intensity
- **Temporal Analysis**: Track changes across frames and correlate with previous frames
- **Edge Movement Detection**: Classify cell edge regions as extending, retracting, or stable
- **Multi-tab Interface**: Dedicated views for different analysis aspects
- **Data Export**: Comprehensive export options for images, data, and reports

## Installation

### Prerequisites

- Python 3.7 or higher
- NumPy, Matplotlib, SciPy
- scikit-image
- pandas
- PyQt5
- tifffile

### Install from Source

```bash
# Clone the repository
git clone https://github.com/your-username/cell-curvature-analyzer.git
cd cell-curvature-analyzer

# Create and activate a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install the package
pip install -e .
```

### Install from PyPI

```bash
pip install cell-curvature-analyzer
```

## Usage

### Starting the Application

```bash
# If installed from source with -e flag
cell-curvature-analyzer

# Or run directly from the source directory
python cell_curvature_analyzer.py
```

### Loading Data

1. Click **Open Images** to load a microscope image stack (TIFF format)
2. Click **Open Masks** to load corresponding binary masks (TIFF format)
3. Set analysis parameters in the right panel
4. Click **Run Analysis** to process all frames

### Navigating the Interface

- **Visualization Tab**: View images and overlay analysis results
-

*[View full README on GitHub]*

