# Inverter Control

The inverter subsystem implements a grid-connected full-bridge inverter with the following control components:

- **Phase-Locked Loop (PLL)** for grid synchronization.
- **dq-transformation** based current control (unbalanced d-q frame handling included).
- **Current PI controllers** to regulate injected currents (Iq / Id) according to references.
- **PWM generator** to create gate signals for the full-bridge switches.
- **LCL filter** at the point of common coupling (PCC).

Refer to `model/blocks_summary.csv` and `model/blocks_full.json` to inspect PI gains, filter values, and PWM carrier frequencies used.
