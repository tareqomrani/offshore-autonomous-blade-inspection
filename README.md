<p align="center">
  <img src="images/banner.png" alt="Offshore Autonomous Blade Inspection Mission Simulator" width="100%">
</p>

<h1 align="center">
Offshore Autonomous Blade Inspection Mission Simulator V2
</h1>

<p align="center">
<b>Concept-Level Systems Engineering Simulator for Autonomous Offshore Wind Turbine Blade Inspection</b>
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-red)
![Status](https://img.shields.io/badge/Status-Research%20Prototype-orange)
![License](https://img.shields.io/badge/License-MIT-green)

</p>

---

# Overview

The **Offshore Autonomous Blade Inspection Mission Simulator V2** is a concept-level systems engineering platform developed to investigate autonomous multirotor uncrewed aircraft system (UAS) operations for offshore wind turbine blade inspection.

The simulator integrates mission planning, blade-relative navigation, propulsion and energy modeling, environmental effects, geometric inspection coverage, systems engineering requirements, and engineering performance metrics into a single research platform. Rather than serving as a flight simulator, the application supports architecture evaluation, engineering trade studies, and concept development for autonomous offshore inspection systems.

The project demonstrates how mission planning, sensing, navigation, and energy management may be integrated into a unified inspection architecture while providing measurable outputs that support systems engineering decision making.

> **Research Prototype**
>
> This application is intended solely for concept development and engineering analysis.
>
> It is **not** a validated flight-dynamics simulator, operational safety tool, digital twin, collision avoidance system, structural health monitoring system, or automated defect-detection application.

---

# Motivation

Offshore wind turbines require routine inspection to identify defects such as leading-edge erosion, coating degradation, cracks, lightning damage, and other structural anomalies.

Traditional inspection methods often require rope-access technicians, cranes, or crewed aircraft, resulting in higher operational costs, increased safety risks, and longer turbine downtime.

Autonomous multirotor UAS platforms offer the potential to improve inspection efficiency while reducing personnel exposure to hazardous offshore environments. This simulator investigates a proposed inspection architecture capable of supporting concept-level engineering analysis before physical implementation.

---

# Objectives

The simulator was developed to support:

- Autonomous offshore blade inspection concepts
- Systems engineering trade studies
- Mission planning analysis
- Energy-aware autonomous operations
- Blade-relative navigation concepts
- Quantitative inspection assessment
- Engineering requirements traceability
- Concept architecture development
- Research and education

---

# Features

## Mission Planning

The simulator generates autonomous blade-by-blade inspection missions consisting of:

- Takeoff
- Transit
- Blade transitions
- Dual-pass blade inspection
- Hub-clearance maneuvers
- Egress
- Return-to-launch
- Landing

Mission trajectories are visualized in an interactive three-dimensional environment.

---

## UAS Platform Model

The simulated multirotor platform includes configurable:

- Aircraft mass
- Rotor configuration
- Propeller diameter
- Rotor figure of merit
- Motor and ESC efficiency
- Aerodynamic drag
- Maximum continuous power
- Battery capacity
- Cruise speed
- Inspection speed
- Stand-off distance

---

## Sensor Architecture

The proposed inspection architecture incorporates:

- High-resolution RGB camera
- LiDAR
- Inertial Measurement Unit (IMU)

User-adjustable parameters include:

- Camera field of view
- Frame rate
- Optical tracking quality
- LiDAR range
- LiDAR update rate
- LiDAR noise
- IMU quality
- Sensor synchronization error

---

## Blade-Relative Navigation

The simulator investigates concept-level blade-relative navigation under multiple positioning conditions:

- RTK Fixed
- RTK Float
- Standard GNSS
- Multipath / degraded GNSS
- GNSS-denied alternate navigation

Rather than implementing a complete navigation stack, the simulator models relative navigation uncertainty using simplified sensor-fusion assumptions.

---

## Propulsion and Energy Modeling

Mission feasibility is evaluated using a simplified propulsion model that estimates:

- Rotor-induced power
- Profile power
- Parasitic drag
- Hotel loads
- Battery energy consumption
- Dynamic return energy
- Reserve battery requirements

The simulator continuously evaluates remaining energy throughout the mission.

If insufficient energy remains to safely complete the mission and return to the launch location, the inspection is automatically terminated.

---

## Environmental Modeling

Mission performance is influenced by user-defined offshore conditions including:

- Mean wind speed
- Gusts
- Turbulence intensity
- Wave height
- Visibility
- Precipitation

Environmental conditions affect:

- Power consumption
- Navigation uncertainty
- Inspection quality
- Mission feasibility

---

## Inspection Performance Metrics

Inspection effectiveness is evaluated using quantitative engineering metrics including:

- Geometric blade-surface coverage
- Image overlap
- Blade stand-off distance
- Relative navigation error
- LiDAR quality index
- Rotor-proximity hazard index
- Inspection Data Suitability Index

These metrics support engineering comparison of alternative mission configurations and operating conditions.

---

## Systems Engineering Integration

The simulator incorporates systems engineering principles through quantitative evaluation of mission requirements.

Illustrative requirement categories include:

| Requirement Area | Example Evaluation |
|------------------|-------------------|
| Navigation | Blade-relative position accuracy |
| Inspection | Blade-surface coverage |
| Energy | Battery reserve compliance |
| Operations | Mission feasibility |
| Safety | Rotor-proximity hazard assessment |

The application supports concept-level requirements traceability by linking operational needs with measurable engineering outputs.

---

# Mission Outputs

Each simulation produces:

- Interactive 3D mission visualization
- Mission telemetry
- Blade coverage heatmap
- Energy profile
- Hazard assessment
- Systems engineering metrics
- Mission report
- CSV telemetry export
- JSON export
- Markdown report export

---

# Technology Stack

- Python
- Streamlit
- NumPy
- Pandas
- Plotly

---

# Repository Structure

```
offshore-autonomous-inspection-platform/
│
├── app.py
├── README.md
├── requirements.txt
├── LICENSE
│
├── images/
│   ├── banner.png
│   ├── mission_view.png
│   ├── telemetry.png
│   ├── coverage.png
│   └── architecture.png
│
├── docs/
│   └── User_Guide.pdf
│
└── examples/
    ├── sample_report.md
    ├── sample_telemetry.csv
    └── sample_simulation.json
```

---

# Installation

Clone the repository.

```bash
git clone https://github.com/tareqomrani/offshore-autonomous-inspection-platform.git
```

Navigate to the project directory.

```bash
cd offshore-autonomous-inspection-platform
```

Install dependencies.

```bash
pip install -r requirements.txt
```

Launch the simulator.

```bash
streamlit run app.py
```

---

# Example Workflow

1. Configure the offshore wind turbine.
2. Define environmental conditions.
3. Configure the multirotor UAS.
4. Configure sensor parameters.
5. Define economic assumptions.
6. Run the autonomous inspection mission.
7. Review mission telemetry.
8. Analyze inspection performance metrics.
9. Export engineering reports.

---

# Current Limitations

This simulator is intended for concept-level engineering analysis.

The current implementation does **not** model:

- Full six-degree-of-freedom flight dynamics
- Rotor wake interactions
- Rotor-blade aerodynamics
- Time-dependent rotating blade tracking
- Collision probability
- Real-time obstacle avoidance
- Visual SLAM
- Extended Kalman filtering
- Flight controller dynamics
- Hardware-in-the-loop testing
- Validated computer vision
- Automated defect recognition
- Certified operational performance

Simulation outputs should therefore be interpreted as engineering trade-study results rather than operational performance predictions.

---

# Future Development

Potential future enhancements include:

- Physics-based six-degree-of-freedom flight dynamics
- Extended Kalman Filter navigation
- Visual-Inertial Odometry (VIO)
- Visual SLAM
- Real-time obstacle avoidance
- Wind-field modeling
- Rotor wake interaction modeling
- Automated defect detection
- Digital twin integration
- Multi-UAS cooperative inspections
- Mission optimization
- Predictive maintenance analytics
- Hardware-in-the-loop validation

---

# References

Acosta, C., Centanaro, B., Tapia, M., & Benavides, F. (2025). *Wind turbine inspection: An autonomous UAV-based approach.*

Carroll, J., McDonald, A., Dinwoodie, I., McMillan, D., Revie, M., & Lazakis, I. (2017). *Availability, operation and maintenance costs of offshore wind turbines with different drive train configurations.*

Castelar Wembers, C., et al. (2024). *LiDAR-based automated UAV inspection of wind turbine rotor blades.*

Heo, S.-J., & Na, W. S. (2025). *Review of drone-based technologies for wind turbine blade inspection.*

Oliveira, A., et al. (2024). *LiDAR-based unmanned aerial vehicle offshore wind blade inspection and modeling.*

Shafiee, M., Zhou, Z., Mei, L., Dinmohammadi, F., Karama, J., & Flynn, D. (2021). *Unmanned aerial drones for inspection of offshore wind turbines: A mission-critical failure analysis.*

Zhang, K., Pakrashi, V., Murphy, J., & Hao, G. (2024). *Inspection of floating offshore wind turbines using multi-rotor unmanned aerial vehicles: Literature review and trends.*

---

# Disclaimer

The **Offshore Autonomous Blade Inspection Mission Simulator V2** is an academic and research-oriented engineering prototype.

It is intended exclusively for:

- Systems engineering research
- Concept development
- Architecture evaluation
- Engineering trade studies
- Education

This software has **not** been validated for operational flight planning, aircraft certification, aviation safety, structural inspection, collision avoidance, or automated defect detection.

Results generated by the simulator are intended solely to support concept-level engineering analysis and should not be interpreted as operational performance predictions.

---

# Author

**Tareq Omrani**

AI Engineering • Autonomous Systems • UAS • Systems Engineering

GitHub: https://github.com/tareqomrani

LinkedIn: https://www.linkedin.com/in/tareqomrani

---

*Version 2.0.0*
*Concept-Level Offshore Autonomous Blade Inspection Mission Simulator*
