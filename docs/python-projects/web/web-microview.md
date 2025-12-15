# web_microview

A web-based microscope image viewer built with Bokeh for interactive visualization of TIFF microscopy data.

**[View on GitHub →](https://github.com/gddickinson/web_microview)**

---

## Overview

**Languages:** Python

## Documentation

# Web Microview

A web-based microscope image viewer built with Bokeh for interactive visualization of TIFF microscopy data.

![Microscope Image Viewer](https://via.placeholder.com/800x450)

## Overview

Web Microview is an interactive dashboard for visualizing and analyzing microscopy images. It provides a user-friendly interface for viewing TIFF files, navigating through image stacks, adjusting contrast, and performing basic region-of-interest (ROI) analysis.

### Features

- **TIFF File Support**: Load and view single images or multi-frame TIFF stacks
- **Interactive Visualization**: Pan, zoom, and navigate through image stacks
- **ROI Analysis**: Select regions of interest and view detailed statistics
- **Image Enhancement**: Adjust contrast with interactive controls
- **Metadata Viewer**: Examine TIFF metadata in an organized display
- **Intensity Profiling**: Visualize intensity profiles across the image (coming soon)

## Installation

### Prerequisites

- Python 3.7+
- pip

### Setup

1. Clone the repository
   ```bash
   git clone https://github.com/username/web_microview.git
   cd web_microview
   ```

2. Create and activate a virtual environment (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install the required packages
   ```bash
   pip install bokeh tifffile numpy scipy
   ```

## Usage

### Running the Application

1. Start the Bokeh server:
   ```bash
   bokeh serve --show app.py
   ```

2. The application will open in your default web browser at http://localhost:5006/app

### Using the Interface

#### Loading Images
- Click the "Choose File" button and select a TIFF file (.tif or .tiff)
- The image will automatically load and display in the main view

#### Navigating Image Stacks
- Use the "Frame" slider to move through different frames in a multi-frame TIFF stack
- The slider will only appear when a multi-frame image is loaded

#### Adjusting

*[View full README on GitHub]*

