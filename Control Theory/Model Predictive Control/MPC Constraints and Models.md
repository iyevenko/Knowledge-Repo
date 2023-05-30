---
description: An overview of constraints, models, and residual specification in Model Predictive Control (MPC), including the format of user attributes and the dynamic programming solution.
---
# Model Predictive Control - Constraints, Models, and Residual Specification

## Overview
This markdown note covers information from the "MPC-book-2nd-edition-1st-printing.pdf" preview window. Specifically, it covers constraints, models, and residual specification in Model Predictive Control (MPC).

## Constraints
MPC includes constraints on manipulated inputs, which are typically bounded. These constraints are represented by linear inequalities. Constraints can also be imposed on states or outputs for safety, operability, and product quality reasons. 

## Models
MPC uses a state space model, which includes an augmented system model to maintain the state space form of the model. The manipulated inputs are represented by valve positions, voltages, torques, etc. 

## Augmented System Model
To limit the rate of change of the input, u(k) - u(k - 1), the state is augmented as w(k). The augmented system model becomes x+(k) = AX(k) + Bu(k) and y(k) = CX(k).

## Residual Specification
In Model Predictive Control, the cost is a sum of terms, each computed as the norm of a residual vector. The residual vector is defined by user sensors, and the norm for each term is defined by the user attribute of the respective user sensor. The residual function is specified in C++ and takes in the model and data as inputs.

### Format of User Attribute
The user attribute of the user sensor is defined in the following format:

```
<sensor>
    <user name="[term_name]" dim="[residual_dimension]" user="[norm_type] [weight] [weight_lower_bound] [weight_upper_bound] [norm_parameters...]">
</sensor>
```

- `term_name`: String describing term name (to appear in GUI).
- `residual_dimension`: Number of elements in residual.
- `norm_type`: Integer corresponding to the NormType enum, see norms.
- `weight`: Real number specifying weight value of the cost.
- `weight_lower_bound`, `weight_upper_bound`: Real numbers specifying lower and upper bounds weight, used for configuring the GUI slider.
- `norm_parameters`: Optional real numbers specifying norm-specific parameters, see norm implementation.

### Declaring User Sensors
All sensors should be defined in the task file, and the user sensors defining the residuals should be declared first. After the cost terms are specified, more sensors can be defined to specify the task, e.g., when the residual implementation relies on reading a sensor value. If a sensor named `trace%i` exists, the GUI will use it to draw the traces of the tentative and nominal trajectories.

## Optimal Control Problem
The optimal control problem PN(x) is defined by (2.7) with the cost function V ( ) defined by (2.3) and the constraints by (2.4).

## Dynamic Programming Solution
DP yields an optimal policy HO = (Ag(), ur , . .., A-1(-)), i.e., a sequence of control laws Mi: X; - U, i = 0,1,..., N - 1. The domain X; of each control law will be defined later. The optimal controlled system is time varying and satisfies x+ = f(x, u? (x)), i = 0,1,..., N - 1.

## Comparison with MPC
The system using MPC is time invariant and satisfies x* = f(X, KN(x)), i = 0,1,..., N -1 with KN () = u%(-). The optimal control law at time i is u (-), but receding horizon control (RHC) uses the time-invariant control law KN ( ) Mo() obtained by assuming that at each time t, the terminal time or horizon is t + N so that the horizon t + N recedes as t increases. One consequence is that the time-invariant control law KN(- ) is not optimal.

## Conclusion
This information provides an overview of constraints, models, and residual specification in MPC. For more information on MPC and its many variants, applications, and comparisons to other control schemes, refer to the "Control Theory" folder.