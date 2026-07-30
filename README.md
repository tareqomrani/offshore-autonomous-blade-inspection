<p align="center">
  <img src="images/banner.png" alt="Offshore Autonomous Blade Inspection Mission Simulator V2" width="100%">
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

</p>

---

# Overview

The **Offshore Autonomous Blade Inspection Mission Simulator V2** is a concept-level systems engineering platform that investigates autonomous multirotor uncrewed aircraft system (UAS) operations for offshore wind turbine blade inspection.

The simulator integrates mission planning, blade-relative navigation, propulsion and energy modeling, environmental effects, geometric blade-surface coverage, inspection performance metrics, and systems engineering requirements into a unified engineering workflow. Rather than serving as a flight simulator, the application supports architecture evaluation, engineering trade studies, concept development, and quantitative analysis of autonomous offshore inspection operations.

The simulator demonstrates how mission planning, sensing, navigation, and energy management can be integrated into a single inspection architecture while providing measurable outputs that support systems engineering decision-making.

> **Research Prototype**
>
> This application is intended exclusively for concept development and engineering analysis.
>
> It is **not** a validated flight-dynamics simulator, operational safety tool, digital twin, collision avoidance system, structural health monitoring system, or automated defect-detection application.

---

# Motivation

Offshore wind turbines require routine inspections to identify leading-edge erosion, coating degradation, cracks, lightning damage, and other structural defects before they affect energy production and maintenance costs.

Traditional inspection approaches frequently require rope-access technicians, cranes, or crewed aircraft, increasing operational costs, safety risks, and turbine downtime.

Autonomous multirotor UAS platforms offer the potential to improve inspection efficiency while reducing personnel exposure to hazardous offshore environments. This simulator investigates a proposed inspection architecture capable of supporting concept-level engineering analysis before physical implementation.

---

# Objectives

The simulator was developed to support:

- Autonomous offshore wind turbine blade inspection concepts
- Systems engineering trade studies
- Mission planning and feasibility analysis
- Blade-relative navigation concepts
- Energy-aware autonomous operations
- Quantitative inspection assessment
- Engineering requirements traceability
- Concept architecture evaluation
- Research and education

---

# Features

## Mission Planning

The simulator generates autonomous blade-by-blade inspection missions consisting of:

- Takeoff
- Transit
- Blade transitions
- Dual-pass blade inspections
- Hub-clearance maneuvers
- Egress
- Return-to-launch
- Landing

Mission trajectories are visualized within an interactive three-dimensional environment.

---

## UAS Platform Model

The multirotor platform is configurable through:

- Aircraft mass
- Rotor count
- Propeller diameter
- Rotor figure of merit
- Motor and ESC efficiency
- Aerodynamic drag
- Maximum continuous power
- Battery capacity
- Cruise speed
- Inspection speed
- Desired blade stand-off distance

---

## Sensor Architecture

The proposed inspection architecture incorporates:

- High-resolution RGB camera
- LiDAR
- Inertial Measurement Unit (IMU)

Configurable sensor parameters include:

- Camera field of view
- Camera frame rate
- Optical tracking quality
- LiDAR range
- LiDAR update rate
- LiDAR range noise
- IMU quality
- Sensor synchronization error

---

## Blade-Relative Navigation

The simulator evaluates concept-level blade-relative navigation under multiple operating conditions:

- RTK Fixed
- RTK Float
- Standard GNSS
- Multipath / Degraded GNSS
- GNSS-Denied Alternate Navigation

Rather than implementing a complete navigation solution, the simulator models relative navigation uncertainty using simplified sensor-fusion assumptions to support engineering trade studies.

---

## Propulsion and Energy Modeling

Mission feasibility is evaluated using a simplified propulsion model that estimates:

- Rotor-induced power
- Profile power
- Parasitic drag
- Hotel loads
- Battery energy consumption
- Predicted return energy
- Dynamic energy margin
- Battery reserve compliance

The simulator continuously evaluates remaining energy throughout each mission.

If insufficient energy remains to safely complete the inspection and return to the launch point, the mission is automatically terminated before reserve limits are exceeded.

---

## Environmental Modeling

Mission performance is influenced by configurable offshore environmental conditions including:

- Mean wind speed
- Peak gusts
- Turbulence intensity
- Wave height
- Visibility
- Precipitation

Environmental conditions influence:

- Power consumption
- Navigation uncertainty
- Inspection quality
- Mission feasibility

---

## Inspection Performance Metrics

Inspection effectiveness is evaluated using quantitative engineering metrics including:

- Geometric blade-surface coverage
- Image overlap
- Blade-relative stand-off distance
- Relative navigation error
- LiDAR quality index
- Rotor-proximity hazard index
- Inspection Data Suitability Index

