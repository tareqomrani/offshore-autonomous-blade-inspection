<p align="center">
  <img src="images/banner7.PNG" alt="Offshore Autonomous Blade Inspection Mission Simulator V2" width="100%">
</p>

<h1 align="center">Offshore Autonomous Blade Inspection Mission Simulator V2</h1>

<p align="center">
<b>Concept-Level Systems Engineering Simulator for Autonomous Offshore Wind Turbine Blade Inspection</b>
</p>

<p align="center">
  <a href="https://www.python.org/">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  </a>
  <a href="https://streamlit.io/">
    <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
  </a>
  <a href="https://numpy.org/">
    <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
  </a>
  <a href="https://pandas.pydata.org/">
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  </a>
  <a href="https://plotly.com/python/">
    <img src="https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white" alt="Plotly">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Research-Prototype-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Systems-Engineering-1976D2?style=for-the-badge">
  <img src="https://img.shields.io/badge/Autonomous-UAS-2E7D32?style=for-the-badge">
  <img src="https://img.shields.io/badge/Offshore-Wind-0097A7?style=for-the-badge">
</p>

---

## Overview

**Offshore Autonomous Blade Inspection Mission Simulator V2** is a concept-level systems engineering application that investigates autonomous multirotor uncrewed aircraft system (UAS) operations for offshore wind turbine blade inspection. The simulator combines mission planning, propulsion and energy estimation, environmental modeling, blade-relative navigation concepts, geometric coverage assessment, inspection performance metrics, and engineering reporting into a unified research platform.

The software is intended for **research, education, concept development, and systems engineering trade studies**. It is **not** a validated flight-dynamics simulator, digital twin, operational flight-planning tool, structural health monitoring system, collision avoidance system, or automated defect-detection application.

---

# Motivation

Offshore wind turbine blade inspections are traditionally labor-intensive, costly, and potentially hazardous. Autonomous multirotor UAS platforms offer the potential to reduce personnel exposure while improving inspection efficiency and data collection. This simulator provides a framework for evaluating inspection architectures, mission feasibility, and engineering tradeoffs before real-world implementation.

---

# Objectives

The simulator supports:

- Autonomous offshore blade inspection concepts
- Systems engineering trade studies
- Mission planning and feasibility analysis
- Energy-aware autonomous operations
- Blade-relative navigation assessment
- Inspection performance evaluation
- Requirements traceability
- Engineering education and research

---

# Features

### Mission Planning

- Autonomous mission generation
- Blade-by-blade inspection sequencing
- Dual-pass inspection trajectories
- Hub-clearance maneuvers
- Return-to-launch planning
- Interactive 3D mission visualization

### UAS Platform Model

Configurable vehicle parameters include:

- Aircraft mass
- Rotor count
- Propeller diameter
- Rotor figure of merit
- Motor and ESC efficiency
- Aerodynamic drag
- Cruise speed
- Inspection speed
- Battery capacity
- Power limits

### Sensor Architecture

The inspection payload supports configurable:

- RGB camera
- LiDAR
- IMU

User-adjustable parameters include:

- Camera field of view
- Frame rate
- Optical quality
- LiDAR range
- LiDAR noise
- LiDAR update rate
- IMU quality
- Sensor synchronization error

### Blade-Relative Navigation

Mission performance can be evaluated under multiple navigation conditions:

- RTK Fixed
- RTK Float
- Standard GNSS
- Multipath / Degraded GNSS
- Alternate GNSS-Denied Navigation

The simulator models navigation uncertainty using simplified engineering assumptions suitable for concept-level analysis.

### Propulsion & Energy Modeling

Mission energy estimation includes:

- Rotor-induced power
- Profile power
- Aerodynamic drag
- Hotel loads
- Battery utilization
- Dynamic reserve prediction
- Return-energy estimation
- Automatic mission termination when reserve requirements are exceeded

### Environmental Modeling

Mission performance is influenced by:

- Mean wind speed
- Gusts
- Turbulence intensity
- Visibility
- Precipitation
- Wave height

Environmental conditions affect navigation uncertainty, energy consumption, hazard assessment, and inspection quality.

