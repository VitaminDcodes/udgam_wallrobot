# 🤖 udgam_wallrobot

<div align="center">

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Version](https://img.shields.io/badge/version-v1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-yellow)
![Event](https://img.shields.io/badge/event-India%20Innovates%202026-orange)
![ROS2](https://img.shields.io/badge/ROS-2-22314E?logo=ros)
![STM32](https://img.shields.io/badge/MCU-STM32F4-03234B)

**Semi-Autonomous High-Rise Wall Painting & Inspection Robot**

*Team Udgam_UrbanSolution — India Innovates 2025-26*

</div>

---

## 📌 Overview

**udgam_wallrobot** is a semi-autonomous robotic system designed to automate exterior painting and inspection of high-rise buildings — eliminating the need for workers to operate at extreme heights.

Traditional high-rise painting exposes workers to severe fall hazards, high labour costs, and inconsistent quality. Our robot solves all of this.

```python
class UdgamWallRobot:
    name    = "HN-WallBot"
    mode    = "semi-autonomous"
    adhesion = VacuumSuction(pressure="negative")
    drive   = ConveyorWheels(torque="high")
    tools   = ["roller_painting", "crack_detection", "thermal_inspection"]

    def operate(self):
        self.ros2.launch()
        self.vslam.localize()
        self.path_planner.coverage_path()
        self.execute_task()
```

---

## 🚨 Problem Statement

| Issue | Impact |
|-------|--------|
| ⚠️ Unsafe high-rise work | High risk of falls & fatalities |
| 🐢 Slow manual painting | High time & operational cost |
| 💸 High labour cost | Dependence on skilled workers |
| 🎨 Inconsistent quality | Human fatigue = uneven finish |

> *"Painter dies after fall from 14th floor of construction site"*
> — Hindustan Times, Sep 2025

---

## ✅ Solution

A wall-climbing robot with:

- **Safe Vertical Mobility** — Climbs 90° vertical walls and inclined surfaces up to 60° with vacuum-based adhesion
- **Multi-Functional Tool Interface** — Interchangeable modules for painting (roller/spray), crack detection, and surface cleaning
- **Remote & Semi-Autonomous Operation** — Wireless ROS 2 control with real-time monitoring
- **Scalable & Cost-Effective** — Adaptable across building types, reduces labour dependency

---

## 🏗️ System Architecture

### Electronics Layers

```
[Power System 48V] → [Sensor Layer] → [Painting Mechanism] → [Safety & Fault Mgmt]
        ↓                  ↓                   ↓                      ↓
[Motion Control]  → [Adhesion System] → [Vision Processing] → [Data Logging]
```

### Software Pipeline (ROS 2)

```
Operator Command → Controller → Motors → Sensor Feedback → GUI Display
                       ↑                        |
                  Path Planner ← Pattern Estimation
```

---

## ⚙️ Technology Stack

### 🔩 Mechanical
| Component | Technology |
|-----------|------------|
| Design & Modeling | SolidWorks, Fusion 360 |
| Simulation | ANSYS (FEA, Fluent) |
| Drive System | Conveyor-Based Wheel Drive |
| Motors | DC Gear Motors (high torque, low RPM) |
| Manufacturing | 3D Printing (FDM), Laser Cutting |
| Adhesion | Vacuum-Based Suction System |

### ⚡ Electronics
| Component | Technology |
|-----------|------------|
| Microcontroller | STM32F4 (FreeRTOS) |
| Communication | CAN Bus, SPI, I²C |
| Motor Drivers | 48V Rated Modules |
| PCB Design | Altium Designer |
| Power Bus | 48V DC → 24V → 5V |
| Data Logging | Onboard fault & sensor logger |

### 💻 Software
| Module | Technology |
|--------|------------|
| Middleware | ROS 2 |
| Localization | VSLAM (Camera + IMU + Encoders) |
| Path Planning | Grid-based wall coverage algorithm |
| Motion Control | PID + Differential Drive |
| GUI | ROS 2 Dashboard |
| Crack Detection | OpenCV visual inspection |
| Embedded IDE | PlatformIO (VS Code) |

---

## 🌟 Key Features / USP

### 1. 🏗️ Automated High-Rise Wall Maintenance
Removes the need for workers to operate at extreme heights — significantly reducing injury and fatality risk.

### 2. 🔍 Intelligent Surface Inspection
Stereo + thermal camera system detects surface cracks, moisture zones, and structural irregularities in real time.

### 3. 💰 Reduces Maintenance Cost
Eliminates scaffolding, large labour teams, and safety equipment overhead — lowering long-term operational expenses.

---

## 📚 References

1. Yang et al. — *Design and analysis of a passive adaptive wall-climbing robot on variable curvature ship facades*
2. Shi et al. — *A 6-DOF humanoid wall-climbing robot with flexible adsorption feet based on negative pressure suction*
3. Zhu et al. — *Review of advancements in wall climbing robot techniques*
4. Yeon Taek OH — *Study of Wall Climbing Robot Structure and Driving Torque Analysis*
5. Wang et al. — *Design of a Modular Wall-Climbing Robot with Multi-Plane Transition and Cleaning Capabilities*
6. Lou et al. — *Current Status and Trends of Wall-Climbing Robots Research*

---

## 📁 Repository Structure

```
udgam_wallrobot/
├── 📄 README.md
├── 📊 presentation/
│   └── HN_WallRobot_GitHub_Theme.pptx
├── 📝 docs/
│   ├── architecture-mechanical.md
│   ├── architecture-electronics.md
│   └── architecture-software.md
├── ⚙️ src/
│   ├── ros2/
│   ├── mechanical/
│   ├── electronics/
│   └── software/
└── 📜 LICENSE
```

---

## 👥 Team

**Team Udgam_UrbanSolution**
GitHub: [@VitaminDcodes](https://github.com/VitaminDcodes)

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<div align="center">
Made with ❤️ for India Innovates 2025
</div>
