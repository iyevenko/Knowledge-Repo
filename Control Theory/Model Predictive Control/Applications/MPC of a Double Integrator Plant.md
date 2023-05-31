---
description: An overview of Model Predictive Control (MPC) of Single-Input-Single-Output and Multi-Input Single-Output Plants using MATLAB & Simulink, covering the definition of plant models, design of MPC controllers, and simulation of closed-loop systems.
---
[1] # Model Predictive Control of Single-Input-Single-Output and Multi-Input Single-Output Plants - MATLAB & Simulink

[2] ## Introduction
This example provides an overview of Model Predictive Control (MPC) of Single-Input-Single-Output and Multi-Input Single-Output Plants using MATLAB & Simulink. It covers the following topics:
- Define the plant model
- Design the MPC controller
- Simulate the system using Simulink

[3] ## Model Predictive Control of Single-Input-Single-Output Plant

[4] ### Define the Plant Model
The plant model used in this example is a double integrator, where the input is the manipulated variable and the output is the measured output. The plant model is defined as follows:
```
plant = tf(1, [1 0 1]);
```

[5] ### Design the MPC Controller
The MPC controller is designed using the following parameters:
- Sampling period: 0.1 seconds
- Prediction horizon: 10 steps
- Control horizon: 3 moves

The controller object is created using the following code:
```
mpcobj = mpc(plant, 0.1, 10, 3);
```
At this point, the MPC problem is still unconstrained as no weights have been specified for the quadratic cost function to be minimized by the controller. The default weights are assumed (0 for the manipulated variables, 0.1 for the manipulated variable rates, and 1 for the output variables). The actuator saturation limits are specified as constraints on the manipulated variable using the following code:
```
mpcobj.MV = struct('Min', -1, 'Max', 1);
```

[6] ### Simulate the System Using Simulink
Simulink is used to simulate the closed-loop system. The plant model is implemented with two integrator blocks in series, and the MPC controller block is configured to use the workspace `mpcobj` object as the controller. The manipulated variables and the output and reference signals are also included in the simulation. The output signal is saved by the To-Workspace block.
