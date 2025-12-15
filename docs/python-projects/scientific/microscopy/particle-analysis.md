# particle_analysis

ParticleAnalysis is an open-source Python application for detecting, tracking, and analyzing fluorescent particles in microscopy image sequences. It provides a user-friendly graphical interface for analyzing single-particle dynamics, with particular emphasis on robust particle detection, reliable tr

**[View on GitHub →](https://github.com/gddickinson/particle_analysis)**

---

## Overview

**Languages:** Python

## Documentation

# ParticleAnalysis: A Python Tool for Single-Particle Tracking in Fluorescence Microscopy

## Overview

ParticleAnalysis is an open-source Python application for detecting, tracking, and analyzing fluorescent particles in microscopy image sequences. It provides a user-friendly graphical interface for analyzing single-particle dynamics, with particular emphasis on robust particle detection, reliable tracking, and comprehensive motion analysis.

## Key Features

- **Advanced Particle Detection**
  - Multi-scale Gaussian detection for varying particle sizes
  - Local background subtraction and noise estimation
  - SNR-based filtering of detections
  - Interactive ROI selection and parameter tuning

- **Robust Particle Tracking**
  - Nearest-neighbor linking algorithm with gap closing
  - Support for particle disappearance and reappearance
  - Track quality control and filtering
  - Visualization of tracking results

- **Comprehensive Motion Analysis**
  - Mean Square Displacement (MSD) analysis
  - Diffusion coefficient calculation
  - Motion type classification (confined, normal, directed, anomalous)
  - Track shape analysis (radius of gyration, asymmetry, fractal dimension)

- **User-Friendly Interface**
  - Interactive visualization of particles and tracks
  - Real-time parameter adjustment
  - Results tables with sorting and filtering
  - Batch processing capabilities

## Installation

```bash
# Create a new conda environment
conda create -n particle_analysis python=3.11
conda activate particle_analysis

# Install dependencies
pip install -r requirements.txt

# Install the package
pip install .
```

## Quick Start

1. Launch the application:
```bash
python -m particle_analysis
```

2. Load data:
   - Click "Open File" to load a TIFF stack
   - Adjust contrast using the histogram sliders
   - Select a region of interest (optional)

3. Detect and track particles:
   - Adjust detection parameters if needed
   - Click "Detect Particles" to identify particles
   - Click

*[View full README on GitHub]*

