# cell-segmenter

A PyQt-based application for segmenting and analyzing microscopy image sequences, specifically designed for DIC (Differential Interference Contrast) images from TIRF microscopy. The tool provides an interactive interface for training machine learning models to segment cellular structures.

**[View on GitHub →](https://github.com/gddickinson/cell-segmenter)**

---

## Overview

**Languages:** Python

## Documentation

# Cell Segmentation Tool

A PyQt-based application for segmenting and analyzing microscopy image sequences, specifically designed for DIC (Differential Interference Contrast) images from TIRF microscopy. The tool provides an interactive interface for training machine learning models to segment cellular structures.

## Features

- Load and view multi-frame TIFF stacks
- Interactive painting tools for creating training data
- Multiple segmentation approaches:
  - Random Forest classifier
  - Convolutional Neural Network (CNN)
- Real-time visualization of segmentation results
- Batch processing capabilities
- Training data management:
  - Multiple label classes
  - Undo/redo functionality
  - Label class editing and removal
  - Option to use training data from single or multiple frames

## Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Dependencies

```bash
pip install -r requirements.txt
```

Main dependencies include:
- PyQt6
- pyqtgraph
- numpy
- scikit-image
- scipy
- torch
- tifffile

### Installation Steps

1. Clone the repository:
```bash
git clone https://github.com/yourusername/cell-segmentation-tool.git
cd cell-segmentation-tool
```

2. Install in development mode:
```bash
pip install -e .
```

## Usage

### Starting the Application

```bash
python main.py
```

### Basic Workflow

1. **Load Data**
   - Click "Load TIFF Stack" to open your image sequence
   - The application accepts multi-frame TIFF files

2. **Create Labels**
   - Click "Add Label" to create a new label class
   - Select a color for the label
   - Create multiple labels for different cellular structures

3. **Add Training Data**
   - Select a label from the list
   - Switch to "Paint" mode
   - Paint over regions in the image to mark training data
   - Use mouse wheel or brush size control to adjust brush size
   - Navigate through frames using the frame slider

4. **Train Model**
   - Choose between Random Forest and CNN
   - Select whether to use training

*[View full README on GitHub]*

