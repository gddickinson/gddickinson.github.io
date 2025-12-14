# Landscape Generator

Procedural terrain generation with multiple biomes and seasonal variations.

**GitHub:** [gddickinson/landscape-generator](https://github.com/gddickinson/landscape-generator)

---

## Overview

A sophisticated procedural landscape generator that creates realistic terrains with multiple biomes, seasonal variations, geographic features, and natural transitions. Uses advanced noise algorithms and feature placement techniques to generate natural-looking landscapes for visualization, game development, or geographic simulation.

---

## Features

### Terrain Generation
- **Multi-Octave Noise**: Perlin-like noise for natural height maps
- **Height Map Generation**: Realistic elevation profiles
- **Smooth Transitions**: Gaussian smoothing for natural blending
- **Customizable Parameters**: Full control over terrain characteristics
- **Seed-Based Generation**: Reproducible terrains

### Biome System
- **Multiple Biomes**: Ocean, beach, plains, forest, hills, mountains, snow
- **Biome Transitions**: Smooth gradients between regions
- **Elevation-Based**: Automatic biome assignment by height
- **Climate Zones**: Temperature and moisture influence
- **Voronoi Regions**: Organic biome boundaries

### Geographic Features
- **Mountains**: Realistic mountain ranges and peaks
- **Water Bodies**: Oceans, lakes, rivers
- **Forests**: Clustered vegetation systems
- **Settlements**: Procedural village/town placement
- **Road Networks**: Path-finding based road generation
- **Rivers**: Flow simulation from mountains to sea

### Seasonal Variations
- **Four Seasons**: Spring, Summer, Autumn, Winter
- **Color Palettes**: Season-specific biome colors
- **Snow Coverage**: Dynamic winter snow levels
- **Vegetation Changes**: Seasonal plant life variations
- **Temperature Maps**: Seasonal climate simulation

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/landscape-generator.git
cd landscape-generator

# Install dependencies
pip install numpy matplotlib scipy opencv-python

# Generate a landscape
python landscape_generator.py
```

---

## Usage

### Basic Generation

```python
from landscape_generator import EnhancedTerrainParams, EnhancedLandscapeGenerator, Season

# Create default parameters
params = EnhancedTerrainParams(
    size=512,
    season=Season.SUMMER,
    feature_density=0.08
)

# Generate landscape
generator = EnhancedLandscapeGenerator(params, seed=42)
generator.generate_enhanced_landscape()
```

### Custom Configuration

```python
# Detailed parameter control
params = EnhancedTerrainParams(
    size=512,                # Landscape size (pixels)
    octaves=6,              # Noise detail level
    persistence=0.5,        # Amplitude falloff
    lacunarity=2.0,         # Frequency increase
    base_frequency=4.0,     # Initial frequency
    sea_level=0.35,         # Water threshold
    mountain_level=0.7,     # Mountain threshold
    snow_level=0.85,        # Snow line elevation
    season=Season.AUTUMN,   # Current season
    feature_density=0.08    # Geographic feature density
)

generator = EnhancedLandscapeGenerator(params, seed=12345)
landscape = generator.generate_enhanced_landscape()
```

### Seasonal Comparison

```python
# Generate all four seasons
for season in [Season.SPRING, Season.SUMMER, Season.AUTUMN, Season.WINTER]:
    params.season = season
    generator = EnhancedLandscapeGenerator(params, seed=42)
    generator.generate_enhanced_landscape()
```

---

## Parameters

### Terrain Parameters

| Parameter | Range | Description | Default |
|-----------|-------|-------------|---------|
| `size` | 128-2048 | Output resolution | 512 |
| `octaves` | 1-12 | Noise layer count | 6 |
| `persistence` | 0.1-0.9 | Detail preservation | 0.5 |
| `lacunarity` | 1.5-4.0 | Frequency scaling | 2.0 |
| `base_frequency` | 1.0-10.0 | Initial noise frequency | 4.0 |

### Elevation Thresholds

| Threshold | Range | Description | Default |
|-----------|-------|-------------|---------|
| `sea_level` | 0.0-0.5 | Water cutoff | 0.35 |
| `mountain_level` | 0.6-0.9 | Mountain start | 0.7 |
| `snow_level` | 0.7-0.95 | Snow line | 0.85 |

### Feature Parameters

| Parameter | Range | Description | Default |
|-----------|-------|-------------|---------|
| `feature_density` | 0.0-0.2 | Feature placement | 0.08 |
| `settlement_count` | 0-50 | Number of settlements | Auto |
| `road_density` | 0.0-1.0 | Road network complexity | Auto |

---

## Biomes

### Biome Types
1. **Deep Ocean**: < sea_level - 0.05
2. **Shallow Ocean**: < sea_level
3. **Beach**: sea_level to sea_level + 0.05
4. **Plains**: Low elevation
5. **Forest**: Medium elevation
6. **Hills**: Medium-high elevation
7. **Mountains**: > mountain_level
8. **Snow-Capped**: > snow_level

### Seasonal Colors

Each biome has season-specific color schemes:
- **Spring**: Light greens, pastels
- **Summer**: Rich greens, vibrant colors
- **Autumn**: Oranges, browns, yellows
- **Winter**: White snow, muted colors

---

## Algorithms

### Noise Generation
- **Multi-Octave Perlin Noise**: Layered noise for detail
- **Random Phase Shifting**: Variation in patterns
- **Gaussian Smoothing**: Natural transitions
- **Rotation & Scaling**: Pattern diversity

### Feature Placement
- **Voronoi Diagrams**: Organic region generation
- **Noise Masks**: Natural feature clustering
- **Path Finding**: Realistic road networks
- **Clustering**: Settlement grouping
- **Flow Simulation**: River generation

---

## Visualization

### Output Views
1. **Height Map**: Raw elevation data (2D/3D)
2. **Biome Map**: Colored regions
3. **Seasonal View**: Season-specific colors
4. **Feature Map**: Geographic features overlay
5. **Analysis Views**: Technical debugging visuals

### 3D Rendering
```python
# Enable 3D visualization
generator.show_3d = True
generator.generate_enhanced_landscape()
```

---

## Technical Stack

### Core Libraries
- **NumPy**: Array operations and noise generation
- **Matplotlib**: 2D/3D plotting and visualization
- **SciPy**: Mathematical operations (smoothing, filtering)
- **OpenCV**: Feature mask generation
- **Pillow** (optional): Image export

### Custom Implementations
- Multi-octave noise algorithm
- Voronoi-based region generation
- Path-finding for roads
- Settlement clustering

---

## Applications

- **Game Development**: Procedural world generation
- **Geographic Simulation**: Terrain modeling
- **Art & Visualization**: Generative landscape art
- **Education**: Teaching geographic principles
- **Virtual Environments**: 3D world creation
- **Map Generation**: Fantasy/sci-fi cartography

---

## Examples

### Desert Landscape
```python
params = EnhancedTerrainParams(
    sea_level=0.2,          # Less water
    mountain_level=0.75,    # More dramatic peaks
    feature_density=0.02,   # Sparse features
    season=Season.SUMMER
)
```

### Alpine Region
```python
params = EnhancedTerrainParams(
    mountain_level=0.6,     # More mountains
    snow_level=0.75,        # Lower snow line
    feature_density=0.12,   # More features
    season=Season.WINTER
)
```

### Island Chain
```python
params = EnhancedTerrainParams(
    sea_level=0.4,          # More ocean
    base_frequency=6.0,     # Smaller landmasses
    octaves=8,              # More detail
    season=Season.SUMMER
)
```

---

## Export Options

```python
# Save as image
generator.save_image("landscape.png")

# Export height map
generator.export_heightmap("heightmap.npy")

# Export biome data
generator.export_biomes("biomes.json")

# Generate animation (seasonal cycle)
generator.create_season_animation("seasons.gif")
```

---

## Future Enhancements

- Erosion simulation
- Weather system integration
- Dynamic day/night cycles
- Flora/fauna placement
- Geological layer simulation
- Real-time generation
- Unity/Unreal Engine export

---

*Generate infinite unique terrains with procedural algorithms*
