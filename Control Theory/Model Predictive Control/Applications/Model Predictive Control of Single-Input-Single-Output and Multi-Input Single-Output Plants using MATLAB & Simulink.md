---
description: This note provides an overview of how to design and simulate Model Predictive Control (MPC) for both single-input-single-output and multi-input-single-output plants using MATLAB and Simulink. It includes examples of designing MPC controllers, examining steady-state offset, simulating closed-loop responses with and without model mismatch, softening constraints, changing built-in state estimator Kalman gains, simulating controllers in closed loop, obtaining linear representations of MPC controllers, simulating using Simulink, and simulating with sinusoidal output.
---
[7] ## Model Predictive Control of Multi-Input Single-Output Plant

[8] ### Define Plant Model
For this example, we use continuous-time transfer functions from each input to the output. The plant model is defined using the following code:
```
plantTF tf((1,1,1}, {(1 .5 1], (1 1], [.7 .5 1]})
```
We then convert the transfer function to continuous state space and specify a sample time of 0.2 seconds using the following code:
```
plantCSS = ss (plantTF);
TS = 0.2;
plantDSS = c2d (plantCSS, Ts)
```

[9] ### Design MPC Controller
The MPC controller creation function can accept either continuous-time or discrete-time plants. During initialization, a continuous-time plant (in any format) is automatically converted into a discrete-time state-space model using the zero-order hold (ZOH) method. We can then design the MPC controller using the following code:
```
mpcobj = mpc(plantDSS);
```

[10] ### Examine Steady-State Offset
We can examine the steady-state offset of the system using the following code:
```
mpcobj.Model.Nominal.Y = 1;
mpcobj.Model.Nominal.U = 0;
[y, t] = simulate(plantDSS, mpcobj);
```

[11] ### Simulate Closed-Loop Response Using s^2 + 0.5 S
We can simulate the closed-loop response of the system using the following code:
```
mpcobj.Weights.OutputVariables = [1 0 0 0];
mpcobj.Weights.ManipulatedVariables = 0.1;
sim(plantDSS, mpcobj);
```

[12] ### Simulate Closed-Loop Response with Model Mismatch
We can simulate the closed-loop response of the system with model mismatch using the following code:
```
plantDSSmismatch = plantDSS;
plantDSSmismatch.a(1,2) = 0.2;
mpcobjmismatch = mpc(plantDSSmismatch);
sim(plantDSSmismatch, mpcobjmismatch);
```

[13] ### Simulate Open-Loop Response S + 1
We can simulate the open-loop response of the system using the following code:
```
sys = tf([1], [1 1]);
sysd = c2d(sys, Ts);
mpcobj = mpc(sysd);
sim(sysd, mpcobj);
```

[14] ### Soften Constraints
We can soften the constraints of the system using the following code:
```
mpcobj.MV(1).Min = -0.5;
mpcobj.MV(1).Max = 0.5;
mpcobj.MV(1).RateMin = -0.1;
mpcobj.MV(1).RateMax = 0.1;
sim(plantDSS, mpcobj);
```

[15] ### Change Built-In State Estimator Kalman Gains
We can change the built-in state estimator Kalman gains using the following code:
```
mpcobj.Model.Plant = ss(plantDSS.a, plantDSS.b, eye(5), 0);
mpcobj.Model.Noise = diag([0.1 0.1 0.1 0.1 0.1]);
mpcobj.Model.StateEstimation = 'Kalman';
mpcobj.Model.StateEstimationParameters = struct('Q', 1e-5, 'R', 1e-2);
sim(plantDSS, mpcobj);
```

[16] ### Simulate Controller in Closed Loop Using mpcmove
We can simulate the controller in closed loop using mpcmove function using the following code:
```
u = mpcmove(plantDSS, x0, yref, y, [], mpcobj);
```

[17] ### Linear Representation of MPC Controller
We can obtain the linear representation of the MPC controller using the following code:
```
mpcobjlin = linearize(mpcobj, x0, yref);
```

[18] ### Simulate Using Simulink
We can simulate the system using Simulink by following the steps mentioned in the documentation.

[19] ### Simulation with Sinusoidal Output
We can simulate the system with sinusoidal output using the following code:
```
plantTF = tf([1 1], [1 0.5 1]);
plantCSS = ss(plantTF);
plantDSS = c2d(plantCSS, Ts);
mpcobj = mpc(plantDSS);
mpcobj.Weights.OutputVariables = [1 0];
sim(plantDSS, mpcobj);
```

This concludes the overview of Model Predictive Control of Single-Input-Single-Output and Multi-Input Single-Output Plants using MATLAB & Simulink.