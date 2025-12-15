# bird_sound_analyzer

A real-time audio analysis application with automatic bird species detection, built in Python using PyQt5 and integrated with BirdNET.

**[View on GitHub →](https://github.com/gddickinson/bird_sound_analyzer)**

---

## Overview

**Languages:** Python

## Documentation

# Sound Analyzer with BirdNET Integration

A real-time audio analysis application with automatic bird species detection, built in Python using PyQt5 and integrated with BirdNET.

<!-- Image not available: Sound Analyzer Screenshot -->

## Features

- **Real-time Audio Visualization**: Live waveform and spectrogram visualizations
- **Automatic Bird Species Identification**: Detect bird species in real-time using BirdNET
- **Detection Database**: Store and manage bird detections with associated audio clips
- **Audio Recording**: Record and analyze audio from microphone input
- **Multiple Visualization Options**: Customizable spectrogram and waveform displays
- **File Analysis**: Load and analyze audio files
- **Data Export**: Export detection data to CSV for further analysis
- **Location Tagging**: Tag detections with geographic coordinates for mapping

## Installation

### Prerequisites

- Python 3.9+ (3.10 or 3.11 recommended)
- PyAudio (for microphone access)
- PyQt5 (for the user interface)
- NumPy and SciPy (for signal processing)
- BirdNETlib package (for bird species detection)
- psutil (for memory monitoring)

### Setup

1. Clone the repository:
   ```
   git clone https://github.com/gddickinson/sound_analyzer.git
   cd sound_analyzer
   ```

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Install BirdNET dependencies:
   ```
   pip install birdnetlib resampy librosa psutil
   ```

5. Run the application:
   ```
   python main.py
   ```

## Usage

### Main Interface

The application has four main areas:
- **Waveform Display**: Shows the audio amplitude over time
- **Spectrogram Display**: Shows the frequency content of the audio
- **BirdNET Plugin**: Controls for bird detection settings and displays results
- **Detection Database**: Manages stored bird dete

*[View full README on GitHub]*

