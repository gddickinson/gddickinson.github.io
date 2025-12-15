# particle_trajectory_analyzer

A computationally efficient geometric method for classifying linear motion in single-particle tracking data without requiring tensor decomposition. The method employs two primary metrics: directionality ratio and normalized perpendicular distance, to classify trajectories as linear unidirectional, l

**[View on GitHub →](https://github.com/gddickinson/particle_trajectory_analyzer)**

---

## Overview

**Languages:** Python

## Documentation

# Geometric Method for Linear Motion Classification in Single-Particle Trajectories


A computationally efficient geometric method for classifying linear motion in single-particle tracking data without requiring tensor decomposition. The method employs two primary metrics: directionality ratio and normalized perpendicular distance, to classify trajectories as linear unidirectional, linear bidirectional, or non-linear. This approach provides comparable classification accuracy to eigenvalue-based methods while offering computational advantages for large-scale trajectory analysis.

## 1. Introduction

A critical challenge in SPT analysis is the automated classification of trajectory patterns, particularly distinguishing between linear (directed or confined linear) and non-linear (random or confined) motion modes

Traditional approaches rely on gyration tensor decomposition to extract eigenvalues and eigenvectors that characterize trajectory shape. While mathematically rigorous, these methods are computationally intensive for large datasets. Here, we introduce a simple geometric method that achieves robust linear motion classification using direct geometric measurements.

## 2. Mathematical Framework

### 2.1 Trajectory Representation

Consider a trajectory consisting of *N* positions recorded at discrete time points:

**X** = {**x**<sub>i</sub> = (*x*<sub>i</sub>, *y*<sub>i</sub>) | *i* = 1, 2, ..., *N*}

where **x**<sub>i</sub> represents the particle position at frame *i*.

### 2.2 Radius of Gyration (Simple Method)

The radius of gyration *R*<sub>g</sub> quantifies the spatial extent of a trajectory:

*R*<sub>g</sub> = √[⟨**x**<sup>2</sup>⟩ - ⟨**x**⟩<sup>2</sup>]

where:
- ⟨**x**⟩ = (1/*N*) Σ<sub>i=1</sub><sup>N</sup> **x**<sub>i</sub> is the mean position
- ⟨**x**<sup>2</sup>⟩ = (1/*N*) Σ<sub>i=1</sub><sup>N</sup> **x**<sub>i</sub><sup>2</sup> is the mean squared position

### 2.3 Scaled Radius of Gyration

Following Golan and Sherman<sup>8</sup>, we normalize *R*<

*[View full README on GitHub]*

