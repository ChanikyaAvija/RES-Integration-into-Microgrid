# Grid-Connected Hybrid PV & Wind Generator system with Battery Energy Storage

This repository contains the Simulink model and supporting files for a **grid-connected hybrid photovoltaic (PV) + wind generation system** with a battery energy storage system (BESS). The model includes MPPT algorithms (Incremental Conductance and Perturb & Observe variants), DC–DC converters (boost, bidirectional), and a grid-connected full-bridge inverter.

## Contents

```
Grid-Connected-Hybrid-PV-Wind-BESS/
├── model/
│   ├── Singlephase_INC_grid.slx        # Main Simulink model (SLX)
│   ├── slx_model_extracted.xml         # Extracted model XML (for inspection)
│   ├── blocks_summary.csv              # Summary of blocks & parameters
│   ├── blocks_full.json                # Full block parameter dump (JSON)
│   └── images/
│       └── system_*.png/jpg            # Screenshots of the model diagram
├── matlab/
│   ├── Design_BoostPV.m
│   ├── Design_Boostwind.m
│   ├── Design_Boostbat.m
│   └── LCL_Calculation.m
├── docs/
│   ├── architecture.md
│   ├── mppt_algorithms.md
│   ├── inverter_control.md
│   └── block_parameters.md
├── .gitignore
├── LICENSE (MIT)
└── README.md
```

## How to use

1. **Requirements**
   - MATLAB with Simulink installed (compatible with `.slx` files).
   - Recommended: Recent MATLAB release (R2018b or later) with Simscape / SimPowerSystems if using physical components.

2. **Open the model**
   - Open `model/Singlephase_INC_grid.slx` in MATLAB/Simulink.
   - Inspect subsystems or run simulations after configuring solver and parameters.

3. **Documentation**
   - Read the files in the `docs/` folder for an overview of architecture, MPPT approaches used, and inverter control strategy.
   - `model/blocks_summary.csv` provides a quick reference of blocks and key parameters.

4. **Licensing**
   - See `LICENSE` (MIT). Adjust if you prefer another license.

## Notes
- The `slx_model_extracted.xml`, `blocks_full.json`, and `blocks_summary.csv` were generated to help review and document the model programmatically.
- If you intend to publish the `.slx` file in a public repo, ensure that you are allowed to share any third-party licensed blocks or protected content.

---

If you want, I can:
- Initialize a Git repository and make an initial commit here.
- Create a ZIP of the repo ready for upload to GitHub.
- Generate a short `CONTRIBUTING.md` or sample GitHub Actions workflow for automated checks.
