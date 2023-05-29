---
description: This note provides an overview of constraints and models in Model Predictive Control (MPC) and compares the DP solution for the optimal control problem to MPC.
---
# Model Predictive Control - Constraints and Models

## Overview
This markdown note covers information from the "MPC-book-2nd-edition-1st-printing.pdf" preview window. Specifically, it covers constraints and models in Model Predictive Control (MPC).

## Constraints
MPC includes constraints on manipulated inputs, which are typically bounded. These constraints are represented by linear inequalities. Constraints can also be imposed on states or outputs for safety, operability, and product quality reasons. 

## Models
MPC uses a state space model, which includes an augmented system model to maintain the state space form of the model. The manipulated inputs are represented by valve positions, voltages, torques, etc. 

## Augmented System Model
To limit the rate of change of the input, u(k) - u(k - 1), the state is augmented as w(k). The augmented system model becomes x+(k) = AX(k) + Bu(k) and y(k) = CX(k).

## Conclusion
This information provides an overview of constraints and models in MPC. For more information on MPC and its many variants, applications, and comparisons to other control schemes, refer to the "Control Theory" folder.

# Dynamic Programming Solution for Optimal Control Problem

## Overview
This markdown note covers information from the "MPC-book-2nd-edition-1st-printing.pdf" preview window. Specifically, it covers the DP solution for the optimal control problem and compares it to MPC.

## Optimal Control Problem
The optimal control problem PN(x) is defined by (2.7) with the cost function V ( ) defined by (2.3) and the constraints by (2.4).

## DP Solution
DP yields an optimal policy HO = (Ag(), ur , . .., A-1(-)), i.e., a sequence of control laws Mi: X; - U, i = 0,1,..., N - 1. The domain X; of each control law will be defined later. The optimal controlled system is time varying and satisfies x+ = f(x, u? (x)), i = 0,1,..., N - 1.

## Comparison with MPC
The system using MPC is time invariant and satisfies x* = f(X, KN(x)), i = 0,1,..., N -1 with KN () = u%(-). The optimal control law at time i is u (-), but receding horizon control (RHC) uses the time-invariant control law KN ( ) Mo() obtained by assuming that at each time t, the terminal time or horizon is t + N so that the horizon t + N recedes as t increases. One consequence is that the time-invariant control law KN(- ) is not optimal.