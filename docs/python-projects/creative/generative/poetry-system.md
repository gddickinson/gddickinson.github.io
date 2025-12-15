# poetry_system

A Python-based system for generating and analyzing poetry using natural language processing and computational creativity techniques. This system combines structured poetic forms with creative word combinations to generate unique poems while maintaining the ability to analyze existing poetry.

**[View on GitHub →](https://github.com/gddickinson/poetry_system)**

---

## Overview

**Languages:** Python

## Documentation

# Computational Poetry System

A Python-based system for generating and analyzing poetry using natural language processing and computational creativity techniques. This system combines structured poetic forms with creative word combinations to generate unique poems while maintaining the ability to analyze existing poetry.

## Features

### Poetry Generation
- Multiple poetic forms:
  - Haiku (5-7-5 syllables)
  - Free Verse
  - Custom forms
- Diverse vocabulary categories:
  - Nature words
  - Emotional expressions
  - Abstract concepts
  - Sensory details
- Creative combinations through:
  - Metaphor generation
  - Image phrase creation
  - Thematic development
  - Mood-based word selection

### Poetry Analysis
- Rhyme scheme detection
- Imagery analysis
- Sentiment analysis
- Syllable counting
- Literary device identification

## Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Required Libraries
```bash
pip install spacy textblob pronouncing numpy
python -m spacy download en_core_web_sm
```

### Setup
```bash
git clone https://github.com/yourusername/poetry-system.git
cd poetry-system
```

## Usage

### Basic Usage
```python
from core.analyzer import PoetryAnalyzer
from core.generator import PoetryGenerator

# Initialize the system
analyzer = PoetryAnalyzer()
generator = PoetryGenerator(analyzer)

# Generate a haiku
haiku = generator.generate_haiku(mood='nature')
print(haiku)

# Generate free verse
poem = generator.generate_free_verse(num_lines=4, mood='emotion')
print(poem)

# Analyze a poem
analysis = analyzer.analyze_imagery(poem)
print(analysis)
```

### Example Output

```
Generated Haiku:
lake self regret pool
courage subtle sigh jade calm
bloom fluid spicy

Generated Free Verse:
where happiness meets infinity
suffering of might rhythm
icy embrace crow faith grief marvel awe branch touch
will of delta

Analysis:
Imagery: {'sensory': ['soft', 'whisper'], 'abstract': ['whisper'], 'nature': ['autumn']}
Sentiment: {'polarity': 0

*[View full README on GitHub]*

