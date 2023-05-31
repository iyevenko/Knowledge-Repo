---
description: An overview of the Model Predictive Control (MPC) design using MATLAB & Simulink, covering topics such as controller design, plant model definition, closed-loop response simulation, and softening constraints.
---
# Get Started with Model Predictive Control Toolbox

## Category: Getting Started with Model Predictive Control Toolbox

### MPC Design
- Design MPC Controller at the Command Line
- Model Predictive Control of a Single-Input-Single-Output Plant
- Model Predictive Control of a Multi-Input Single-Output Plant
- Model Predictive Control of a Multi-Input Multi-Output Plant
- Gain-Scheduled MPC Design

### Nonlinear MPC Design
- Design and simulate a model predictive controller at the MATLAB command line
- Create and simulate model predictive controller for a SISO plant
- Create and simulate model predictive controller for a plant with multiple inputs and a single output
- Create and simulate a model predictive controller for a MIMO plant

### Explicit MPC Design
- Automated Driving Applications

## Code Generation

## Type
- All

## MATLAB
- Simulink

## How useful was this information?
- 3 (out of 5)

# Model Predictive Control of Multi-Input Single-Output Plant

## Introduction
This document provides an overview of the Model Predictive Control (MPC) of Multi-Input Single-Output Plant using MATLAB & Simulink. It covers the following topics:

## Built-in "active-set" QP solver with MaxIterations of 120
The MPC controller uses a built-in "active-set" QP solver with MaxIterations of 120.

## Plant Model Definition
The plant model is defined as a Multi-Input Single-Output Plant.

## Steady-State Offset Examination
To examine whether the MPC controller can reject constant output disturbances and track a constant setpoint with zero offsets in steady state, calculate the closed-loop DC gain from output disturbances to controlled outputs using the cloffset command. This gain is also known as the steady state output sensitivity of the closed loop.

## MPC Controller Design
The MPC controller is designed to reject constant output disturbances and track a constant setpoint with zero offsets in steady state.

## Closed-Loop Response Simulation Using sim
The sim command provides a quick way to simulate an MPC controller in a closed loop with a linear time-invariant plant when constraints and weights stay constant and you can easily and completely specify the disturbance and reference signals ahead of time.

## Linear Representation of MPC Controller
The linear representation of the MPC controller is used to simulate the closed-loop response to reference and measured input disturbance signals.

## Simulation Using Simulink
Simulink is used to simulate the closed-loop response to reference and measured input disturbance signals.

## Softening Constraints
Constraints are softened to improve the performance of the MPC controller.

## Model Mismatch
Model mismatch is taken into account when designing the MPC controller.

## Changing Built-In State Estimator Kalman Gains
The built-in state estimator Kalman gains can be changed to improve the performance of the MPC controller.