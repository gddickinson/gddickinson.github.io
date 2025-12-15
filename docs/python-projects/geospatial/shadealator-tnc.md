# Shadealator_TNC

A collection of ArcGIS Python scripts for stream temperature modeling and riparian shade analysis using the Shade-a-lator model.

**[View on GitHub →](https://github.com/gddickinson/Shadealator_TNC)**

---

## Overview

**Languages:** Python

## Documentation

# TTools & Shade-a-lator

A collection of ArcGIS Python scripts for stream temperature modeling and riparian shade analysis using the Shade-a-lator model.

## Overview

This repository contains Python scripts and tools for running the Shade-a-lator model from within ArcGIS. The Shade-a-lator model was originally developed by Y.D. Chen and the Oregon Department of Environmental Quality (ODEQ) as part of their HeatSource model version 6. This implementation interfaces with ArcGIS using TTools (also developed by ODEQ) to estimate input values for shade calculations from GIS data.

The workflow consists of several sequential steps that:
1. Process stream centerlines and banks
2. Create observation points (nodes) along streams
3. Sample topographic and vegetation characteristics
4. Calculate shade conditions using the Shade-a-lator model
5. Export results back to ArcGIS

## System Requirements

- ArcGIS 10.3.1 or higher (tested on ArcGIS 10.3.1)
- Python 2.7 (specifically the version installed with ArcGIS)
- Microsoft Excel (with macros enabled)
- Required Python packages:
  - openpyxl
  - pypiwin32 (for Excel automation)
  - xlrd
  - Other standard libraries (numpy, math, etc.)

## Installation

1. Clone or download this repository
2. Ensure you have the required Python packages installed in ArcGIS's Python environment:

```bash
cd C:\Python27\ArcGIS10.x\Scripts
pip.exe install openpyxl pypiwin32
```

3. Add Georges_Tools.tbx to your ArcMap toolbox

## Required Input Data

- Stream centerline feature class (with fields: OBJECTID, Shape, Shape_Length, Id)
- Right bank feature class (with fields: OBJECTID, Shape, Shape_Length, LEFT_FID, RIGHT_FID)
- Left bank feature class (with fields: OBJECTID, Shape, Shape_Length, LEFT_FID, RIGHT_FID)
- Elevation raster (e.g., LiDAR DEM)
- Land cover/vegetation height raster

## Workflow Steps

### Step 1: Segment Stream (Step1_SegmentStream.py)
Creates evenly spaced nodes along the stream centerline with unique IDs.

### Step 2: Measu

*[View full README on GitHub]*

