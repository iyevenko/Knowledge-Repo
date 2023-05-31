---
description: An introduction to Model Predictive Control (MPC) including the use of dynamic models, state estimation, and cost functions. The note also provides a list of introductory texts for readers new to MPC.
---
[3] ## Background
Readers with background in MPC and linear systems theory may skim this chapter briefly and proceed to Chapter 2. Other introductory texts covering the basics of MPC include:
- Maciejowski (2002)
- Camacho and Bordons (2004)
- Rossiter (2004)
- Goodwin, Sern, and De Don (2005)
- Kwon (2005)
- Wang (2009)

[4] ## Models and Modeling
MPC uses a dynamic model to forecast system behavior and optimize the forecast to produce the best decision - the control move at the current time. Models are central to every form of MPC. The state estimation problem is to evaluate the record of measurements to determine the most likely initial state of the system.

[5] ## Cost Function

- Formulating an MPC problem involves picking a series of n control inputs to stabilize a system to equilibrium.
- To use an optimizer-based approach for finding an optimal solution, we need a cost function to evaluate the current state.
- A quadratic cost function is a great choice for many practical problems as it is convex and can be optimized easily with the optimization tools we have at hand.
- The cost function can be represented as xT Qx + u Ru, where Q is a diagonal matrix  0, R is a scalar > 0, and +u  1 is the input constraint.
- The cost of the state of the system is represented by Qx, and the cost of the input is represented by Ru.
