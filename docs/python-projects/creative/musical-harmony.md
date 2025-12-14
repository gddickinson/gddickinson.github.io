# Musical Harmony Visualization

Generate, visualize, and synthesize musical harmonies across different styles.

**GitHub:** [gddickinson/musical-harmony-visualization](https://github.com/gddickinson/muscial-harmony-visualization)

---

## Overview

A sophisticated Python system that generates, visualizes, and synthesizes musical harmonies across different musical styles. Combines music theory, audio synthesis, and creative visualization techniques to create rich, multi-sensory representations of harmonic progressions.

---

## Features

### Harmony Generation
- **Multiple Musical Styles**: Jazz, Classical, Impressionist, Modal
- **Chord Progressions**: Automatic generation of harmonic sequences
- **Voice Leading**: Smooth transitions between chords
- **Extended Harmonies**: 7ths, 9ths, 11ths, 13ths
- **Modal Harmony**: Dorian, Phrygian, Lydian, Mixolydian modes

### Musical Styles

#### Jazz
- Extended harmonies (9ths, 11ths, 13ths)
- Complex chord progressions
- Altered chords and substitutions
- ii-V-I progressions
- Tritone substitutions

#### Classical
- Traditional functional harmony
- Authentic and plagal cadences
- Suspensions and resolutions
- Secondary dominants
- Common practice progressions

#### Impressionist
- Colorful, unconventional harmonies
- Whole-tone and pentatonic scales
- Parallel chord movement
- Unresolved dissonances
- Extended tertian harmonies

#### Modal
- Sustained modal harmonies
- Modal characteristic tones
- Non-functional progressions
- Dorian, Phrygian, Lydian flavors
- Drone bass foundations

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/musical-harmony-visualization.git
cd musical-harmony-visualization

# Install dependencies
pip install numpy matplotlib scipy midiutil music21 pydub

# Run the system
python harmony_visualizer.py
```

---

## Usage

### Basic Harmony Generation

```python
from harmony_visualizer import HarmonyGenerator, Style

# Create generator
generator = HarmonyGenerator()

# Generate jazz progression
progression = generator.generate_progression(
    style=Style.JAZZ,
    length=8,
    key='C'
)

# Visualize the harmony
generator.visualize(progression, show_voice_leading=True)
```

### Audio Synthesis

```python
# Generate and synthesize
progression = generator.generate_progression(style=Style.CLASSICAL)

# Create audio
audio = generator.synthesize(
    progression,
    tempo=120,
    instrument='piano',
    duration=4.0
)

# Save audio file
audio.export("harmony.wav", format="wav")
```

### Advanced Visualization

```python
# Multiple visualization types
generator.visualize_progression(
    progression,
    views=['piano_roll', 'circle_of_fifths', 'voice_leading', 'spectrum']
)

# Animated progression
generator.create_animation(
    progression,
    filename="harmony_progression.mp4",
    fps=30
)
```

---

## Visualization Types

### 1. Piano Roll
- Horizontal time, vertical pitch
- Color-coded voices
- Duration representation

### 2. Circle of Fifths
- Harmonic relationships
- Key modulation paths
- Chord quality indicators

### 3. Voice Leading Diagram
- Individual voice movements
- Smooth/disjunct motion
- Voice crossing detection

### 4. Spectral Analysis
- Frequency content
- Harmonic overtones
- Dissonance visualization

### 5. 3D Harmony Space
- Multi-dimensional chord relationships
- Trajectory through harmonic space
- Cluster analysis

---

## Configuration

### Harmony Parameters

```python
config = {
    'style': 'jazz',           # Musical style
    'key': 'C',                # Tonic key
    'length': 8,               # Number of chords
    'tempo': 120,              # BPM
    'complexity': 'medium',    # Simple/medium/complex
    'voice_count': 4,          # Number of voices
    'register': 'mid'          # Low/mid/high
}
```

### Visualization Options

```python
viz_config = {
    'colormap': 'viridis',     # Color scheme
    'show_labels': True,       # Chord names
    'show_grid': True,         # Grid lines
    'animation': False,        # Animated view
    'resolution': (1920, 1080) # Output size
}
```

---

## Technical Implementation

### Music Theory Engine
```python
# Core components
- ChordGenerator: Create chord voicings
- ProgressionBuilder: Harmonic sequences
- VoiceLeader: Smooth voice transitions
- ScaleAnalyzer: Modal analysis
- TensionResolver: Dissonance handling
```

### Algorithms
- **Chord Voicing**: Optimal spacing algorithms
- **Voice Leading**: Minimal motion principles
- **Harmonic Function**: Roman numeral analysis
- **Dissonance Resolution**: Tendency tone handling
- **Modulation**: Key change smoothness

---

## Example Progressions

### Jazz ii-V-I

```python
progression = generator.generate_specific([
    'Dm7', 'G7', 'CM7', 'A7',
    'Dm7', 'G7', 'CM7', 'CM7'
])
```

### Classical I-IV-V-I

```python
progression = generator.generate_specific([
    'C', 'F', 'G7', 'C'
])
```

### Modal Dorian

```python
progression = generator.generate_modal(
    mode='dorian',
    tonic='D',
    length=4
)
```

---

## Audio Synthesis

### Synthesizer Options
- Piano (sampled/synthesized)
- Strings (ensemble)
- Choir (vocal pads)
- Organ (drawbar simulation)
- Custom instruments

### Effects Processing
- Reverb
- Chorus
- Delay
- EQ
- Compression

---

## Output Formats

### Visual
- PNG/JPG images
- PDF vector graphics
- SVG scalable graphics
- Animated GIF
- MP4 video

### Audio
- WAV (uncompressed)
- MP3 (compressed)
- MIDI (notation)
- OGG (compressed)

### Data
- JSON (structured data)
- MusicXML (notation)
- CSV (analysis data)

---

## Analysis Features

### Harmonic Analysis
- Roman numeral notation
- Functional harmony labels
- Dissonance measurements
- Voice leading evaluation
- Modulation detection

### Statistical Analysis
- Chord usage frequency
- Voice range statistics
- Motion type analysis
- Interval distributions

---

## API Reference

```python
class HarmonyGenerator:
    def generate_progression(style, length, key) -> Progression
    def synthesize(progression, **kwargs) -> Audio
    def visualize(progression, **kwargs) -> Figure
    def analyze(progression) -> Analysis

class Progression:
    chords: List[Chord]
    key: str
    style: Style
    
class Chord:
    notes: List[Note]
    root: str
    quality: str
    extensions: List[int]
```

---

## Use Cases

- **Music Education**: Teaching harmony principles
- **Composition**: Exploring harmonic possibilities
- **Analysis**: Understanding chord progressions
- **Performance**: Backing track generation
- **Research**: Music theory visualization
- **Creative Coding**: Generative music projects

---

## Technical Stack

- **NumPy**: Numerical operations
- **Matplotlib**: 2D/3D visualization
- **SciPy**: Audio processing
- **music21**: Music theory framework
- **MIDIUtil**: MIDI generation
- **Pydub**: Audio synthesis and export

---

## Future Development

- Real-time harmony generation
- Machine learning chord suggestion
- DAW integration (MIDI out)
- Interactive web interface
- VR/AR visualization
- Microton

al harmony support
- Style transfer between systems

---

*Visualize the beauty of harmonic progression*
