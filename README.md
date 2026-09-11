# EV Battery Management System (BMS) Simulation

A MATLAB/Simulink implementation of a Battery Management System (BMS) designed for electric vehicle (EV) battery packs. This project models a 3-cell series (3S1P) Lithium-Ion battery pack featuring real-time State-of-Charge (SoC) estimation, voltage and thermal fault monitoring, debounced signal processing, and state-machine-driven contactor protection.

---

## 🚀 Key Features

* **State-of-Charge (SoC) Estimation:** Implements discrete-time Coulomb counting integration to track pack SoC, remaining capacity, and energy output in real time.
* **Fault Detection & Signal Debouncing:** Monitors individual cell voltages and module temperatures using debounced error counters to prevent false-positive fault triggers.
* **State-Machine Control:** Built using Stateflow/logic state machines to manage seamless transitions across `Idle`, `Discharge`, `Charge`, and `Fault` operational modes.
* **Automated Contactor Isolation:** Automatically trips high-voltage safety contactors to isolate the pack upon detecting over-voltage, under-voltage, or thermal safety violations.
* **Dynamic Cell Modeling:** Incorporates lookup tables for Open-Circuit Voltage ($OCV\text{--}SoC$) and Internal Resistance ($R_{int}\text{--}Temp$) dynamics.

---

## 📂 Repository Structure

* `BMS.slx` — Main Simulink simulation model containing the 3S1P battery pack, sensor blocks, control state machine, and interactive dashboard.
* `BMSLib.slx` — Custom Simulink block library containing reusable debounce filter components.
* `Variables.m` — MATLAB initialization script defining pack parameters, lookup matrices, sample times, and safety thresholds.

---

