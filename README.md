# WH5470

Final Project for ASTR 5470: Wisdom-Holman N-body Symplectic Integrator

This project simulates the gravitational interactions between multiple bodies in space using the Wisdom-Holman symplectic integrator, an efficient method for long-term numerical simulations of planetary systems. It's designed to conserve the system's Hamiltonian over time, making it practical for studying orbital dynamics.

---

## Features

- **Symplectic Integration**: Uses the Wisdom-Holman method to ensure better long-term energy conservation.
- **3D Visualization**: Includes functionality to visualize the trajectories of celestial bodies in three dimensions.
- **Energy and Angular Momentum Conservation Check**: Computes and plots total energy and angular momentum to verify their conservation over the simulation period.
- **Close Encounter Detection**: Integrations are paused when a hill radius close encounter happens.
- **General Relativity Modification**: Adds optional gr module to modify general relativity effects.
- **Long Term Evolution Stability Check**: Wisdom-Holman integrators are best used for long-term evolution and stability check.

  
## Getting Started

### Prerequisites

- Python 3.x
- NumPy
- Matplotlib
- mpl_toolkits for 3D plotting
- rebound (optional, only required for Test 3)

### Installation

Clone this repository to your local machine using:

```bash
git clone https://github.com/ASTRX470/final-project-minliqiu.git
```

### Usage
**How to Use the integrator**

Here is a simple guide on how to use the integrator:

1. **Initialization**: First, you need to create an instance of the NBody class by providing the masses, initial positions, and velocities of the bodies or orbital elements.

2. **Run Simulation**: Call the `integrate()` method to perform the simulation.

3. **Plot Trajectory**: After the simulation, you can get outputs from the simulation and plot the trajectory in both Cartesian and Jacobi coordinates.

**Example Code**:
```python
from wh5470 import wh5470

masses = [1e10, 1e10]  # Masses of two bodies in kilograms
positions = [[0, 0], [100, 0]]  # Initial positions in meters
velocities = [[0, 10], [0, -10]]  # Initial velocities in meters per second

sim = wh5470(masses, positions, velocities)
sim.integrate()
```

### Inputs
**Inputs to the integrator**

- `masses`: A list of masses of the bodies (in kilograms).
- `orbital_elements`: A list of lists containing the orbital elements of each body (in meters).
- `positions`: A list of lists containing the x and y coordinates of each body (in meters).
- `velocities`: A list of lists representing the velocity in the x and y directions for each body (in meters per second).
- `time_step`: The time step for each iteration of the simulation (in seconds).
- `total_time`: The total time to run the simulation (in seconds).

### Outputs
**Outputs from the integrator**

- `trajectory`: A list of trajectories (positions) in Cartesian coordinates of the bodies over time.
- `velocity`: A list of velocities in Cartesian coordinates of the bodies over time.
- `energy`: A list of total energy of the system over time.
- `angular_momentum`: A list of total angular momentum
- `trajectory_jacobi`: A list of trajectories (positions) in Jacobi coordinates of the bodies over time.
- `velocity_jacobi`: A list of velocities in Jacobi coordinates of the bodies over time.
- `orbital_elements`: A list of orbital elements of the bodies over time.

## Configuration

To change the simulation parameters (e.g., number of bodies, time step), modify the parameters directly in `wh5470.py`.

## Authors

- **Minli Qiu** - *Initial work* - [minliqiu](https://github.com/minliqiu/wh5470)

---
