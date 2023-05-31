---
description: A software framework and library developed by DeepMind for real-time predictive control with MuJoCo, allowing users to easily author and solve complex robotics tasks. The framework includes a graphical user interface and supports three shooting-based planners, while the library includes three planners that use different techniques to perform numerical optimization for improved policies.
---
# MuJoCo MPC and mujoco_mpc Library

MuJoCo MPC (MJPC) and mujoco_mpc library are software frameworks developed by DeepMind for real-time predictive control with MuJoCo. They allow users to easily author and solve complex robotics tasks.

## MuJoCo MPC

### Overview

MJPC is an interactive application and software framework for real-time predictive control with MuJoCo. It uses predictive control to solve complex robotics tasks and currently supports three shooting-based planners: derivative-based iLQG and Gradient Descent, and a simple yet very competitive derivative-free method called Predictive Sampling.

### Graphical User Interface

MJPC has a graphical user interface that allows users to easily author and solve complex robotics tasks.

### Installation

MJPC can be installed on macOS and Ubuntu. For installation instructions, please refer to their README.md file on their GitHub page.

### Contributing

If you would like to contribute to MJPC, please refer to their GitHub page for more information.

### Known Issues

Please refer to their GitHub page for a list of known issues.

### Citation

If you use MJPC in your research, please cite their preprint available on their website.

### Acknowledgments

MJPC was developed by DeepMind.

### License and Disclaimer

MJPC is licensed under the Apache-2.0 license. Please refer to their GitHub page for more information.

## mujoco_mpc Library

### Overview

The mujoco_mpc library is a collection of planners that use numerical optimization to find improved policies. The library includes three planners that use different techniques to perform this search: Predictive Sampling, Gradient Descent, and Iterative Linear Quadratic Gaussian (iLQG).

### Planners

1. Predictive Sampling
   - Random search
   - Derivative-free
   - Spline representation for controls
2. Gradient Descent
   - Requires gradients
   - Spline representation for controls
3. Iterative Linear Quadratic Gaussian (iLQG)
   - Requires gradients and Hessians
   - Direct representation for controls

### State

Rollouts are performed after setting both the simulation and initialization states.

#### Simulation State

This includes:
- Configuration: data->qpos
- Velocity: data->qvel
- Acceleration: data->qacc

#### Initialization State

This includes:
- Mocap: data->mocap
- Userdata: data->userdata
- Time: data->time

### Applications

This library can be used for applications in control theory, specifically in Model Predictive Control. It offers a variety of options for planners and state representation, making it a versatile tool for control engineers. Comparisons to other control schemes can also be made using this library.