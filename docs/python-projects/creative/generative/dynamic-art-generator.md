# dynamic-art-generator

A real-time audiovisual art generation system with a plugin-based architecture. Create mesmerizing art that responds to music and sound in real-time.

**[View on GitHub →](https://github.com/gddickinson/dynamic-art-generator)**

---

## Overview

**Languages:** Python

## Documentation

# Dynamic Art Generator

A real-time audiovisual art generation system with a plugin-based architecture. Create mesmerizing art that responds to music and sound in real-time.

## Features

- **Real-time Audio Processing**: Responds to microphone input or internal audio
- **Plugin System**: Extensible architecture for different art styles
- **Interactive GUI**: Full-featured interface with parameter controls
- **Multiple Art Styles**: 
  - Pendulum Art: Paint-can style elliptical pendulum trails
  - Particle Systems: Dynamic sand/smoke-like particle effects
- **Audio Responsiveness**: Art reacts to amplitude, frequency, and beat detection
- **Parameter Tweaking**: Real-time adjustment of visual parameters

## Installation

### Prerequisites

Make sure you have Python 3.8+ installed on your system.

### Platform-Specific Setup

#### Windows
```bash
# Install Microsoft Visual C++ Build Tools if needed
# Download from: https://visualstudio.microsoft.com/visual-cpp-build-tools/
pip install -r requirements.txt
```

#### macOS
```bash
# Install portaudio using Homebrew
brew install portaudio
pip install -r requirements.txt
```

#### Linux (Ubuntu/Debian)
```bash
# Install audio development libraries
sudo apt-get update
sudo apt-get install portaudio19-dev python3-dev
pip install -r requirements.txt
```

### Quick Install
```bash
git clone [your-repo-url]
cd dynamic-art-generator
pip install -r requirements.txt
python main.py
```

## Usage

### Basic Operation

1. **Launch the Application**:
   ```bash
   python main.py
   ```

2. **Select a Plugin**: Choose from available art plugins in the dropdown menu

3. **Configure Audio**: 
   - Check "Enable Audio Input" to use your microphone
   - Make sure your microphone permissions are enabled

4. **Start Generating**: Click "Start" to begin real-time art generation

5. **Adjust Parameters**: Use the sliders and controls to modify the visual effects

### Plugin Overview

#### Pendulum Plugin
Creates flowing, paint-can-like trail

*[View full README on GitHub]*

