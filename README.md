# Improvement of Motor Controller for Small-Scale Vehicles

This repository documents an engineering project completed at the
Technical University of Munich (TUM) as part of an *Ingenieurspraxis*
at the Chair of Automatic Control Engineering.

The project investigates improved velocity control for a small-scale
autonomous vehicle equipped with stepper motors and Field-Oriented
Control (FOC).

Three control strategies were evaluated:

- Proportional-Integral (PI) control
- Proportional-Integral-Derivative (PID) control
- Model Predictive Control (MPC)

The objective was to improve speed tracking while reducing overshoot,
oscillations and steady-state error, and to evaluate the practical
trade-offs of predictive control on embedded hardware.

---

## Project Motivation

The original TAS vehicle used a PI controller in the outer velocity-control
loop.

Experimental measurements showed:

- overshoot,
- oscillatory behavior,
- steady-state tracking error,
- and non-ideal transient response.

The project therefore investigated whether PID and MPC could improve the
velocity response while keeping the existing FOC structure.

---

## Approach

The inner current-control architecture of the vehicle was kept unchanged.

Only the outer velocity controller was replaced and evaluated.

```text
Reference Velocity
        ↓
Velocity Controller
   PI / PID / MPC
        ↓
Quadrature Current Reference
        ↓
Field-Oriented Control
        ↓
Motor Driver
        ↓
Stepper Motor
        ↓
Encoder Feedback
