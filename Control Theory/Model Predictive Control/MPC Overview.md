---
description: This note provides an overview of Model Predictive Control (MPC), including its basics, advantages over other control schemes, variants, and applications. It also includes references to introductory texts for readers with no background in MPC and linear systems theory.
---
# Introduction to Model Predictive Control

## Background
Readers with background in MPC and linear systems theory may skim this chapter briefly and proceed to Chapter 2. Other introductory texts covering the basics of MPC include:
- Maciejowski (2002)
- Camacho and Bordons (2004)
- Rossiter (2004)
- Goodwin, Sern, and De Don (2005)
- Kwon (2005)
- Wang (2009)

## Models and Modeling
MPC uses a dynamic model to forecast system behavior and optimize the forecast to produce the best decision - the control move at the current time. Models are central to every form of MPC. The state estimation problem is to evaluate the record of measurements to determine the most likely initial state of the system.

## Applications
MPC has been used in various applications, including:
- Chemical processes
- Power systems
- Robotics
- Autonomous vehicles
- Aerospace systems

## Comparisons to Other Control Schemes
MPC has several advantages over other control schemes, such as PID control and LQR. It can handle constraints and nonlinearities, and it can optimize control inputs over a finite time horizon. However, it can be computationally expensive and requires a good model of the system. MPC has been compared to other control schemes, such as adaptive control and fuzzy control.

## Variants of MPC
There are several variants of MPC, including:
- Nonlinear MPC
- Distributed MPC
- Stochastic MPC
- Robust MPC
- Economic MPC

## Overview
Model Predictive Control (MPC) is a control scheme that uses a model of the system being controlled to predict future behavior and optimize control inputs accordingly. 

## Basics of MPC
MPC involves solving a quadratic program at each time step to determine the optimal control inputs based on the current state of the system. The length of the finite time horizon and the upper bound of the MPC procedure's runtime depend on the problem at hand.

## Matrix Construction
Quadratic program solvers take a cost function in the form of a single matrix H, which is internally used to evaluate X'HX with (optional) constraints on the states. There are two main ways to construct this matrix: QP by substitution and QP without substitution.

## Closed Form Solutions
There are even ways to find closed form solutions to the MPC problem, which can save computational resources. This method involves computing the closed form solution offline and then evaluating the solution using these equations on the target hardware which may not be powerful enough to run the optimization procedure in real time.

For more information on MPC, including its many variants and applications, as well as comparisons to other control schemes, refer to the folder "/Control Theory/Model Predictive Control - An overview of Model Predictive Control and the many variants of it as well as applications, and comparisons to other control schemes.