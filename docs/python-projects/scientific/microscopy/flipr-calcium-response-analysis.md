# flipr-calcium-response-analysis

1. [Introduction](#introduction)

**[View on GitHub →](https://github.com/gddickinson/flipr-calcium-response-analysis)**

---

## Overview

**Languages:** Python

## Documentation

# FLIPR Analysis Tool User Manual

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Getting Started](#getting-started)
4. [Main Interface](#main-interface)
5. [Loading Data](#loading-data)
6. [Plate Layout Configuration](#plate-layout-configuration)
7. [Experiment Metadata](#experiment-metadata)
8. [Data Analysis](#data-analysis)
9. [Diagnostic Analysis](#diagnostic-analysis)
10. [Visualization](#visualization)
11. [Exporting Results](#exporting-results)
12. [Troubleshooting](#troubleshooting)

## Introduction

The FLIPR Analysis Tool is a specialized software application designed for analyzing calcium imaging data from FLIPR (Fluorometric Imaging Plate Reader) experiments. It provides a comprehensive suite of tools for data processing, visualization, analysis, and diagnostic evaluation of calcium responses in 96-well plate formats.

### Key Features
- Interactive 96-well plate layout configuration
- Raw and ΔF/F₀ trace visualization
- Automated artifact removal
- Statistical analysis with multiple metrics
- Ionomycin normalization capability
- Comprehensive data export options
- Area Under Curve (AUC) analysis
- Time to peak measurements
- Direct import from FLIPR CSV output
- Experiment metadata tracking
- Diagnostic analysis for clinical applications
- Customizable quality control parameters

## Installation

### System Requirements
- Python 3.9 or later
- Required libraries:
  - PyQt5
  - pandas
  - numpy
  - pyqtgraph
  - openpyxl
  - matplotlib

### Installation Steps
1. Install Python from https://www.python.org/downloads/
2. Install required packages using pip:
```bash
pip install PyQt5 pandas numpy pyqtgraph openpyxl matplotlib
```
3. Download and run the FLIPR Analysis Tool script

## Getting Started

### Initial Setup
1. Launch the application
2. Configure analysis parameters (Analysis → Parameters)
3. Load your FLIPR data file
4. Configure your plate layout before analysis
5. Set up diagnosis parameters if perfor

*[View full README on GitHub]*

