# novel-genre-analysis

A comprehensive Python tool for analyzing and visualizing the evolution of literary genres throughout history. This project combines network analysis, phylogenetic tree construction, and detailed genre characteristics to provide insights into how literary genres have emerged, evolved, and influenced

**[View on GitHub →](https://github.com/gddickinson/novel-genre-analysis)**

---

## Overview

**Languages:** Python

## Documentation

# Literary Genre Evolution Analyzer

A comprehensive Python tool for analyzing and visualizing the evolution of literary genres throughout history. This project combines network analysis, phylogenetic tree construction, and detailed genre characteristics to provide insights into how literary genres have emerged, evolved, and influenced each other over time.

## Overview

The Literary Genre Evolution Analyzer is a collaboration with Anthropic's Claude AI, aiming to create a data-driven understanding of literary genre evolution. The project maps over 120 genres from ancient forms to contemporary developments, analyzing their relationships, characteristics, and evolutionary patterns.

### Key Features

- **Timeline Visualization**: Creates a network graph showing genre evolution over time
- **Phylogenetic Analysis**: Generates evolutionary trees using UPGMA clustering
- **Characteristic Analysis**: Tracks the emergence and prevalence of genre features
- **Comprehensive Genre Database**: Contains detailed information about 120+ literary genres
- **Genre Writing Guides**: Includes detailed guides for writing in specific genres

## Visualizations

The project generates two main visualizations:

1. **Timeline Graph** (`genre_timeline.png`):
   - Shows chronological evolution of genres
   - Displays parent-child relationships
   - Includes time markers for historical context

2. **Phylogenetic Tree** (`genre_phylogeny.png`):
   - Illustrates genre clustering based on similarities
   - Shows evolutionary relationships
   - Highlights genre family groupings

## Installation

```bash
git clone https://github.com/gddickinson/genre-evolution.git
cd genre-evolution
pip install -r requirements.txt
```

### Dependencies

- NetworkX
- Matplotlib
- NumPy
- Pandas
- SciPy

## Usage

```python
from genre_evolution import GenreEvolution

# Create analyzer instance
analyzer = GenreEvolution()

# Generate visualizations
analyzer.create_timeline_graph()
analyzer.create_phylogenetic_tree()


*[View full README on GitHub]*

