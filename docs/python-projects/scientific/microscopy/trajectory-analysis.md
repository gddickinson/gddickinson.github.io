# trajectory_analysis

A comprehensive, modular application for analyzing particle trajectories from TIRF microscopy recordings and other single-molecule imaging data.

**[View on GitHub →](https://github.com/gddickinson/trajectory_analysis)**

---

## Overview

**Languages:** Python

## Documentation

# Particle Tracking Application

A comprehensive, modular application for analyzing particle trajectories from TIRF microscopy recordings and other single-molecule imaging data.

## Features

### 🔬 **Multi-Method Particle Detection**
- Threshold-based detection
- Laplacian of Gaussian (LoG) blob detection
- Trackpy integration
- Background subtraction and filtering

### 🔗 **Advanced Trajectory Linking**
- Nearest neighbor linking
- Trackpy-based linking with gap filling
- Adaptive search parameters
- Minimum track length filtering

### 📊 **Comprehensive Feature Analysis**
- Radius of gyration (simple and tensor methods)
- Asymmetry, skewness, kurtosis
- Fractal dimension
- Mean squared displacement (MSD)
- Velocity and diffusion analysis
- Nearest neighbor distances

### 🤖 **Machine Learning Classification**
- SVM-based trajectory classification
- Threshold-based mobility classification
- Custom feature selection
- Training data import

### 📈 **Interactive Visualization**
- Real-time image display with overlays
- Track visualization with customizable colors
- Feature-based coloring schemes
- Playback controls for time series
- Export capabilities

### 💼 **Project Management**
- Save and load analysis projects
- Parameter persistence
- Data file management
- Analysis result tracking

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Install from PyPI (when available)
```bash
pip install particle-tracker
```

### Install from Source
```bash
git clone https://github.com/yourusername/particle-tracker.git
cd particle-tracker
pip install -e .
```

### Development Installation
```bash
git clone https://github.com/yourusername/particle-tracker.git
cd particle-tracker
pip install -e ".[dev,docs,optional]"
```

## Quick Start

### GUI Application
```bash
# Start the application
particle-tracker

# Or run directly
python main.py

# With debug logging
python main.py --debug

# Load a project on startup
python main.py --project my_analysis.ptpr

*[View full README on GitHub]*

