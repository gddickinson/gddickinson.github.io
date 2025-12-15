# direction_autocorrelation_analysis

A Python tool for analyzing directional persistence in cell migration and particle trajectories from fluorescence microscopy data.

**[View on GitHub →](https://github.com/gddickinson/direction_autocorrelation_analysis)**

---

## Overview

**Languages:** Python

## Documentation

# Autocorrelation Analysis

A Python tool for analyzing directional persistence in cell migration and particle trajectories from fluorescence microscopy data.

## Overview

This script performs autocorrelation analysis on trajectory data for fluorescently labeled proteins and cells tracked in microscope recordings. It calculates direction autocorrelation coefficients that quantify how well a cell maintains its direction of movement over time.

Key features:
- Processes individual files or entire experimental datasets
- Supports hierarchical data organization (file → condition → cross-condition analysis)
- Creates detailed visualizations of persistence measurements
- Analyzes individual tracks and condition-level aggregates
- Compares different experimental conditions
- Supports both Excel (.xlsx, .xls) and CSV (.csv) files

## Installation

### Requirements
- Python 3.6 or higher
- Required packages: numpy, pandas, matplotlib, tkinter

```bash
pip install numpy pandas matplotlib
```

## Data Requirements

The script works with cell trajectory data in CSV or Excel format with:
- Frame numbers (time points)
- X coordinates
- Y coordinates

You can organize your data in different ways:
1. **Single file** with one or more sheets (conditions)
2. **Condition folder** containing multiple files (replicates)
3. **Experiment directory** containing multiple condition folders

## Usage

### From Spyder/IDE
Modify the CONFIG section at the top of the script:

```python
# Basic parameters
INPUT_TIME_INTERVAL = 1.0    # Time between frames
INPUT_NUM_INTERVALS = 25     # Number of time intervals to analyze

# Choose ONE of these input modes:
INPUT_FILE = '/path/to/file.csv'  # Single file mode
# or
INPUT_CONDITION_DIR = '/path/to/condition_folder'  # Condition folder mode
# or
INPUT_EXPERIMENT_DIR = '/path/to/experiment_dir'   # Experiment directory mode

# Advanced options
SAVE_INDIVIDUAL_TRACKS = True  # Save track-by-track data
PLOT_INDIVIDUAL_TRACKS = True  # Create plots with 

*[View full README on GitHub]*

