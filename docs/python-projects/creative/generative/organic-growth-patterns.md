# organic-growth-patterns

A Python-based cellular automaton system that generates and visualizes organic growth patterns inspired by natural phenomena like coral, lichen, and mycelium growth. The system combines cellular automata rules with environmental factors to create visually striking and biologically-inspired patterns.

**[View on GitHub →](https://github.com/gddickinson/organic-growth-patterns)**

---

## Overview

**Languages:** Python

## Documentation

# Organic Pattern Generator

A Python-based cellular automaton system that generates and visualizes organic growth patterns inspired by natural phenomena like coral, lichen, and mycelium growth. The system combines cellular automata rules with environmental factors to create visually striking and biologically-inspired patterns.

## Features

### Multiple Growth Patterns
- **Coral Growth**: Branching patterns with yellow-orange-red coloring
- **Lichen Growth**: Spreading patterns with yellow-green visualization
- **Mycelium Growth**: Network-like patterns with copper tones

### Seeding Methods
- Random distribution
- Center-point growth
- Linear initialization

### Environmental Factors
- Light gradients (radial influence)
- Moisture gradients (vertical influence)
- Customizable environmental effects

### Visualization
- Real-time pattern development tracking
- Custom color schemes for each pattern type
- High-resolution output images
- Progress tracking and statistics

## Installation

### Prerequisites
```bash
Python 3.7 or higher
```

### Required Libraries
```bash
pip install numpy matplotlib scipy opencv-python
```

### Setup
```bash
git clone https://github.com/yourusername/organic-pattern-generator.git
cd organic-pattern-generator
```

## Usage

### Basic Usage
```python
from organic_patterns import OrganicPatternGenerator

# Create a generator
generator = OrganicPatternGenerator(width=100, height=100)

# Initialize with random seeding
generator.seed_random(density=0.3)

# Grow the pattern
for i in range(30):
    generator.grow(pattern_type='coral')
    
# Visualize the result
generator.visualize(save_path='coral_pattern.png')
```

### Pattern Types
Each pattern type has unique growth characteristics:

```python
# Coral pattern
generator.grow(pattern_type='coral')    # Branching growth

# Lichen pattern
generator.grow(pattern_type='lichen')   # Spreading growth

# Mycelium pattern
generator.grow(pattern_type='mycelium') # Network growth
```

### Seeding Method

*[View full README on GitHub]*

