# interference_simulation

This project is an interactive simulation of wave phenomena, focusing on interference patterns in a 2D environment. It provides a visual representation of various wave behaviors, including reflection, absorption, diffraction, and interference. The simulation is built using Python and PyQt5 for the g

**[View on GitHub →](https://github.com/gddickinson/interference_simulation)**

---

## Overview

**Languages:** Python

## Documentation

# Wave Interference Simulation

## Overview

This project is an interactive simulation of wave phenomena, focusing on interference patterns in a 2D environment. It provides a visual representation of various wave behaviors, including reflection, absorption, diffraction, and interference. The simulation is built using Python and PyQt5 for the graphical user interface, with matplotlib for rendering the wave field.

## Features

- Real-time simulation of wave propagation and interference
- Multiple wave sources (slits) with adjustable properties
- Various boundary conditions: reflective, absorbing, and open
- Addition of obstacles to observe diffraction and reflection
- Generation of wave packets and interference points
- Standing wave mode visualization
- Adjustable global parameters: time scale, depth, and decay factor

## Installation

1. Clone this repository:
git clone https://github.com/yourusername/wave-interference-simulation.git

2. Install the required dependencies:
pip install numpy matplotlib PyQt5

3. Run the simulation:
python main.py

## Usage Instructions

1. **Starting the Simulation**: Upon launching, you'll be prompted to enter the number of slits for each side of the tank. After setup, click the "Start" button to begin the simulation.

2. **Adjusting Global Parameters**:
- Use the "Time Scale" slider to speed up or slow down the simulation.
- The "Depth" slider adjusts the simulated water depth, affecting wave speed.
- "Wave Decay" controls how quickly waves dissipate over distance.

3. **Boundary Conditions**: Select between "Reflective", "Absorbing", or "Open" boundaries using the dropdown menu.

4. **Slit Controls**: Each slit has individual controls for amplitude, wavelength, frequency, and width.

5. **Adding Elements**:
- Click "Add Obstacle" to place a random circular obstacle in the tank.
- "Add Wave Packet" creates a localized wave disturbance.
- "Add Interference Point" places a point source of waves.

6. **Standing Waves**: Select a stand

*[View full README on GitHub]*

