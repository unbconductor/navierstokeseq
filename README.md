# Phyllo-CFD: Hybrid Quantum-Classical Fluid Dynamics Solver

Phyllo-CFD is a specialized Computational Fluid Dynamics (CFD) solver that bridges quantum-inspired neural architecture with classical fluid mechanics. By utilizing the "Phyllo" N-Gate potential as a momentum forcing term, this engine simulates the complex, non-linear interaction of fluid topologies such as synthetic vortex dipoles, fractal cascades, and real-world chaotic data assimilation.

## Core Architecture

Standard explicit fluid solvers often suffer from numerical instability when introduced to high-gradient topological forcing. Phyllo-CFD overcomes this by employing an **Implicit (Backward Euler) integration scheme** coupled with a rigorous **Pressure Projection** method. 

### Mathematical Framework
The engine solves the incompressible Navier-Stokes equations in their velocity-pressure formulation:

$$\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{u} = -\frac{1}{\rho}\nabla p + \nu \nabla^2 \mathbf{u} + \mathbf{f}$$

To ensure mass conservation ($\nabla \cdot \mathbf{u} = 0$), we enforce incompressibility by solving the Poisson equation for pressure:

$$\nabla^2 p = \frac{\rho}{\Delta t} (\nabla \cdot \mathbf{u}^*)$$

## The Three Modules

This repository contains three independent scripts demonstrating the capabilities of the Phyllo-CFD engine. You can run any of them directly from your terminal.

### 1. Vortex Dipole Interaction (`phyllo_dipole.py`)
This module maps a synthetic Vortex Dipole interaction. Two quantum-stable potential centers of opposite phase are injected into the grid, creating a classic "S-pattern" shear layer.
* **To run:** `python3 phyllo_dipole.py`

### 2. Real-World Data Assimilation (`phyllo_assimilation.py`)
This module acts as a digital twin. It generates 50 randomized, chaotic telemetry sensors and uses SciPy's Delaunay triangulation to interpolate the sparse data across the continuous fluid space, simulating intense turbulence.
* **To run:** `python3 phyllo_assimilation.py`

### 3. Fractal Vortex Cascade (`phyllo_fractal.py`)
This script forces the fluid into a Sierpinski Gasket topological lattice. The fluid resolves the energy into a stationary vortex cascade that mirrors the fractal geometry.
* **To run:** `python3 phyllo_fractal.py`

## Dependencies
Ensure you have the required scientific libraries installed before running the solvers:
`pip install numpy matplotlib scipy`
