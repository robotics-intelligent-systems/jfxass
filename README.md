# jfxai4mass
## AI-Powered Modular Autonomous Mobility & Simulation Systems

> Open-source reference architecture for modeling, simulation, digital twins,
> artificial intelligence and modular autonomous mobility systems.

**jfxai4mass** is an open-source engineering and research compendium for the
development of **Modular Autonomous Mobility and Simulation Systems (MASS)**.

The project brings together Model-Based Systems Engineering (MBSE), Modelica,
digital twins, vehicle simulation, robotics, autonomous driving, artificial
intelligence and modular hardware/software architectures into a common
technology-neutral reference framework.

The objective is not to reproduce a specific commercial vehicle or proprietary
platform. Instead, jfxai4mass studies reusable engineering principles and open
technologies that can support simplified, interoperable and extensible mobility
platforms.

---

## Table of Contents

- [Project Vision](#project-vision)
- [Description and Context](#description-and-context)
- [Objectives](#objectives)
- [Reference Architecture](#reference-architecture)
- [Engineering Domains](#engineering-domains)
- [Digital Twin Architecture](#digital-twin-architecture)
- [AI and Autonomous Systems](#ai-and-autonomous-systems)
- [Modelica and Multiphysics Simulation](#modelica-and-multiphysics-simulation)
- [Open-Source Technology Compendium](#open-source-technology-compendium)
- [Reference Platforms](#reference-platforms)
- [MBSE Engineering Process](#mbse-engineering-process)
- [Modular Mobility Concept](#modular-mobility-concept)
- [OpenTwin Concept](#opentwin-concept)
- [Repository Structure](#repository-structure)
- [User Guide](#user-guide)
- [Installation Guide](#installation-guide)
- [Dependencies](#dependencies)
- [Development Roadmap](#development-roadmap)
- [How to Contribute](#how-to-contribute)
- [Code of Conduct](#code-of-conduct)
- [Authors and Maintainers](#authors-and-maintainers)
- [Intellectual Property and Reference Material](#intellectual-property-and-reference-material)
- [Disclaimer](#disclaimer)
- [License](#license)

---

# Project Vision

jfxai4mass explores a transition from vertically integrated vehicle platforms toward:

**Open Architecture + Modular Hardware + Digital Twins + Modelica + AI + Autonomous Systems**

The long-term goal is to provide reusable engineering knowledge for building
and evaluating autonomous mobility platforms without requiring dependence on
a single proprietary vehicle architecture, simulation environment, AI model,
cloud provider or hardware vendor.

The project follows five principles:

1. **Open architecture**
2. **Modularity**
3. **Interoperability**
4. **Simulation-first engineering**
5. **Technology independence**

---

# Description and Context

Modern mobility systems combine mechanical engineering, electrical and
electronic systems, embedded computing, robotics, control engineering,
artificial intelligence, communications, cloud/edge computing, simulation and
systems engineering.

jfxai4mass provides a structured compendium and reference architecture for
studying these cyber-physical systems using open-source tools and open
engineering standards.

The repository investigates technologies applicable to autonomous ground
vehicles, electric vehicles, modular utility vehicles, delivery systems,
robotic vehicles, emergency and rescue mobility, agricultural vehicles,
research vehicles, aerial mobility, UAV integration, multimodal mobility,
digital vehicle prototypes and software-defined vehicles.

---

# Objectives

## Primary Objective

Develop a reusable open engineering framework for researching, modeling,
simulating and prototyping modular autonomous mobility systems.

## Specific Objectives

- Integrate MBSE with executable simulation.
- Use Modelica for multidomain physical modeling.
- Investigate open-source autonomous-driving stacks.
- Support Software-in-the-Loop simulation.
- Support Hardware-in-the-Loop experimentation.
- Explore digital-twin architectures.
- Integrate AI-based perception and decision systems.
- Investigate modular vehicle hardware.
- Decouple applications from vehicle-specific implementations.
- Promote reproducible mobility research.

---

# Reference Architecture

```text
┌──────────────────────────────────────────────────────┐
│                 APPLICATION LAYER                    │
│ Mobility │ Logistics │ Rescue │ Research │ Utility  │
└──────────────────────────┬───────────────────────────┘
                           │
┌──────────────────────────▼───────────────────────────┐
│                  AI & AUTONOMY                       │
│ Perception │ Planning │ Prediction │ Optimization   │
└──────────────────────────┬───────────────────────────┘
                           │
┌──────────────────────────▼───────────────────────────┐
│                DIGITAL TWIN LAYER                    │
│ State │ Telemetry │ Models │ Simulation │ Analytics │
└──────────────────────────┬───────────────────────────┘
                           │
┌──────────────────────────▼───────────────────────────┐
│               SIMULATION / MODELICA                  │
│ Mechanical │ Electrical │ Thermal │ Fluid │ Control │
└──────────────────────────┬───────────────────────────┘
                           │
┌──────────────────────────▼───────────────────────────┐
│                 VEHICLE SERVICES                     │
│ ROS 2 │ Vehicle APIs │ Middleware │ V2X │ Data Bus  │
└──────────────────────────┬───────────────────────────┘
                           │
┌──────────────────────────▼───────────────────────────┐
│                MODULAR HARDWARE                      │
│ Sensors │ Compute │ Energy │ Drive │ Payload │ UAV  │
└──────────────────────────────────────────────────────┘
```

---

# Engineering Domains

| Domain | Purpose |
|---|---|
| Mechanical | Chassis, suspension, structures and vehicle dynamics |
| Electrical | Power distribution, motors and electronic systems |
| Energy | Battery, hybrid and alternative energy architectures |
| Control | Vehicle control and feedback systems |
| Sensors | Camera, LiDAR, radar, GNSS, IMU and IoT |
| Compute | Edge computing and vehicle computers |
| Communications | Vehicle networks, V2X and telemetry |
| AI | Perception, prediction and intelligent decision support |
| Simulation | Virtual validation and scenario execution |
| Digital Twin | Synchronization between physical and virtual systems |
| Payload | Mission-specific interchangeable modules |

---

# Digital Twin Architecture

```text
PHYSICAL SYSTEM
      │
      ▼
Sensors / Vehicle Network
      │
      ▼
Telemetry & Data Acquisition
      │
      ▼
Open Integration Layer
      │
      ├───────────────┐
      ▼               ▼
Digital Twin      Data Platform
      │               │
      ▼               ▼
Modelica          AI / Analytics
Simulation            │
      │               │
      └───────┬───────┘
              ▼
       Decision Support
              │
              ▼
       Vehicle / Operator
```

Potential interfaces include ROS 2, MQTT, OPC UA, CAN, V2X, REST APIs,
event streaming and co-simulation interfaces.

---

# AI and Autonomous Systems

Potential AI capabilities include perception (object detection, semantic
segmentation, lane/terrain detection and sensor fusion), prediction
(trajectory, energy and predictive maintenance), planning (route, motion,
mission and fleet optimization), and digital-twin intelligence (anomaly
detection, surrogate modeling, simulation acceleration and parameter
estimation).

AI should remain a modular subsystem rather than a mandatory dependency of the
physical architecture.

---

# Modelica and Multiphysics Simulation

Modelica provides a foundation for multidomain physical modeling.

```text
Vehicle
├── Mechanical
│   ├── Chassis
│   ├── Suspension
│   └── Vehicle Dynamics
├── Electrical
│   ├── Motors
│   ├── Power Electronics
│   └── Distribution
├── Energy
│   ├── Battery
│   ├── Hybrid Systems
│   └── Energy Management
├── Thermal
│   ├── Battery Cooling
│   ├── Electronics
│   └── HVAC
└── Control
    ├── Steering
    ├── Braking
    └── Powertrain Control
```

---

# Open-Source Technology Compendium

The following projects and technology families are research references.
Inclusion does **not** imply mandatory dependency or redistribution.

## Autonomous Driving

| Technology | Research Role |
|---|---|
| Autoware | Autonomous driving software stack |
| openpilot | Robotics/autonomous driving reference |
| RoboCar | Lightweight autonomous-driving architecture |
| OSCC | Open vehicle-control research |
| RTK Autosteer | Positioning and autonomous steering |
| AV4EV | Modular autonomous electric-vehicle research |

## Simulation

| Technology | Research Role |
|---|---|
| Gazebo | Robotics and vehicle simulation |
| CARLA | Autonomous-driving simulation |
| DeepDrive | Driving simulation research |
| Gym environments | Reinforcement-learning experiments |
| AutoDRIVE | Integrated autonomous-vehicle simulation |
| soda.sim | Vehicle and robotics simulation |
| Vamos | Real-time 3D automotive simulation |
| CETRAN CoSim | Co-simulation research |

## Robotics and Experimental Platforms

- JPL Open Source Rover
- AutoRally
- VESC vehicle platforms
- Grizzly RUV
- OpenPodcar
- Open Kei Truck

## Modelica and Physical Modeling

The project investigates Modelica vehicle architectures, multidomain motor
models, electric/hybrid powertrain libraries, energy-storage models, OpenIPSL,
Modelica-MVEMLib, internal-combustion engine modeling and multidomain vehicle
interfaces.

## Software-Defined Vehicle Technologies

Research areas include Eclipse Velocitas, containerized vehicle applications,
open ECUs, ECU virtualization, Software-in-the-Loop, Hardware-in-the-Loop and
service-oriented vehicle architectures.

## Engineering Tools

| Layer | Candidate Technologies |
|---|---|
| MBSE | Capella / Arcadia |
| Physical Modeling | Modelica / OpenModelica |
| Robotics | ROS 2 |
| Simulation | Gazebo / CARLA |
| AI | Python ecosystem |
| Computer Vision | OpenCV |
| Containers | Docker |
| Orchestration | Kubernetes |
| Visualization | Grafana |
| Time-Series Data | InfluxDB |
| Vehicle Applications | Eclipse Velocitas |

---

# Reference Platforms

The research catalog covers NATURE, CMOSS, SOSA, DrivAerNet++, soda.sim,
AutoRally, VESC vehicle platforms, AutoDRIVE, JPL Open Source Rover, Gazebo
vehicle environments, modular ambulance research, Open Kei Truck, DeepDrive,
CARLA, openpilot, open ECUs, ECU virtualization, RoboCar, Autoware,
RTK Autosteer, AV4EV, OSCC, OpenPodcar, Eclipse Velocitas, OSCAR, Modelica
vehicle libraries and CETRAN CoSim.

Each reference should be independently evaluated for license, maturity,
maintenance status, interoperability, documentation, hardware/software
requirements and integration suitability.

---

# MBSE Engineering Process

The existing `MBSE` area can evolve into the following lifecycle:

```text
Requirements
     │
     ▼
Operational Analysis
     │
     ▼
System Architecture
     │
     ▼
Logical Architecture
     │
     ▼
Physical Architecture
     │
     ├───────────┬───────────┐
     ▼           ▼           ▼
    CAD         CAM         CAS
     │           │           │
     └───────────┴─────┬─────┘
                       ▼
                 Digital Twin
                       │
                       ▼
                 AI Optimization
```

Arcadia and Capella can provide the systems-engineering methodology and
architecture-modeling environment. CAD supports simplified reusable
vehicle/component geometry, CAM manufacturing-oriented prototype analysis,
and CAS end-to-end, vehicle, multiphysics, autonomy, control, energy and
performance simulation.

---

# Modular Mobility Concept

```text
COMMON PLATFORM
│
├── Drive-by-wire
├── Energy
├── Compute
├── Communications
├── Safety
├── Sensors
└── Vehicle API
        │
        ▼
INTERCHANGEABLE MODULES
│
├── Cargo
├── Passenger
├── Research
├── Rescue
├── Agricultural
├── Logistics
├── Sensor Platform
└── UAV / Robotic Payload
```

---

# OpenTwin Concept

`OpenTwin` is the conceptual digital-twin layer proposed for this repository.
It is not intended to represent a proprietary commercial digital-twin product.

```text
Physical Vehicle
      +
Open Sensors
      +
Edge Computing
      +
Modelica Simulation
      +
AI
      +
Open Data Interfaces
      =
Open Digital Twin
```

The implementation should prioritize standard interfaces and replaceable
components.

---

# Repository Structure

```text
jfxai4mass/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── MBSE/
│   ├── requirements/
│   ├── operational-analysis/
│   ├── logical-architecture/
│   └── physical-architecture/
├── CAD/
│   ├── vehicle/
│   ├── modules/
│   └── payloads/
├── CAM/
│   ├── prototypes/
│   └── manufacturing/
├── CAS/
│   ├── modelica/
│   ├── robotics/
│   ├── vehicle/
│   └── cosimulation/
├── digital-twin/
├── autonomy/
├── ai/
├── interfaces/
├── simulation/
└── docs/
```

---

# User Guide

A typical workflow is:

1. Define the mobility use case.
2. Capture requirements using MBSE.
3. Create the logical system architecture.
4. Select sufficiently abstract hardware modules.
5. Create physical models using Modelica.
6. Select an appropriate robotics or vehicle simulator.
7. Define open interfaces.
8. Execute virtual scenarios.
9. Connect AI components where required.
10. Analyze results and iterate.

---

# Installation Guide

There is no mandatory monolithic installation.

```bash
git clone https://github.com/robotics-intelligent-systems/jfxai4mass.git
cd jfxai4mass
```

Example conceptual environment:

```text
MBSE             -> Capella
Physical Models  -> OpenModelica
Robotics         -> ROS 2
Simulation       -> Gazebo
AI               -> Python
Containers       -> Docker
```

Exact procedures should be maintained inside each module.

---

# Dependencies

The project distinguishes:

- **Required Dependencies** — software strictly required by a module.
- **Optional Integrations** — tools extending functionality.
- **Research References** — projects used for comparison or evaluation.

This prevents the compendium from incorrectly suggesting that every referenced
project forms part of one software distribution.

---

# Development Roadmap

## Phase 1 — Compendium Refactoring
- [x] Identify open mobility technologies.
- [x] Organize MBSE/CAD/CAM/CAS concepts.
- [x] Establish intellectual-property disclaimer.
- [ ] Normalize technology catalog.
- [ ] Record licenses for external projects.
- [ ] Separate dependencies from references.

## Phase 2 — Reference Architecture
- [ ] Define MASS logical architecture.
- [ ] Define OpenTwin architecture.
- [ ] Define vehicle abstraction layer.
- [ ] Define modular payload interface.
- [ ] Define simulation interfaces.

## Phase 3 — Simulation MVP
- [ ] Create simplified vehicle model.
- [ ] Implement Modelica physical subsystem.
- [ ] Connect ROS 2.
- [ ] Integrate an open simulator.
- [ ] Implement telemetry pipeline.
- [ ] Create digital-twin dashboard.

## Phase 4 — AI Integration
- [ ] Perception experiments.
- [ ] Predictive maintenance.
- [ ] Energy optimization.
- [ ] Simulation surrogate models.
- [ ] Autonomous planning experiments.

## Phase 5 — Modular Mobility
- [ ] Ground mobility module.
- [ ] Cargo module.
- [ ] Rescue module.
- [ ] UAV integration.
- [ ] Multimodal simulation scenarios.

---

# How to Contribute

Contributions are welcome in Modelica, autonomous systems, robotics, MBSE,
digital twins, open vehicle interfaces, AI, simulation, documentation, open
hardware and interoperability testing.

```bash
git checkout -b feature/my-contribution
git add .
git commit -m "Add: description of contribution"
git push origin feature/my-contribution
```

Pull requests should describe the problem, solution, dependencies, licenses and
validation/simulation results. Do not submit proprietary models, confidential
information or assets without redistribution rights.

---

# Code of Conduct

Contributors are expected to maintain a professional, inclusive and
collaborative environment. A dedicated `CODE_OF_CONDUCT.md` should be
maintained at repository root.

---

# Authors and Maintainers

Maintained by the **Robotics Intelligent Systems** open-source initiative.

Project repository: `robotics-intelligent-systems/jfxai4mass`

Original authorship of third-party projects remains with their respective
developers and organizations.

---

# Intellectual Property and Reference Material

This repository is intended to develop **original, sufficiently simplified and
abstract engineering models**.

Photographs, renders, vehicle concepts, diagrams or multimedia resources used
during early research phases may serve exclusively as conceptual references.
Their inclusion must not be interpreted as ownership of a referenced design,
authorization to manufacture it, transfer of intellectual-property rights or
endorsement by its original designer/manufacturer.

Where a reference asset cannot legally be redistributed, it should be replaced
by an original abstract representation before publication or distribution.

---

# Disclaimer

jfxai4mass is a research, educational and experimental project. It is **not a
certified automotive, aviation, medical, emergency-response or safety-critical
system**.

Simulation results are not sufficient evidence for operating a real autonomous
vehicle. Real-world deployment requires independent engineering validation,
verification, safety analysis and compliance with applicable regulations and
standards.

The project uses the BID repository template only as a documentation-structure
reference. This repository does not claim BID funding, endorsement, catalog
membership or institutional affiliation.

---

# License

The applicable project license should be maintained in the repository root:

```text
LICENSE
```

Third-party projects, libraries, models and datasets retain their respective
licenses. Before incorporating external components into a distributable build,
verify software-license compatibility, model/data licensing, attribution,
trademark restrictions, patent considerations and redistribution permissions.

---

# Open Engineering Principles

**Open Standards · Open Interfaces · Open Models · Modular Architecture ·
Reproducible Simulation · Interoperability · Sustainable Engineering**

> Build models before machines.  
> Simulate before deployment.  
> Design interfaces before dependencies.  
> Keep the architecture replaceable.
