# MPPT Algorithms implemented

This model includes two commonly used MPPT (Maximum Power Point Tracking) algorithms:

## 1. Perturb & Observe (P&O)
- Perturbs operating voltage or duty-cycle and observes power change.
- If power increases, continue perturbation direction; otherwise reverse.
- Simple and widely used, may oscillate around MPP.

## 2. Incremental Conductance (IncCond)
- Uses the derivative dP/dV = 0 at MPP: compares incremental conductance (dI/dV) to instantaneous conductance (I/V).
- Better performance in rapidly changing irradiance conditions.

Both MPPT blocks drive the DC–DC converter duty cycle via a PWM generator. Check `model/blocks_summary.csv` and the model subsystems to see concrete parameter names used in the implementation.
