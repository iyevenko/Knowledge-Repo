---
description: An overview of Model Predictive Control. Just the high level stuff.
---
# Control Theory and Model Predictive Control Overview

## Control Theory

Control theory is a branch of engineering and mathematics that deals with the analysis and design of systems that are subject to control. It involves the use of mathematical models to describe the behavior of a system, and the design of control algorithms to manipulate the system to achieve desired objectives.

## Model Predictive Control (MPC) Overview

Model predictive control (MPC) is an advanced method of process control that is used to control a process while satisfying a set of constraints. It has been in use in the process industries in chemical plants and oil refineries since the 1980s. In recent years, it has also been used in power system balancing models and in power electronics.

### High-level overview of MPC

- MPC allows the current timeslot to be optimized, while keeping future timeslots in account. This is achieved by optimizing finite time-horizon, but only implementing the current timeslot and then optimizing again, repeatedly, thus differing from a linear-quadratic regulator (LQR).
- MPC has the ability to anticipate future events and can take control actions accordingly. PID controllers do not have this predictive ability.
- MPC relies on dynamic models of the process, most often linear empirical models obtained by system identification.
- MPC is nearly universally implemented as a digital control, although there is research into achieving faster response times with specially designed analog circuitry.
- Generalized predictive control (GPC) and dynamic matrix control (DMC) are classical examples of MPC.
- The models used in MPC are generally intended to represent the behavior of complex and simple dynamical systems.
- Common dynamic characteristics that are difficult for PID controllers include large time delays and high-order dynamics.
- MPC models predict the change in the dependent variables of the modeled system that will be caused by changes in the independent variables.
- Nonlinear MPC can be used when linear models are not sufficiently accurate to represent the real process nonlinearities.
- The prediction horizon keeps being shifted forward and for this reason MPC is also called receding horizon control.

### Comparison to other control schemes

Compared to other control schemes, MPC has the following advantages:

- MPC allows for optimization of future time-horizons, while PID controllers only optimize the current time-step.
- MPC has the ability to anticipate future events and can take control actions accordingly, while PID controllers do not have this predictive ability.
- MPC relies on dynamic models of the process, while PID controllers do not require a model of the process.
- MPC is nearly universally implemented as a digital control, while PID controllers can be implemented as either analog or digital controls.
- Nonlinear MPC can be used when linear models are not sufficiently accurate to represent the real process nonlinearities, while PID controllers are generally limited to linear systems.

### Applications of Model Predictive Control

MPC has been used in various industries, including:

- Chemical plants
- Oil refineries
- Power system balancing models
- Power electronics.

## Conclusion

Model Predictive Control is a powerful control scheme that has found many applications in various fields, including process control, robotics, and autonomous vehicles. It allows for optimization of future time-horizons, can anticipate future events, and can handle constraints and uncertainties in the system. However, it can be computationally expensive and requires a good model of the system being controlled.