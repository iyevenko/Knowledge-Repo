---
description: This note discusses the concepts of controllability and convergence in linear control systems, including definitions, simplifications, and the controllability matrix, as well as the infinite horizon objective function and feedback control law for LQR convergence.
---
# Controllability and Convergence in Linear Control Systems

## Controllability in Linear Time-Invariant Systems

### Definition
A system is controllable if any state in the state space can be reached in finite time from any other state. In other words, the system can be controlled to reach any desired state.

### Linear Discrete Time System
A linear discrete time system x+ = Ax + Bu is controllable if there exists a finite time N and a sequence of inputs (u(0), u(1),...u(N - 1)) that can transfer the system from any x to any z.

### Simplification
The matrix powers Ak for k  n are expressible as linear combinations of the powers 0 to n - 1. Therefore, the range of the matrix B AB AN-1B for N 2n is the same as B AB An-1 B. In other words, if we cannot reach z in n moves, we cannot reach it in any number of moves.

### Controllability Matrix
The controllability matrix C is defined as C = B AB An-'B. The system (A, B) is controllable if and only if the rows of the n X nm controllability matrix are linearly independent.

### Conclusion
The question of controllability of a linear time-invariant system is a question of existence of solutions to linear equations for an arbitrary right-hand side. Controllability is an important concept in control theory and is necessary for designing effective control schemes.

## Convergence of the Linear Quadratic Regulator

### Objective Function
- Define the infinite horizon objective function:
  - V(x,u) = 1/2 * (k=0 to ) [x(k)'Qx(k) + u(k)'Ru(k)]
  - subject to x+ = Ax + Bu and x(0) = x
- Q and R are positive definite matrices
- If (A,B) is controllable, the optimal solution to the optimization problem min V(x,u) exists and is unique for all x
- Denote the optimal solution by u(x), and the first input in the optimal sequence by u(x)

### Feedback Control Law
- The feedback control law K() for this infinite horizon case is defined as u = Ko(x) in which Koo(x) = u(x) = u(0;x)

### LQR Convergence
- Lemma 1.3 (LOR convergence): For (A,B) controllable, the infinite horizon LQR with Q, R > 0 gives a convergent closed-loop system
- x* = Ax + BK(x)