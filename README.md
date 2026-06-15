# Astra UAV Project

## Overview

Astra is a modular UAV development project focused on building autonomous navigation capabilities using Artificial Intelligence, Machine Learning, path planning algorithms, simulation, and hardware integration.

Instead of attempting to build a complete autonomous UAV immediately, the project follows a modular engineering approach.

Each subsystem will be developed independently, tested, and later integrated into a complete UAV system.

The first major objective is to develop a **GPS-denied autonomous navigation system**.

---

# Project Objective

The goal of Astra is to develop a UAV capable of navigating through an environment without depending on GPS signals.

The system will:

1. Collect satellite images of the same geographical region across multiple days.
2. Analyse terrain and environmental changes over time.
3. Generate a stability/risk map of the environment.
4. Generate the safest possible route instead of only the shortest route.
5. Convert the route into UAV waypoints.
6. Simulate autonomous movement.
7. Integrate the navigation system with the physical UAV.

The system will always maintain:

- Manual control mode
- Autonomous navigation mode
- Emergency manual override

---

# System Architecture

```
Satellite Images
        |
        v
Dataset Collection & Processing
        |
        v
Machine Learning Pipeline
        |
        v
Terrain Classification + Change Detection
        |
        v
Risk / Stability Map Generation
        |
        v
Path Planning Algorithm
        |
        v
Waypoint Generation
        |
        v
Drone Simulation
        |
        v
Hardware Integration
```

---

# Project Modules

## 1. Machine Learning Module

The ML system is responsible for understanding the environment.

Responsibilities:

- Satellite image preprocessing
- Terrain classification
- Change detection between multiple days
- Feature extraction
- Risk map generation
- Model training and evaluation

Expected areas of work:

- CNN-based models
- Computer Vision
- Image processing
- Deep Learning pipelines

Possible technologies:

- Python
- PyTorch / TensorFlow
- OpenCV
- NumPy
- Scikit-learn

Folder:

```
software/ml/
```

---

# 2. Dataset Module

The dataset team handles all data requirements.

Responsibilities:

- Collect satellite imagery
- Organize datasets
- Clean and preprocess data
- Define dataset formats
- Prepare training and testing data
- Maintain dataset documentation

Important:

Large datasets should NOT be directly uploaded to GitHub.

The repository should contain:

- Dataset structure
- Metadata
- Processing scripts
- Download instructions

Folder:

```
datasets/
```

---

# 3. Path Planning Module

The path planning team converts environmental information into navigation routes.

Responsibilities:

- Route generation algorithms
- Cost function design
- Safe path calculation
- Waypoint generation
- Navigation logic
- Algorithm testing

The planner should consider:

- Terrain risk
- Environmental changes
- Distance
- Flight constraints

Folder:

```
software/path-planning/
```

---

# 4. Simulation Module

The simulation team creates the virtual testing environment.

Responsibilities:

- Drone movement simulation
- Waypoint following
- Position estimation
- Navigation testing
- Algorithm validation

Folder:

```
software/simulation/
```

---

# 5. Hardware Module

The hardware team focuses on UAV construction and integration.

Responsibilities:

- Drone frame selection
- Motor selection
- ESC configuration
- Flight controller setup
- Battery selection
- Sensor integration
- Telemetry collection
- Manual/autonomous mode switching

Required systems:

- Flight controller
- IMU sensors
- GPS (for testing/reference)
- Communication systems
- Remote control system

Folder:

```
hardware/
```

---

# Development Workflow

Astra follows a controlled GitHub development workflow.

## Main Rules

- No direct commits to the main branch.
- No direct pushes to the main branch.
- Every task must be developed in a separate branch.
- Every change must go through a Pull Request.
- Every Pull Request requires approval before merging.

---

# Git Workflow

```
GitHub Issue Created
          |
          v
Task Assigned
          |
          v
Create Feature Branch
          |
          v
Development Work
          |
          v
Commit Changes
          |
          v
Push Branch
          |
          v
Create Pull Request
          |
          v
Code Review
          |
          v
Approval
          |
          v
Merge into main
```

---

# Branch Naming Convention

All branches must follow:

```
name/feature-name
```

Examples:

```
shreyas/terrain-classifier

rahul/path-planning

alex/drone-setup

member/dataset-cleaning
```

---

# Pull Request Policy

Every PR must:

- Have at least one approved review before merging.
- Not be merged by the author.
- Be linked to a GitHub Issue where applicable.
- Contain a proper description.
- Clearly explain changes made.

PRs that do not follow the required format will be returned for revision.

---

# Commit Guidelines

Commits should be small and meaningful.

Examples:

```
feat: add terrain preprocessing pipeline

fix: correct waypoint calculation

docs: update architecture documentation

chore: update dependencies
```

Avoid:

```
final code
updated stuff
changes
new version
```

---

# Current Development Phase

## Phase 1: Research and Foundation

The project is currently starting development.

Before implementation, teams must prepare:

## Software Team

Research:

- ML models suitable for terrain analysis
- Computer vision approaches
- Satellite datasets
- Data processing methods
- Path planning algorithms
- Technology stack decisions

Expected outcome:

A clear technical approach for implementation.

---

## Hardware Team

Research:

- UAV frame requirements
- Motors
- ESC
- Flight controller
- Battery
- Sensors
- Communication systems

Also determine:

- How drone telemetry will be collected
- How heading, speed, and time data will be obtained
- How manual and autonomous modes will switch

Expected outcome:

A complete hardware architecture plan.

---

# Repository Structure

```
astra-uav/

├── README.md

├── docs/
│   ├── architecture.md
│   └── meeting-notes/

├── software/
│   ├── ml/
│   ├── path-planning/
│   └── simulation/

├── hardware/

└── datasets/
```

---

# Project Meeting

Technical meeting:

Date:
Friday, 8th May

Time:
1:25 PM

Agenda:

- Review project idea
- Discuss implementation approaches
- Finalize technical decisions
- Begin development planning

---

# Project Status

Current status:

```
Planning Phase
      |
      v
Repository Setup
      |
      v
Research Phase
      |
      v
Implementation Phase
```

Astra is currently in the initial development stage.

All members are expected to understand their assigned module and contribute through the defined GitHub workflow.

