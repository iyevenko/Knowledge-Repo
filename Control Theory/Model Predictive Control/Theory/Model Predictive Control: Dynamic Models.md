---
description: This note discusses the dynamic models used in Model Predictive Control (MPC) and the state estimation problem, as well as provides an overview of MPC and its implementation for target tracking problems using the Casadi framework and MATLAB simulation environment.
---
# Model Predictive Control: Dynamic Models and State Estimation

## Introduction
Model Predictive Control (MPC) involves dynamic models and optimization to produce an optimal state estimate. In this text, we discuss the dynamic models used in MPC and the state estimation problem.

## Dynamic Models
### Differential Equation Models
The familiar differential equation models used in MPC are:

dx/dt = f(x, u, t)

y = h(x, u, t)

x(to) = x0

where x is the state, u is the input, y is the output, and t is time. The initial condition specifies the value of the state x at time = to, and the solution to the differential equation is sought for time greater than to.

### Linear Dynamic Models
Linear state space models are commonly used in MPC. The most general linear state space model is the time-varying model:

dx/dt = A(t)x + B(t)u

y = C(t)x + D(t)u

x(0) = x0

where A(t) is the state transition matrix, B(t) is the input matrix, C(t) is the output matrix, and D(t) allows a direct coupling between u and y. In many applications, D = 0.

If A, B, C, and D are time-invariant, the linear model reduces to:

dx/dt = Ax + Bu

y = Cx + Du

x(0) = x0

## State Estimation
### Joint Density
The joint density of (x(0), v(0)) is expressed using the independent joint normal result (1.20).

### Linear Transformation
The pair (x(0), y(0)) is a linear transformation of the pair (x(0), v(0)). Using the linear transformation of normal result (1.21), and the density of (x(0), v(0)) gives the density of (x(0), y(0)).

### Conditional Density
The conditional density of x(0) given y(0) is normal. The optimal state estimate is the value of x(0) that maximizes this conditional density. For a normal, that is the mean, and we choose x(0) = m. We also denote the variance in this conditional after measurement y(0) by P(0) = P with P given in the previous equation.

### Information Increase
The change in variance after measurement (Q(0) to P(0)) quantifies the information increase by obtaining measurement y(0). The variance after measurement, P(0), is always less than or equal to Q(0), which implies that we have gained information by obtaining the measurement.

## Model Predictive Control - An Overview
### What is Model Predictive Control?
- Model Predictive Control (MPC) uses the system model to predict future states of the system.
- It applies optimal inputs in a prediction horizon and compensates for unmeasured noise or disturbance in the system.
- MPC is a control scheme used in various applications, including robotics, mobile robots, and aerial robotics.

### Target Tracking Problem
- The current repository implements MPC for target tracking problems.
- The system is an unmanned aerial vehicle (UAV) following a mobile vehicle target.
- The cost function to be minimized for predicted inputs is the distance between the UAV and the moving target.

### Repository Information
- Repository Name: devsonni/MPC-Implementation
- Description: This repository has the code for the nonlinear model predictive controller for target tracking problems with the use of Casadi framework and Matlab simulation environment.
- Languages Used: Python (56.8%), MATLAB (43.2%)

### Repository Contents
- "State predictive model of target" folder contains the target's model, which serves as a moving reference for the UAV and provides the cost value from the initial point of the UAV.
- "NMPC_TT" contains the code for the nonlinear model predictive controller.

## Conclusion
Understanding the dynamic models used in MPC and the state estimation problem is crucial for designing and implementing effective control schemes. Linear state space models are commonly used in MPC, and can be either time-varying or time-invariant. The optimal state estimate is obtained by maximizing the conditional density of x(0) given y(0), which is normal.

MPC is a powerful control scheme used in various applications, including target tracking problems. The current repository provides an implementation of MPC for target tracking problems using the Casadi framework and MATLAB simulation environment.