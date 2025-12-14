# Color Palette Generator

Generate harmonious color combinations using color theory principles.

**GitHub:** [gddickinson/colour-palette](https://github.com/gddickinson/colour-palette)

---

## Overview

A creative color palette generator that creates harmonious color combinations using established color theory principles. Produces both visual representations and detailed color data, perfect for designers, artists, and developers seeking professional color schemes.

---

## Features

### Color Harmony Types
- **Complementary**: Opposite colors on the color wheel
- **Analogous**: Adjacent colors for natural schemes
- **Triadic**: Three evenly-spaced colors
- **Tetradic**: Four colors in two complementary pairs
- **Split-Complementary**: Base color with two adjacent to complement
- **Monochromatic**: Variations of a single hue

### Temperature Control
- **Warm Palettes**: Reds, oranges, yellows
- **Cool Palettes**: Blues, greens, purples
- **Neutral Palettes**: Balanced temperature
- **Custom Temperature**: Fine-grained control

### Palette Features
- **Automatic Generation**: Based on color theory rules
- **Seed Control**: Reproducible palettes
- **Multiple Formats**: RGB, HSV, HEX, CMYK
- **Visual Output**: Beautiful palette visualizations
- **Detailed Analysis**: Color relationships and metrics

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/colour-palette.git
cd colour-palette

# Install dependencies
pip install numpy matplotlib colormath Pillow

# Run the generator
python color_palette_generator.py
```

---

## Usage

### Basic Generation

```python
from color_palette_generator import ColorPaletteGenerator, HarmonyType

# Create generator with optional seed
generator = ColorPaletteGenerator(seed=42)

# Generate a specific palette
palette_data = generator.generate_palette(
    temperature="neutral",
    harmony_type=HarmonyType.COMPLEMENTARY,
    num_colors=5
)

# Create visualization
from colour import Color

colors = [Color.from_rgb(r/255, g/255, b/255) 
          for r, g, b in palette_data["rgb_values"]]
          
generator.visualize_palette(
    colors,
    title="Custom Palette",
    filename="custom_palette.png"
)
```

### Temperature Preferences

```python
# Warm palette
warm_palette = generator.generate_palette(temperature="warm")

# Cool palette
cool_palette = generator.generate_palette(temperature="cool")

# Specific number of colors
palette = generator.generate_palette(num_colors=3)
```

### Harmony Types

```python
# Triadic harmony
triadic = generator.generate_palette(
    harmony_type=HarmonyType.TRIADIC
)

# Analogous scheme
analogous = generator.generate_palette(
    harmony_type=HarmonyType.ANALOGOUS
)

# Monochromatic variations
mono = generator.generate_palette(
    harmony_type=HarmonyType.MONOCHROMATIC
)
```

---

## Harmony Types Explained

### Complementary
- Two colors opposite on color wheel
- High contrast and energy
- Best for: Emphasis, bold designs

### Analogous
- Three adjacent colors
- Natural, pleasing combinations
- Best for: Harmonious designs, nature themes

### Triadic
- Three evenly-spaced colors
- Balanced and vibrant
- Best for: Playful, energetic designs

### Tetradic (Double Complementary)
- Four colors in two complementary pairs
- Rich color schemes
- Best for: Complex designs, variety

### Split-Complementary
- Base color plus two adjacent to complement
- Softer than complementary
- Best for: Subtle contrast

### Monochromatic
- Single hue with variations in saturation/value
- Cohesive and elegant
- Best for: Minimalist, sophisticated designs

---

## Palette Analysis

Each palette includes detailed analysis:

```python
# Palette data structure
{
    "rgb_values": [(255, 100, 50), ...],
    "hex_values": ["#FF6432", ...],
    "hsv_values": [(15, 80, 100), ...],
    "cmyk_values": [(0, 60, 80, 0), ...],
    "harmony_type": "complementary",
    "temperature": "warm",
    "dominant_color": (255, 100, 50),
    "contrast_ratio": 4.5,
    "color_names": ["Coral", "Teal", ...]
}
```

---

## Visualization Options

### Standard Palette View
```python
generator.visualize_palette(
    colors,
    title="My Palette",
    show_hex=True,
    show_rgb=True,
    filename="palette.png"
)
```

### Advanced Visualization
```python
# Multiple views
generator.create_visualization_suite(
    colors,
    views=['swatches', 'wheel', 'gradient', 'comparison']
)
```

### Color Wheel Visualization
```python
# Show relationships on color wheel
generator.visualize_on_wheel(
    colors,
    show_harmony_lines=True,
    filename="color_wheel.png"
)
```

---

## Color Formats

### RGB (Red, Green, Blue)
- Web standard
- Range: 0-255 per channel
- Example: `(255, 100, 50)`

### HEX (Hexadecimal)
- Web/CSS format
- 6-digit hex code
- Example: `#FF6432`

### HSV (Hue, Saturation, Value)
- Intuitive color model
- Hue: 0-360°, Saturation/Value: 0-100%
- Example: `(15, 80, 100)`

### CMYK (Cyan, Magenta, Yellow, Black)
- Print standard
- Range: 0-100% per channel
- Example: `(0, 60, 80, 0)`

---

## Parameters

| Parameter | Type | Options | Default |
|-----------|------|---------|---------|
| `temperature` | str | 'warm', 'cool', 'neutral' | 'neutral' |
| `harmony_type` | HarmonyType | COMPLEMENTARY, ANALOGOUS, etc. | COMPLEMENTARY |
| `num_colors` | int | 2-12 | 5 |
| `saturation` | float | 0.0-1.0 | 0.7 |
| `value` | float | 0.0-1.0 | 0.9 |
| `seed` | int | Any integer | None |

---

## Advanced Features

### Custom Base Colors
```python
# Start from specific color
palette = generator.generate_from_base(
    base_color=(120, 200, 150),
    harmony_type=HarmonyType.ANALOGOUS
)
```

### Color Accessibility
```python
# Check WCAG contrast ratios
contrast = generator.check_accessibility(
    foreground=(0, 0, 0),
    background=(255, 255, 255)
)
# Returns: {'ratio': 21.0, 'aa': True, 'aaa': True}
```

### Batch Generation
```python
# Generate multiple palettes
palettes = generator.generate_batch(
    count=10,
    harmony_type=HarmonyType.TRIADIC,
    temperature="warm"
)
```

---

## Use Cases

### Web Design
- Website color schemes
- UI/UX design
- Brand identity
- Responsive design systems

### Graphic Design
- Print materials
- Branding packages
- Marketing collateral
- Social media graphics

### Art & Illustration
- Digital art palettes
- Traditional painting guides
- Color study references
- Mood boards

### Data Visualization
- Chart color schemes
- Accessible data colors
- Dashboard theming
- Infographic palettes

---

## Export Options

```python
# Save as image
generator.export_image(palette, "palette.png")

# Export color data
generator.export_json(palette, "palette.json")

# CSS variables
generator.export_css(palette, "colors.css")

# Adobe Swatch Exchange
generator.export_ase(palette, "palette.ase")
```

---

## Integration Examples

### CSS Variables
```css
/* Generated by color palette generator */
:root {
    --color-primary: #FF6432;
    --color-secondary: #32FF64;
    --color-accent: #6432FF;
}
```

### Python Dictionary
```python
colors = {
    'primary': '#FF6432',
    'secondary': '#32FF64',
    'accent': '#6432FF'
}
```

---

## Technical Stack

- **NumPy**: Color calculations
- **Matplotlib**: Visualization
- **colormath**: Color space conversions
- **Pillow**: Image generation
- **colorsys**: HSV transformations

---

## Color Theory Resources

The generator implements principles from:
- Johannes Itten's color theory
- Josef Albers' color interactions
- Modern digital color systems
- WCAG accessibility guidelines

---

## Future Enhancements

- Machine learning palette suggestions
- Image-based palette extraction
- Real-time web interface
- Figma/Sketch plugin integration
- AI-powered color naming
- Cultural color associations
- Seasonal palette themes

---

*Create beautiful, harmonious color schemes based on proven color theory*
