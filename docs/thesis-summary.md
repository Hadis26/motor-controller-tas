# Project Summary

## Problem

The TAS small-scale autonomous vehicle originally used a PI velocity controller within its Field-Oriented Control architecture.

Experimental tests showed several limitations in the baseline response, including:

- overshoot,
- oscillations,
- steady-state error,
- and non-ideal transient behavior.

The goal of the project was to investigate whether more advanced velocity-control strategies could improve the motor response while remaining practical for embedded implementation.

---

## Approach

Three controllers were evaluated.

### PI Controller

The existing PI controller served as the baseline.

### PID Controller

The PID controller extended the baseline approach with derivative action and low-pass filtering.

Its purpose was to improve transient response and reduce overshoot and oscillations.

### Model Predictive Control

The MPC used a discrete-time state-space model to predict future motor-speed behavior over a finite horizon.

The controller optimized the future control action by balancing:

- tracking accuracy,
- and control effort.

The controllers were first evaluated in a simplified simulation environment and then tested experimentally on the TAS vehicle.

---

## Key Findings

The **PID controller** improved the baseline PI response by reducing overshoot and significantly damping oscillations.

The **MPC controller** achieved the strongest nominal tracking performance, with:

- minimal overshoot,
- negligible oscillation,
- low steady-state error,
- and fast settling behavior.

However, the MPC was more sensitive to:

- model uncertainty,
- external load torque,
- inaccurate motor parameters,
- and embedded computational limitations.

The experiments therefore highlighted an important practical trade-off:

> More advanced control can improve nominal performance, but model accuracy and computational resources become increasingly important.

---

## Main Contributions

- Comparison of PI, PID and MPC velocity-control strategies
- Design and tuning of an improved PID controller
- Design and implementation of a Model Predictive Controller
- Simulation-based verification of controller behavior
- Experimental validation on a small-scale autonomous vehicle
- Analysis of load disturbances and model uncertainty
- Evaluation of MPC feasibility on embedded hardware

---

## Engineering Areas

The project combines concepts from:

- automatic control,
- Model Predictive Control,
- PID control,
- Field-Oriented Control,
- embedded systems,
- motor control,
- state-space modeling,
- and experimental validation.
