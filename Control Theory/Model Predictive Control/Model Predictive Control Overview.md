---
description: An overview of the essential elements of MPC, including models and modeling, stability assumptions, terminal constraints, and comparisons to other control schemes. It also includes examples of MPC, scholarly articles, basics of MPC, closed form solutions, hyperparameters, and references.
---
# Model Predictive Control (MPC) Review

## Introduction
Model Predictive Control (MPC) is an advanced control method that uses a process model to predict the future and make control decisions accordingly. This chapter provides an overview of the essential elements of MPC, including models and modeling, stability assumptions, terminal constraints, and comparisons to other control schemes.

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
MPC is a control scheme that uses a model of the system to predict future behavior and optimize control inputs over a finite time horizon. The optimization problem is solved at each time step, and the first control input is applied to the system. MPC has become increasingly popular in recent years due to its ability to handle constraints and nonlinearities.

## Examples of MPC
There are many different forms of MPC that can be used for various applications. The most useful forms of MPC are presented here, which also display the roles of the three main assumptions used to guarantee closed-loop asymptotic stability. These assumptions are summarized in Table 2.1 for the time-invariant case, and Table 2.2 for the time-varying case.

### Stability Assumptions
- Continuity of system and cost
- Properties of constraint sets
- Basic stability assumption
- Uniform weak controllability

## Terminal Constraint
One question that is often asked is whether or not the terminal constraint is necessary. Since the conditions given previously are sufficient, necessity cannot be claimed. Further discussion on this topic is provided later in the book.

## Scholarly Articles
- "Model Predictive Control: Review of the Three Decades" by Mayne et al. (Cited by 678)
- "Model Predictive Control: Recent Developments and Tutorial Overview" by Rawlings et al. (Cited by 1378)
- "Review on Model Predictive Control: An Engineering Perspective" by Schwenzer (Cited by 126)
- "Model Predictive Control Tuning Methods: A Review" by Garriga (Cited by 418)
- "Review Model Predictive Controller for Stability and Plant Model" by MathWorks

## Basics of MPC
The basics of MPC involve creating a mathematical model of the system, defining a cost function, and optimizing control inputs over a time horizon. The cost function can be adjusted to prioritize different objectives, such as minimizing error or energy consumption. MPC requires solving an optimization problem at each time step, which can be computationally intensive.

## Closed Form Solutions
There are even ways to find closed form solutions to the MPC problem, which can save computational resources. This method involves computing the closed form solution offline and then evaluating the solution using equations on the target hardware.

## Hyperparameters
MPC has several hyperparameters that can be adjusted, such as the cost matrices and length of time horizon. Finding a good set of parameters requires trial and error based on how the system behaves on running on the controller.

## References
- https://www.itk.ntnu.no/fag/fordypning/TK16-filer/Samling1_MorariLee.pdf
- https://engineering.utsa.edu/ataha/wp-content/uploads/sites/38/2017/10/MPC_Intro.pdf
- https://www.uiam.sk/pc11/data/workshops/mpc/MPC_PC11_Lecture1.pdf
- http://underactuated.mit.edu/lqr.html
- https://www.ni.com/en-in/innovations/white-papers/06/pid-theory-explained.html
- http://cse.lab.imtlucca.it/~bemporad/teaching/mpc/stuttgart_2012/5-hybrid_mpc.pdf