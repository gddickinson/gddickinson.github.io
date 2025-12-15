# object_detection_system

A comprehensive computer vision application for detecting, segmenting, and tracking objects in images and videos, with optional LLM integration for enhanced object recognition.

**[View on GitHub →](https://github.com/gddickinson/object_detection_system)**

---

## Overview

**Languages:** Python

## Documentation

# Object Detection and Tracking System

A comprehensive computer vision application for detecting, segmenting, and tracking objects in images and videos, with optional LLM integration for enhanced object recognition.

## Features

- **Object Detection**: Identify objects in images and videos using state-of-the-art models (YOLOv8, TensorFlow, CoreML)
- **Instance Segmentation**: Generate precise object outlines using Segment Anything Model (SAM)
- **Object Tracking**: Track objects across video frames with ByteTrack or SORT algorithms
- **LLM Integration**: Enhanced object recognition using Ollama (local) or Cloud APIs
- **Multi-Format Support**: Process various image and video formats
- **Hardware Optimization**: Automatic detection and utilization of available hardware (CUDA, MPS on Apple Silicon)
- **User Authentication**: Secure login system with user management
- **Plugin System**: Extensible architecture through plugins
- **Rich Visualization**: Interactive display with zooming, panning, and object highlighting

## System Requirements

- Python 3.8 or higher
- PyTorch 2.0 or higher
- OpenCV 4.7 or higher
- PyQt5 5.15 or higher
- 4GB RAM minimum (8GB+ recommended)
- NVIDIA GPU with CUDA support (optional, for acceleration)
- Apple Silicon (M1/M2/M3) for MPS acceleration (optional)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/object-detection-system.git
   cd object-detection-system
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download models:
   
   For YOLOv8:
   ```bash
   mkdir -p data/models
   # Download YOLOv8n (small)
   wget -O data/models/yolov8n.pt https://github.com/ultralytics/assets/releases/download/v0.0.0/yolov8n.pt
   ```
   
   For SAM (Segment Anything Model):
   ```bash
   # Download SAM ViT-B
   wget -O data/models/sam_vit_b_01ec64.pth https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth
   ```

## Usage

### Starting the Applica

*[View full README on GitHub]*

