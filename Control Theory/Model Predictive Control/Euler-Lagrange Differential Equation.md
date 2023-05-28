---
description: The fundamental equation of calculus of variations used in Model Predictive Control.
---
# Control Theory

## Model Predictive Control
Model Predictive Control (MPC) is a control strategy that uses a mathematical model of the system to predict its future behavior and optimize a control sequence that minimizes a given cost function. MPC is widely used in various applications, including robotics, process control, and autonomous vehicles.

Some of the variants of MPC include:
- Linear MPC
- Nonlinear MPC
- Stochastic MPC
- Distributed MPC
- Model Reference Adaptive Control (MRAC)

MPC can be compared to other control schemes such as PID control, LQR control, and adaptive control. Each has its own advantages and disadvantages depending on the specific application.

## Euler-Lagrange Differential Equation
The Euler-Lagrange differential equation is the fundamental equation of calculus of variations used in Model Predictive Control. It states that if J is defined by an integral of the form J=f(x,y,y')dx, then J has a stationary value if the Euler-Lagrange differential equation of d(f/y')/dx - (f/y) = 0 is satisfied.

In MPC, the Euler-Lagrange differential equation is used to derive the optimal control sequence that minimizes a given cost function. The cost function is typically defined as a sum of the predicted future states and inputs over a finite time horizon. By solving the Euler-Lagrange differential equation, the optimal control sequence can be obtained and applied to the system.

The Wolfram Language package VariationalMethods^ provides an implementation of the Euler-Lagrange differential equation as EulerEquations[f, u[x], x]. Problems in the calculus of variations can often be solved by solution of the appropriate Euler-Lagrange equation.