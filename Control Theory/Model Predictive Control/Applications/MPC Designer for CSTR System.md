---
description: A step-by-step guide to designing a Model Predictive Controller (MPC) using MPC Designer in MATLAB & Simulink, covering input and output channel attributes, simulation scenario configuration, controller horizon definition, input constraints, and tuning weights.
---
# Designing a Model Predictive Controller using MPC Designer

## Introduction
This note provides a step-by-step guide to designing a Model Predictive Controller (MPC) using MPC Designer in MATLAB & Simulink.

## CSTR Model

The linearized model of a Continuously Stirred Tank Reactor (CSTR) is shown in this section. The model includes the concentration of reagent (C) and the temperature of the reactor (T) as state variables, and the coolant temperature (Tc) and the inflow feed reagent concentration (CA) as inputs.

## MPC Designer
MPC Designer is a graphical user interface (GUI) tool that allows users to design and simulate MPC controllers. It provides a range of features, including input and output channel specifications, simulation scenario configuration, controller horizon definition, input constraints, tuning weights, and more.

## Input and Output Channel Attributes
To define input and output channel attributes in MPC Designer, follow these steps:
1. Select 1/0 Attributes on the MPC Designer tab.
2. In the Input and Output Channel Specifications dialog box, specify a meaningful name for each input and output channel in the Name column.
3. Optionally, specify the units for each channel in the Unit column.
4. Keep the Nominal Value for each input and output channel at 0, since the state-space model is defined using deviations from the nominal operating point.
5. Keep the Scale Factor for each channel at the default value of 1.

## Import Plant and Define MPC Structure

This section explains how to import the plant and define the MPC structure. It includes information on attributes and input/output channels.

## Simulation Scenario Configuration
To configure a simulation scenario in MPC Designer, follow these steps:
1. Click Edit Scenario > scenario1 in the Scenario section on the MPC Designer tab.
2. In the Simulation Scenario dialog box, set the Simulation duration to the desired value.
3. Specify the reference signals in the Reference Signals table. For example, you can specify a step size and time for each reference signal.
4. Select a Constant reference for the concentration setpoint to hold it at its nominal value, which is defined in the Input and Output Channel Specifications dialog box.

## Controller Horizon Definition
To define the controller horizon in MPC Designer, follow these steps:
1. Click Edit Controller > Controller Settings in the Controller section on the MPC Designer tab.
2. In the Controller Settings dialog box, specify the prediction and control horizons.
3. Optionally, specify the weights for the prediction and control horizons.

## Define Input Constraints
This section explains how to define input constraints for the MPC controller.

## Input Constraints
To specify input constraints in MPC Designer, follow these steps:
1. Click Edit Controller > Input Constraints in the Controller section on the MPC Designer tab.
2. In the Input Constraints dialog box, specify the lower and upper bounds for each input channel.

## Specify Controller Tuning Weights
This section details how to specify controller tuning weights to optimize controller performance.

## Tuning Weights
To specify tuning weights in MPC Designer, follow these steps:
1. Click Edit Controller > Tuning Weights in the Controller section on the MPC Designer tab.
2. In the Tuning Weights dialog box, specify the weights for the input and output channels.

## Eliminate Output Overshoot
This section explains how to eliminate output overshoot in the MPC controller.

## Test Controller Disturbance Rejection
This section details how to test the MPC controller's ability to reject disturbances.

## Specify Concentration Output Constraint
This section explains how to specify a concentration output constraint for the MPC controller.

## Conclusion
This note provides a brief overview of how to design a Model Predictive Controller using MPC Designer in MATLAB & Simulink. It covers input and output channel attributes, simulation scenario configuration, controller horizon definition, input constraints, and tuning weights. For more information, refer to the MATLAB documentation on MPC Designer.