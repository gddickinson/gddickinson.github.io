# deep_particle_tracking

A Python application for deep learning-based particle tracking in microscopy images.

**[View on GitHub →](https://github.com/gddickinson/deep_particle_tracking)**

---

## Overview

**Languages:** Python

## Documentation

# Deep Particle Tracker

A Python application for deep learning-based particle tracking in microscopy images.

## Overview

Deep Particle Tracker is a comprehensive tool for detecting and tracking fluorescent particles in microscopy image sequences using deep learning. The application integrates:

- Simulation of realistic microscopy data
- Neural network training for particle detection
- Tracking of particles across frames
- Visualization of results

The application leverages the power of convolutional neural networks, particularly U-Net architectures with ConvLSTM layers, to process multiple frames simultaneously for improved detection and tracking.

## Features

- **Data Simulation**: Generate realistic particle data with various motion models, PSF types, and noise characteristics
- **Model Training**: Train deep learning models on simulated or experimental data
- **Prediction**: Apply trained models to detect particles and track them across frames
- **Visualization**: Interactive visualization of results with tracks and probability maps
- **User-Friendly GUI**: Intuitive interface for all operations

## Installation

### Requirements

- Python 3.7 or newer
- PyTorch 1.7 or newer
- PyQt5 for the GUI
- Various scientific Python packages (numpy, scipy, matplotlib, etc.)

### Installation Steps

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/deep_particle_tracker.git
   cd deep_particle_tracker
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Install the package:
   ```
   pip install -e .
   ```

## Usage

### Starting the Application

Run the following command to start the application:

```
python main.py
```

Or if installed via pip:

```
deep_particle_tracker
```

### Command Line Options

- `--debug`: Enable debug logging
- `--cpu`: Force CPU mode (disable GPU)

### Using the GUI

The application has three main tabs:

1. **Simulation**: Create simulated particle data
2. **Training**: Train model

*[View full README on GitHub]*

