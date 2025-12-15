# comlex-function-visualization

A Python tool for creating beautiful visualizations and animations of complex function transformations. This program provides insights into how complex functions transform the complex plane through domain coloring and animated transitions.

**[View on GitHub →](https://github.com/gddickinson/complex-function-visualization)**

---

## Overview

**Languages:** Python

## Documentation

# Complex Function Visualizer

A Python tool for creating beautiful visualizations and animations of complex function transformations. This program provides insights into how complex functions transform the complex plane through domain coloring and animated transitions.

## Features

- Domain coloring visualizations of complex functions
- Phase and magnitude visualizations in separate plots
- Animated transformations showing how functions map the complex plane
- Custom HSV-based colormap for intuitive phase visualization
- Support for a wide range of complex functions
- Generates both static images (PNG) and animations (GIF)

## Installation

1. Clone this repository:
```bash
git clone [repository-url]
cd complex-function-visualizer
```

2. Install the required dependencies:
```bash
pip install numpy matplotlib
```

## Usage

Run the main script:
```bash
python complex_visualizer.py
```

The program will generate:
- Static visualizations for all example functions (saved as PNG files)
- Animations for selected transformations (saved as GIF files)
- Real-time display of all visualizations

## Included Functions

The visualizer comes with several pre-defined complex functions:
- `f(z) = z²` (Basic quadratic function)
- `f(z) = z³ - 1` (Cubic function with roots of unity)
- `f(z) = exp(z)` (Complex exponential)
- `f(z) = sin(z)` (Complex sine)
- `f(z) = z/(1-z)` (Rational function)
- `f(z) = sqrt(z)` (Complex square root)
- `f(z) = z·exp(z)` (Product function)
- `f(z) = ln(1+z)` (Complex logarithm)

## Customization

You can easily add new functions or modify existing ones:

```python
def create_example_functions():
    return [
        (lambda z: your_function(z), "f(z) = your_function_description"),
        # Add more functions here
    ]
```

### Parameters to Adjust

- `size`: Resolution of the visualization (default: 500)
- `x_range` and `y_range`: Range of the complex plane to visualize
- `frames`: Number of frames in animations (default: 50)

## Output Files

The

*[View full README on GitHub]*

