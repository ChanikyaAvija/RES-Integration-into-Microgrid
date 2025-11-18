# Architecture Overview

This document describes the high-level structure of the Simulink model.

## Main Subsystems

- **PV MPPT (Boost Converter)**  
  - Perturb & Observe (P&O) and Incremental Conductance MPPT blocks are implemented.
  - A DC–DC boost converter extracts maximum power from PV modules.

- **Wind MPPT (Turbine + Converter)**  
  - Wind energy conversion block with PO MPPT for rotor/turbine-side optimization.
  - Converter interfaces the wind generator to the DC bus.

- **Battery Energy Storage (Bidirectional DC/DC)**  
  - Controls charging/discharging to maintain DC-bus voltage and state-of-charge (SOC).
  - Employs a bidirectional converter (buck/boost) controlled by a voltage controller and PWM generator.

- **DC Load and Boost converter**  
  - Local DC loads and boost stage for regulated DC bus.

- **Grid-Connected Full-Bridge Inverter**  
  - Inverts DC bus voltage to AC for grid injection.
  - Includes LCL filter and synchronization with the grid.

## Data Flow
- Renewable sources (PV, Wind) feed the DC bus via their respective converters and MPPT controllers.
- The battery converter balances DC-bus power and provides smoothing under transients.
- The inverter synchronizes with the grid and injects/absorbs active/reactive power as controlled by the inverter controller block.

