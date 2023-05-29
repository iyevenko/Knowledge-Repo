---
description: An introduction to optimal control and multistage optimization, as well as the application of dynamic programming to solve the LQ control problem.
---
# Introduction to Optimal Control and Multistage Optimization

## Overview
The current document is titled "MPC-book-2nd-edition-1st-printing.pdf" and is on page 60 of 819. It provides an introduction to optimal control and multistage optimization.

## Optimal LQ Control Problem
The document formulates an optimal LQ control problem as follows:
```
min V(x(0), u)
```
The Q, Pf, and R matrices are often chosen to be diagonal, but the document does not assume that here. However, it assumes that Q, Pf, and R are real and symmetric; Q and Pr are positive semidefinite; and R is positive definite. These assumptions guarantee that the solution to the optimal control problem exists and is unique.

## Multistage Optimization
The document also provides a brief introduction to methods for solving multistage optimization problems. It considers the set of variables w, x, y, and z, and an objective function with special structure in which each stage's cost function in the sum depends only on adjacent variable pairs. The document presents a method for solving the problem by optimizing a sequence of three single-variable problems.

## Folder Location
This markdown note can be found in the following folder on the computer:
```
/Control Theory/Model Predictive Control - An overview of Model Predictive Control and the many variants of it as well as applications, and comparisons to other control schemes.
```

# Introduction to Dynamic Programming Solution for LQ Control Problem

## Overview
This section discusses the application of Dynamic Programming (DP) to solve the LQ control problem. The problem is first rewritten to optimize over input u (N - 1) and state * (N) using backward DP.

## Problem Formulation
The overall objective function is rearranged as follows:
```
min f(x(0), u(0)) + l(x(1), u(1)) + . .  +
u(0),x (1),...u (N-2),x (N-1)
```
where the stage cost "(x, u) = (1/2) (x'Qx + u' Ru), k = 0,..., N- 1 and the terminal stage cost N(x) = (1/2)x'Pex. The problem to be solved at the last stage is:
```
min "((N - 1), u(N - 1)) + IN (x (N))
```
subject to `x (N) = Ax (N - 1) + Bu(N -1)`.

## Conclusion
DP is a convenient method to solve the LQ control problem.