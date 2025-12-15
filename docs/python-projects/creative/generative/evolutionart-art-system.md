# evolutionart-art-system

This repository contains two evolutionary art generation systems that explore different approaches to computational creativity. These systems use genetic algorithms and mathematical functions to create abstract visual art that evolves over time.

**[View on GitHub →](https://github.com/gddickinson/evolutionart-art-system)**

---

## Overview

**Languages:** Python

## Documentation

# Computational Art Evolution Systems

This repository contains two evolutionary art generation systems that explore different approaches to computational creativity. These systems use genetic algorithms and mathematical functions to create abstract visual art that evolves over time.

## Overview

The repository contains two main systems:
1. Basic Evolutionary Art System (`evolutionary-art.py`)
2. Enhanced Art System (`enhanced-art-system.py`)

Both systems demonstrate different approaches to computational creativity, with the enhanced system building upon the foundations of the basic system to create more diverse and dramatic results.

## Features

### Basic Evolutionary Art System
- Generates art using mathematical functions and color theory
- Uses genetic algorithms to evolve artistic patterns
- Implements basic aesthetic measures
- Creates MIDI-like smooth transitions between generations
- Focuses on mathematical patterns and color harmony

### Enhanced Art System
- More sophisticated evolutionary algorithms
- Dynamic mutation rates
- Multiple artistic styles (geometric, organic, fluid, structured)
- Multiple moods (calm, energetic, mysterious, harmonious)
- Advanced layer combinations and transformations
- Style-specific visual effects
- More dramatic color variations
- Coordinate system transformations

## Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Required Libraries
```bash
pip install numpy Pillow deap matplotlib scipy opencv-python
```

## Usage

### Basic System
```python
# Create and run the basic evolutionary art system
art_system = EvolutionaryArt(width=800, height=800)
art_system.evolve()
```

### Enhanced System
```python
# Create and run the enhanced art system
art_system = EnhancedEvolutionaryArt(width=800, height=800)
art_system.evolve()
```

Both systems will create an `evolution_output` directory containing generated artwork from each generation.

## Technical Details

### Basic System Architecture

The basi

*[View full README on GitHub]*