### Inspection Performance Metrics

Simulation outputs include:

- Geometric blade-surface coverage
- Image overlap
- Stand-off distance
- Relative navigation error
- Hazard Index
- Inspection Data Suitability Index
- Mission duration
- Final battery state of charge

---

# Systems Engineering

The simulator applies systems engineering principles by connecting operational needs with measurable engineering outputs.

Illustrative evaluation categories include:

| Requirement Area | Example Metric |
|------------------|----------------|
| Navigation | Relative navigation accuracy |
| Inspection | Geometric blade coverage |
| Energy | Battery reserve compliance |
| Mission | Operational feasibility |
| Safety | Rotor-proximity hazard index |

---

# Outputs

Each simulation generates:

- Interactive 3D mission visualization
- Mission summary dashboard
- Mission telemetry
- Coverage assessment
- Inspection quality metrics
- Battery and energy estimates
- Hazard assessment
- Markdown mission report
- CSV telemetry export
- JSON simulation export

---

# Technology Stack

| Component | Technology |
|-----------|------------|
| Programming Language | Python 3.11 |
| Web Framework | Streamlit |
| Numerical Computing | NumPy |
| Data Processing | Pandas |
| Visualization | Plotly |

---

# Repository Structure

```text
offshore-autonomous-inspection-platform/
│
├── app.py
├── README.md
├── requirements.txt
├── images/
├── docs/
│   └── User_Guide.pdf
├── examples/
└── assets/
```

---

# Installation

```bash
git clone https://github.com/tareqomrani/offshore-autonomous-inspection-platform.git

cd offshore-autonomous-inspection-platform

pip install -r requirements.txt

streamlit run app.py
```

---

# Typical Workflow

1. Configure turbine characteristics.
2. Define environmental conditions.
3. Configure the UAS platform.
4. Configure onboard sensors.
5. Execute the inspection mission.
6. Review mission telemetry and visualizations.
7. Evaluate engineering metrics.
8. Export reports and simulation data.

---

# Current Limitations

The current implementation does **not** include:

- Six-degree-of-freedom flight dynamics
- Rotor-wake interaction modeling
- Visual SLAM
- Extended Kalman Filter navigation
- Real-time obstacle avoidance
- Automated defect recognition
- Hardware-in-the-loop testing
- Flight-certified operational performance

Simulation outputs should therefore be interpreted as engineering trade-study results rather than validated operational predictions.

---

# Future Development

Planned enhancements include:

- Six-degree-of-freedom flight dynamics
- Wind-field modeling
- Visual-Inertial Odometry (VIO)
- Extended Kalman Filter navigation
- Visual SLAM
- Automated defect detection
- Predictive maintenance analytics
- Multi-UAS cooperative inspection
- Digital twin integration
- Hardware-in-the-loop validation

---

# References

- Carroll, J., et al. (2017). *Availability, operation and maintenance costs of offshore wind turbines.*
- Heo, S.-J., & Na, W. S. (2025). *Review of drone-based technologies for wind turbine blade inspection.*
- Oliveira, A., et al. (2024). *LiDAR-based UAV offshore wind blade inspection and modeling.*
- Shafiee, M., et al. (2021). *Unmanned aerial drones for inspection of offshore wind turbines: A mission-critical failure analysis.*
- Zhang, K., et al. (2024). *Inspection of floating offshore wind turbines using multi-rotor unmanned aerial vehicles.*

---

# Disclaimer

**Offshore Autonomous Blade Inspection Mission Simulator V2** is a **concept-level systems engineering research prototype**. It is intended to support engineering analysis, concept development, research, and education. The software has **not** been validated for operational flight planning, aircraft certification, aviation safety, collision avoidance, structural inspection, or automated defect detection. Simulation results should not be interpreted as validated operational performance predictions.

---

# Author

**Tareq Omrani**

AI Engineering • Autonomous Systems • UAS • Systems Engineering

**GitHub:** https://github.com/tareqomrani

**LinkedIn:** https://www.linkedin.com/in/tareqomrani

---

<p align="center">
<b>Version 2.0.0</b><br>
Concept-Level Systems Engineering Research Prototype
</p>
