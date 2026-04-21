# Two-Stage CMOS Operational Amplifier (0.18µm)

## Project Overview
This repository contains the design analysis and simulation results for a two-stage, Miller-compensated CMOS operational amplifier. The design was developed using a **0.18µm process** with a focus on optimizing stability (Phase Margin) and Open-Loop Gain through iterative hand calculations and Cadence Virtuoso verification.

## Architecture
The design utilizes a standard two-stage topology to maximize swing and gain:
* **Input Stage:** NMOS differential pair with PMOS active load.
* **Output Stage:** PMOS common-source amplifier with an NMOS current source load.
* **Compensation:** Miller capacitor ($C_c$) for pole-splitting to ensure frequency stability.
* **Biasing:** Precision resistive divider network used to establish stable tail and load currents.

## Design Methodology
The project followed a rigorous "Hand Calculation to Simulation" workflow:
1. **Analytical Modeling:** Used square-law equations to determine initial $W/L$ ratios for all transistors.
2. **Gain Optimization:** Iteratively increased $g_m$ through device sizing to meet the >60dB open-loop gain requirement.
3. **Verification:** Validated results in Cadence Virtuoso using AC analysis and transient response testing.

## Performance Summary
The final design met or exceeded all target specifications:

| Parameter | Target Spec | Result |
| :--- | :--- | :--- |
| **Open-Loop Gain** | $\ge 60$ dB | **77.9 dB** |
| **Unity-Gain BW** | $\ge 10$ MHz | **15.9 MHz** |
| **Phase Margin** | $\ge 60^\circ$ | **$60.5^\circ$** |
| **Slew Rate** | $\ge 10$ V/µs | **10.5 V/µs** |
| **Power Dissipation**| $\le 9$ mW | **1.51 mW** |

## Repository Contents
* **Project_Report.pdf:** Full technical breakdown including small-signal models, KVL/KCL derivations, and bias point summaries.
* **Specifications.pdf:** Summary of target constraints and final performance metrics.

---
*This project highlights the correlation between theoretical small-signal analysis and high-fidelity SPICE models in sub-micron processes.*
