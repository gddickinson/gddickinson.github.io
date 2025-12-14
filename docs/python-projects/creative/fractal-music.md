# Fractal Music Generator

Generate unique melodies based on Mandelbrot set fractal patterns.

**GitHub:** [gddickinson/fractal_music_generator](https://github.com/gddickinson/fractal_music_generator)

---

## Overview

A creative music generation system that translates mathematical patterns from the Mandelbrot set into musical compositions. Each unique coordinate in the fractal space generates a distinct melody, creating an infinite palette of algorithmic music.

---

## Features

### Fractal-to-Music Mapping
- **Mandelbrot Set Calculation**: High-precision fractal generation
- **Pattern Recognition**: Extract musical patterns from fractal iterations
- **Coordinate-Based Generation**: Each point produces unique music
- **Infinite Variations**: Unlimited unique melodies from fractal space

### Musical Output
- **Melodic Generation**: Convert fractal patterns to notes
- **Rhythmic Patterns**: Derive timing from iteration counts
- **Harmonic Structure**: Map fractal features to musical harmony
- **Audio Synthesis**: Generate playable audio files

### Customization
- **Zoom Levels**: Explore different fractal scales
- **Coordinate Selection**: Choose specific fractal regions
- **Musical Parameters**: Adjust scales, tempo, instruments
- **Export Options**: Save as MIDI or audio files

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/fractal_music_generator.git
cd fractal_music_generator

# Install dependencies
pip install numpy matplotlib scipy midiutil

# Run the generator
python fractal_music.py
```

---

## Usage

### Basic Generation

```python
from fractal_music_generator import FractalMusicGenerator

# Create generator
generator = FractalMusicGenerator()

# Generate melody from coordinates
melody = generator.generate_from_coordinates(
    x=-0.7, 
    y=0.27015,
    zoom=1.0
)

# Export to MIDI
generator.export_midi(melody, "fractal_melody.mid")
```

### Advanced Options

```python
# Configure musical parameters
generator = FractalMusicGenerator(
    scale='major',           # Musical scale
    tempo=120,              # Beats per minute
    octave_range=(3, 6),    # Note range
    max_iterations=100      # Fractal precision
)

# Generate with custom parameters
melody = generator.generate(
    center_x=-0.5,
    center_y=0.0,
    zoom_level=2.0,
    resolution=128
)
```

---

## How It Works

### Fractal Calculation
1. Generate Mandelbrot set for specified coordinates
2. Calculate iteration counts for each point
3. Extract pattern sequences from iteration data
4. Map patterns to musical parameters

### Music Mapping Algorithm
1. **Pitch**: Iteration count modulo scale length
2. **Duration**: Normalized iteration values
3. **Velocity**: Gradient between adjacent points
4. **Timing**: Sequential processing of fractal coordinates

---

## Parameters

| Parameter | Description | Default |
|-----------|-------------|---------|
| `x, y` | Fractal coordinates | (-0.7, 0.27015) |
| `zoom` | Magnification level | 1.0 |
| `scale` | Musical scale (major, minor, pentatonic, etc.) | 'major' |
| `tempo` | BPM | 120 |
| `max_iterations` | Fractal calculation depth | 100 |
| `resolution` | Grid size for calculation | 64 |

---

## Musical Scales Supported

- Major
- Minor (Natural, Harmonic, Melodic)
- Pentatonic
- Blues
- Chromatic
- Whole Tone
- Custom scales

---

## Example Coordinates

Interesting fractal regions for music generation:

```python
# Classic Mandelbrot antenna
x=-0.75, y=0.1

# Seahorse valley
x=-0.7, y=0.27015

# Elephant valley
x=0.3, y=0.03

# Triple spiral
x=-0.7269, y=0.1889
```

---

## Output Formats

- **MIDI**: For further editing in DAW
- **WAV**: Direct audio output
- **Visualization**: Fractal pattern plots
- **Musical Notation**: Score generation (optional)

---

## Technical Stack

### Libraries
- **NumPy**: Fractal calculations
- **SciPy**: Audio processing
- **Matplotlib**: Visualization
- **MIDIUtil**: MIDI file generation
- **PyAudio** (optional): Real-time playback

---

## Applications

- **Generative Music**: Algorithmic composition
- **Ambient Soundscapes**: Evolving musical textures
- **Educational Tool**: Visualize mathematics through sound
- **Sound Design**: Unique audio material for production
- **Art Installations**: Interactive fractal music exhibits

---

## Future Enhancements

- Real-time audio generation
- 3D fractal exploration
- Additional fractal types (Julia sets, Burning Ship, etc.)
- Polyphonic harmony generation
- Interactive GUI with visual feedback
- Integration with music software via OSC/MIDI

---

*Mathematical beauty transformed into musical patterns*