These metrics support comparison of alternative mission configurations and operating conditions during concept development.

---

## Systems Engineering Integration

The simulator incorporates systems engineering principles by linking operational needs with measurable engineering outputs.

Illustrative requirement categories include:

| Requirement Area | Example Evaluation |
|------------------|--------------------|
| Navigation | Blade-relative position accuracy |
| Inspection | Geometric blade-surface coverage |
| Energy | Battery reserve compliance |
| Mission | Operational feasibility |
| Safety | Rotor-proximity hazard assessment |

This traceability supports concept-level requirements verification and early-stage engineering analysis.

---

# Mission Outputs

Each simulation produces:

- Interactive 3D mission visualization
- Mission telemetry
- Blade coverage heatmap
- Battery and energy profile
- Rotor-proximity hazard assessment
- Inspection performance metrics
- Systems engineering outputs
- Markdown mission report
- CSV telemetry export
- JSON simulation export

---

# Technology Stack

- Python
- Streamlit
- NumPy
- Pandas
- Plotly

---

# Repository Structure

```text
offshore-autonomous-inspection-platform/
│
├── app.py
├── README.md
├── requirements.txt
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

Install the required packages.

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
4. Configure onboard sensor parameters.
5. Define economic assumptions.
6. Run the autonomous inspection mission.
7. Review mission telemetry.
8. Evaluate inspection performance.
9. Export engineering reports and simulation data.

---

# Current Limitations

The Offshore Autonomous Blade Inspection Mission Simulator V2 is intended for concept-level systems engineering analysis.

The current implementation does **not** include:

- Six-degree-of-freedom flight dynamics
- Rotor wake interaction modeling
- Time-dependent rotating blade tracking
- Flight controller simulation
- Collision probability estimation
- Real-time obstacle avoidance
- Visual SLAM
- Extended Kalman Filter navigation
- Visual-inertial odometry
- Hardware-in-the-loop testing
- Validated computer vision
- Automated defect recognition
- Flight-certified operational performance

Simulation outputs should therefore be interpreted as engineering trade-study results rather than operational performance predictions.

---

# Future Development

Potential future enhancements include:

- Six-degree-of-freedom flight dynamics
- Wind-field and rotor-wake modeling
- Visual-Inertial Odometry (VIO)
- Extended Kalman Filter navigation
- Visual SLAM
- Real-time obstacle avoidance
- Automated defect detection
- Predictive maintenance analytics
- Multi-UAS cooperative inspection
- Digital twin integration
- Hardware-in-the-loop validation
- Mission optimization algorithms

---

# References

Acosta, C., Centanaro, B., Tapia, M., & Benavides, F. (2025). *Wind turbine inspection: An autonomous UAV-based approach.*

Carroll, J., McDonald, A., Dinwoodie, I., McMillan, D., Revie, M., & Lazakis, I. (2017). *Availability, operation and maintenance costs of offshore wind turbines with different drive train configurations.*

Castelar Wembers, C., Pflughaupt, J., Moshagen, L., Kurenkov, M., Lewejohann, T., & Schildbach, G. (2024). *LiDAR-based automated UAV inspection of wind turbine rotor blades.*

Heo, S.-J., & Na, W. S. (2025). *Review of drone-based technologies for wind turbine blade inspection.*

Oliveira, A., Dias, A., Santos, T., Rodrigues, P., Martins, A., & Almeida, J. (2024). *LiDAR-based unmanned aerial vehicle offshore wind blade inspection and modeling.*

Shafiee, M., Zhou, Z., Mei, L., Dinmohammadi, F., Karama, J., & Flynn, D. (2021). *Unmanned aerial drones for inspection of offshore wind turbines: A mission-critical failure analysis.*

Zhang, K., Pakrashi, V., Murphy, J., & Hao, G. (2024). *Inspection of floating offshore wind turbines using multi-rotor unmanned aerial vehicles: Literature review and trends.*

---

# Disclaimer

The **Offshore Autonomous Blade Inspection Mission Simulator V2** is a concept-level engineering and research application.

The simulator is intended to support:

- Systems engineering investigations
- Concept development
- Engineering trade studies
- Mission architecture evaluation
- Research and education

The software has **not** been validated for operational flight planning, aircraft certification, aviation safety, structural inspection, collision avoidance, or automated defect detection.

Simulation outputs are intended solely to support engineering analysis and should not be interpreted as validated operational performance predictions.

---

# Author

**Tareq Omrani**

AI Engineering • Autonomous Systems • UAS • Systems Engineering

**GitHub:** https://github.com/tareqomrani

**LinkedIn:** https://www.linkedin.com/in/tareqomrani

---

<p align="center">
<b>Version 2.0.0</b><br>
Concept-Level Offshore Autonomous Blade Inspection Mission Simulator
</p>
