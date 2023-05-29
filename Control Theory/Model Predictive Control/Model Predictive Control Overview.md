---
description: An introduction to the essential elements of model predictive control (MPC), including models and modeling, stability assumptions, terminal constraints, and a comparison to other control schemes.
---
# Model Predictive Control (MPC)

## Introduction
This chapter provides an overview of the essential elements of model predictive control (MPC). It covers deterministic and stochastic models, regulation, state estimation, dynamic programming (DP), tracking, disturbances, and important performance properties such as closed-loop stability and zero offset to disturbances.

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

## Applications and Comparisons
MPC has its roots in optimal control and is used in a variety of applications. It is often compared to other control schemes to determine its effectiveness in different scenarios.

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

## Comparison to Other Control Schemes
MPC has several advantages over other control schemes, such as PID control and LQR. It can handle constraints and nonlinearities, and it can optimize control inputs over a finite time horizon. However, it can be computationally expensive and requires a good model of the system.