# calcium_simulator

The Calcium Simulator is a sophisticated tool designed to model and visualize intracellular calcium dynamics in a 2D representation of a cell. This simulator focuses on the interplay between the cytosol, endoplasmic reticulum (ER), and mitochondria, providing a detailed look at calcium signaling pro

**[View on GitHub →](https://github.com/gddickinson/calcium_simulator)**

---

## Overview

**Languages:** Python

## Documentation

# Calcium Simulator

## Introduction

The Calcium Simulator is a sophisticated tool designed to model and visualize intracellular calcium dynamics in a 2D representation of a cell. This simulator focuses on the interplay between the cytosol, endoplasmic reticulum (ER), and mitochondria, providing a detailed look at calcium signaling processes.

Key features include:
- Simulation of calcium dynamics in cytosol, ER, and mitochondria
- Modeling of IP3 receptor (IP3R) channel behavior
- Visualization of calcium concentrations and cellular structures
- Customizable parameters for tailoring simulations
- Ability to save and load different cell states

This simulator is particularly useful for researchers, students, and educators in the fields of cell biology, biophysics, and computational biology.

## Mathematical Model

The simulator is based on a reaction-diffusion model that describes the spatiotemporal evolution of calcium concentrations. The core equations are:

1. Cytosolic calcium:
d[Ca2+]_cyt/dt = D_Ca ∇²[Ca2+]_cyt + J_IP3R + J_leak - J_SERCA - J_PMCA - J_MCU - J_buffer
2. ER calcium:
d[Ca2+]_ER/dt = -J_IP3R - J_leak + J_SERCA
3. Mitochondrial calcium:
d[Ca2+]_mito/dt = J_MCU
4. IP3 concentration:
d[IP3]/dt = D_IP3 ∇²[IP3] - J_degradation

Where:
- D_Ca and D_IP3 are diffusion coefficients
- J_IP3R is the flux through IP3 receptors
- J_leak is the leak from ER to cytosol
- J_SERCA is the flux through SERCA pumps
- J_PMCA is the flux through plasma membrane Ca2+ ATPase
- J_MCU is the flux through mitochondrial Ca2+ uniporter
- J_buffer represents Ca2+ buffering

The IP3R flux is modeled stochastically, with opening and closing probabilities dependent on cytosolic calcium and IP3 concentrations.

## Installation

1. Clone this repository:
git clone https://github.com/yourusername/calcium-simulator.git

2. Navigate to the project directory:
cd calcium-simulator

3. Create a virtual environment (optional but recommended):
python -m venv venv
source venv/bin/activate  

*[View full README on GitHub]*

