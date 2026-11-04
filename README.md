# (99942) Apophis High-Precision N-Body Dynamics & Yarkovsky Thermal Drift Model

[![ORCID](https://shields.io)](https://orcid.org)
[![Journal](https://shields.io)](https://aasjournals.org)
[![Physics Engine](https://shields.io)](https://readthedocs.io)
[![License: MIT](https://shields.io)](https://opensource.org)

This repository hosts the high-precision astronomical numerical software framework, hybrid execution pipelines, and non-gravitational acceleration algorithms designed to integrate the April 13, 2029 close encounter of near-Earth asteroid **(99942) Apophis**.

This standalone pipeline serves as the reproducible open-science benchmark supporting the research manuscript titled *"Orbital Class Mutation and High-Precision N-Body Dynamics of Asteroid (99942) Apophis"*.

## 🪐 Core Architecture & Physical Benchmarks

The integration framework deploys a **Hybrid Execution Architecture** combining primary live queries to the NASA/JPL Horizons API (via `astroquery`) with an explicit local JSON sub-matrix to guarantee operational continuity during database intermitencias or air-gapped executions.

### Key Simulation Milestones Resolved:
* **Standard Newtonian Perigee Calibration:** Resolves a precise geocentric minimum approach radius of **36,082.12 km** using the adaptive 15th-order Gauss-Radau implicit integrator (`IAS15`), positioning the bolide underneath the Earth's geosynchronous satellite ring ($35,786 \text{ km}$ altitude baseline).
* **Dynamic Node Convergence:** Maps an exact post-perigee alignment intersection on relative day **14.73** from initialization, where Newtonian N-body mechanics and non-gravitational trajectories dynamically converge onto identical geometric spatial nodes.
* **Yarkovsky Drift Isolation:** Quantifies the minute relativistic acceleration drag induced by anisotropic solar radiation re-emission (diurnal Yarkovsky effect via the transverse $A_2$ vector), isolating a final orbital displacement of exactly **0.00018 km** ($18.0 \text{ cm}$).
* **Numerical Constraints:** Operates under a strict local truncation error threshold ($\tau = 10^{-12}$), ensuring total mathematical consistency throughout the intense planet-centric gravitational well.

## 📂 Repository Layout

* `apophis_yarkovsky_simulation.ipynb`: Main Jupyter / Google Colab notebook enclosing the hybrid vector resolvers, adaptive integration cells, and matplotlib trajectory log output.
* `data/initial_state_vectors_20290401.json`: Local contingency baseline structures encapsulating calibrated J2000 state vectors relative to the Sun.
* `requirements.txt`: Environment configuration file listing essential scientific software dependencies.

## 🚀 Environment Initialization

To deploy and execute this standalone non-gravitational model inside a clean environment, initialize the dependencies via:

```bash
pip install -r requirements.txt
```

## 🎓 Author & Open Science Compliance

* **Author:** René Sagal Andrade
* **Role:** Independent Researcher / System Architect & Astro-aerospace Analyst
* **Academic Background:** University College London (UCL) Alumnus
* **Identifier:** [ORCID: 0009-0003-5574-5384](https://orcid.org)

*The author explicitly acknowledges the computational validation frameworks and algorithmic workflow optimization support provided by Google's Smart Mode processors throughout the formulation of this independent astronomical software architecture.*
