# (99942) Apophis Orbital Transition & N-Body Integration Framework

[![Journal](https://shields.io)](https://aasjournals.org)
[![ORCID](https://shields.io)](https://orcid.org)
[![Physics](https://shields.io)](https://readthedocs.io)

This repository hosts the high-precision N-body numerical integration pipelines, local contingency data structures, and osculating elements transformation matrices designed to analyze the historical close approach of the hazardous Aten-class near-Earth asteroid **(99942) Apophis** on April 13, 2029.

This software framework serves as the reproducible open-science benchmark supporting the full-length research manuscript submitted to ***The Astronomical Journal***.

## 🪐 Project Architecture & Physics

The pipeline utilizes the implicit 15th-order Gauss-Radau adaptive integrator (**IAS15 engine**) embedded within the `REBOUND` simulation ecosystem. To eliminate non-inertial frame drifts and ensure sub-kilometer precision during deep perigee tracking, the simulation directly couples heliocentric state vectors with individual, real-time Earth and Moon coordinate tensors.

### Key Analytical Features:
* **Deterministic Perigee Tracking:** Resolves a precise geocentric minimum approach radius of **38,011.82 km**, tracking the bolide deep within the terrestrial geosynchronous ring.
* **Orbital Mutation Matrix:** Maps the immediate expansion of the heliocentric semi-major axis jumping from a pre-encounter state of **0.9241 AU** to a permanent post-encounter baseline of **0.9535 AU**, documenting the physical transition from an Aten-class into an Apollo-class family orbit.
* **Osculating Eccentricity Strain:** Captures a severe non-monotonic deformation profile peaking at **0.1960** at the minimum perigee vertex before stabilizing at a lower boundary condition of **0.1812**.
* **Contingency Sub-matrix:** Incorporates an integrated localized vector array to ensure structural workflow continuity and mathematical integrity during interferences or intermitencias with the JPL Horizons ephemeris servers.

## 📂 Repository Layout

* `apophis_2029_encounter.ipynb`: Main Jupyter / Google Colab notebook containing the local contingency matrices, N-body integration blocks, and `matplotlib` dual-panel analytical plots.
* `requirements.txt`: Environment configuration file listing essential scientific software dependencies.

## 🚀 Environment Initialization

To initialize this coupled astronomical framework locally or inside a Google Colab notebook instance, deploy the following environment parameters:

```bash
pip install -r requirements.txt
```

## 🎓 Author & Open Science Compliance

* **Author:** René Sagal Andrade
* **Role:** Independent Researcher / System Architect & Astro-aerospace Analyst
* **Academic Background:** University College London (UCL) Alumnus
* **Identifier:** [ORCID: 0009-0006-8968-301X](https://orcid.org)

*The author explicitly acknowledges the computational validation frameworks and algorithmic workflow optimization support provided by Google's Smart Mode processors throughout the formulation of this independent astronomical software architecture.*
