# Limitations and Future Work

The project demonstrated the practical benefits and limitations of PI, PID and MPC velocity control on a small-scale autonomous vehicle.

## Main Limitations

- Controller gains and motor parameters were tuned manually.
- The MPC relied on a simplified motor model.
- External load torque was not explicitly estimated.
- The MPC implementation used only partial constraint handling.
- Larger prediction and control horizons increased computational load on the embedded hardware.
- The simulation model was intended for controller verification rather than high-fidelity physical prediction.

---

## Future Work

Possible extensions include:

- disturbance observers,
- adaptive or robust MPC,
- automatic motor-parameter identification,
- explicit MPC,
- lightweight embedded optimization,
- and improved real-time constraint handling.
