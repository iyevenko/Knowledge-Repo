---
description: This note provides an introduction to Model Predictive Control (MPC), discussing its basics, variants, applications, and comparisons to other control schemes. It also explores the intersection of MPC and Reinforcement Learning (RL) and provides an example of NMPC-based UAV 3D target tracking in the presence of obstacles and visibility constraints.
---
# Model Predictive Control (MPC) - An Overview

## Introduction
Model Predictive Control (MPC) is a popular control strategy used in various applications. It is a feedback control strategy that uses a model of the system to predict future behavior and optimize control inputs. In this note, we will discuss the basics of MPC, its variants, applications, and comparisons to other control schemes.

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

## Variants of MPC
There are several variants of MPC, including:
- Linear MPC
- Nonlinear MPC
- Robust MPC
- Stochastic MPC
- Distributed MPC

## Applications of MPC
MPC has been used in various applications, including:
- Chemical processes
- Automotive control
- Robotics
- Aerospace
- Power systems

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
MPC has several advantages over other control schemes, including:
- Ability to handle constraints
- Ability to handle nonlinear systems
- Ability to handle disturbances
- Ability to handle time-varying systems

However, MPC also has some limitations, including:
- High computational requirements
- Sensitivity to model inaccuracies
- Limited ability to handle large-scale systems

MPC has been compared to other control schemes, such as PID control and LQR, to determine its effectiveness in different scenarios.

## MPC and RL Intersection
MPC and Reinforcement Learning (RL) are two popular control strategies that have been used in various applications. The intersection of these two strategies has been explored in recent years. 

## NMPC-based UAV 3D Target Tracking In The Presence Of Obstacles and Visibility Constraints
This code is the source code of the paper titled "NMPC-based UAV 3D Target Tracking In The Presence Of Obstacles and Visibility Constraints". The code is available on GitHub.

## Conclusion
MPC is a powerful control strategy that has been used in various applications. It has several advantages over other control schemes, but also has some limitations. Understanding the basics of MPC, its variants, applications, and comparisons to other control schemes is important for anyone interested in control theory.