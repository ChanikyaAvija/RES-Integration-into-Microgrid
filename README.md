# 🌱 Renewable Energy Sources Integration into a Microgrid  
*A Hybrid Solar–Wind–Battery Grid-Connected System (MATLAB/Simulink)*

This project presents the design and simulation of a **hybrid renewable energy microgrid** integrating **Solar PV**, **Wind Energy Conversion System (WECS)**, and a **Battery Energy Storage System (BESS)** into a stable **DC microgrid**, followed by AC grid synchronization through a controlled inverter.  
The system is developed and tested using **MATLAB/Simulink**.

---

## 🔋 Project Overview

Modern power systems are gradually shifting toward decentralized and sustainable energy solutions. However, renewable sources like solar and wind are naturally **intermittent**. This project addresses that challenge by combining multiple sources and integrating a **battery storage unit** to maintain stability, reliability, and continuous power flow.

The hybrid system includes:

- **Solar PV Generation**
- **Wind Turbine + PMSG**
- **Battery Energy Storage**
- **DC–DC Converters (Boost & Bidirectional)**
- **MPPT Algorithms**
- **Grid-Tied Inverter with PLL Synchronization**
- **DC Microgrid Architecture**

---

## ⚡ System Architecture

### **1. Solar PV Subsystem**
- User-defined PV array (8 modules in series, 1 string)
- Maximum power ~2 kW at STC  
- **Incremental Conductance MPPT** used for maximum power extraction  
- **Boost converter** steps up the voltage to the DC bus

### **2. Wind Energy Conversion Subsystem**
- Wind turbine rated at **2.5 kW**
- Permanent Magnet Synchronous Generator (**PMSG**)
- AC output rectified via **diode bridge**
- **P&O MPPT** algorithm optimizes wind energy capture  
- DC–DC **boost converter** regulates output to the DC microgrid

### **3. Battery Energy Storage System**
- Lithium-Ion battery bank  
- Rated at **240 V, 48 Ah (≈ 11.52 kWh)**  
- Connected through a **bidirectional buck–boost converter**
- Supports:
  - **Charging** (absorbs excess renewable power)
  - **Discharging** (supplies power during deficits)
- DC-bus voltage regulation + SoC-based control

### **4. Inverter + Grid Interconnection**
- Full-bridge voltage source inverter (VSI)
- **d-q reference frame control** for active & reactive power flow
- **PLL (Phase-Locked Loop)** for perfect grid synchronization
- Allows:
  - Exporting power to grid  
  - Supplying local loads  
  - Maintaining AC voltage and frequency

---

## 🔧 Control Algorithms Used

| Subsystem | Control Method | Purpose |
|----------|----------------|---------|
| Solar PV | Incremental Conductance MPPT | Extract maximum PV power under varying irradiance |
| Wind Turbine | Perturb & Observe (P&O) MPPT | Capture optimum wind power |
| Battery | DC-bus Voltage Control + SoC Logic | Maintain DC link stability and energy balance |
| Inverter | d-q Current Control + PWM + PLL | Grid synchronization & power quality |

---

## 🧩 Block Diagram Summary
<img width="800" height="600" alt="Block Diagram" src="https://github.com/user-attachments/assets/c7bf947c-fc14-41e0-b4b2-ffd498771a90" />


