# 🤖 AtomQuest Autonomous Cleaning Robot

> **ESP32-Based Autonomous Mobile Robot**  
> **Top 10 Finalist Across India | AtomQuest 2025 – Atomberg Technologies**

---

## 📖 Overview

The **AtomQuest Autonomous Cleaning Robot** is an embedded systems project developed for **AtomQuest 2025**, a national robotics competition conducted by **Atomberg Technologies**.

The project focuses on designing and developing an autonomous mobile robot capable of navigating indoor environments using an **ESP32 microcontroller** and distance sensors for real-time obstacle detection and avoidance.

The robot demonstrates autonomous navigation, differential drive motor control, and embedded system integration, providing a foundation for future AI-powered cleaning robots.

---

## ✨ Features

- ESP32-based embedded control system
- Autonomous obstacle avoidance
- Differential drive motor control
- Sensor-based navigation
- Real-time decision making
- Modular hardware architecture
- Embedded C / Arduino implementation

---

## 🛠 Hardware Components

| Component | Purpose |
|-----------|---------|
| ESP32 | Main Controller |
| Ultrasonic Sensor | Obstacle Detection |
| Motor Driver | Motor Control |
| DC Geared Motors | Robot Locomotion |
| Robot Chassis | Mechanical Platform |
| Battery Pack | Power Supply |

---

## 💻 Software Stack

- Arduino IDE
- Embedded C
- ESP32 Arduino Framework

---

## ⚙️ System Workflow

```
Power ON
     │
     ▼
Read Sensor Data
     │
     ▼
Obstacle Detected?
     │
 ┌───┴────┐
 │        │
No       Yes
 │        │
 ▼        ▼
Move    Stop
Forward   │
          ▼
    Change Direction
          │
          ▼
 Continue Navigation
```

---

## 📁 Repository Structure

```
atomquest-autonomous-cleaning-robot/

│── README.md
│── LICENSE
│── .gitignore
│
├── esp32_code/
│
├── hardware/
│
├── images/
│
├── videos/
│
└── docs/
```

---

## 📷 Project Images

The **images/** directory contains:

- Robot Prototype
- Hardware Setup
- ESP32 Controller
- Wiring Connections
- Testing Images

---

## 🎥 Demonstration

A demonstration video of the robot is available in the **videos/** directory.

---

## 🚧 Challenges Faced

- Sensor calibration
- Motor synchronization
- Stable power management
- Reliable obstacle detection
- Mechanical alignment of the robot chassis

---

## 🚀 Future Enhancements

The following features were planned as future improvements and are **not part of the current implementation**:

- Raspberry Pi integration
- Camera-based object detection
- YOLOv8-based waste classification
- ROS2 middleware
- LiDAR-based SLAM
- Autonomous path planning
- Intelligent cleaning decisions
- Automatic docking and charging

---

## 🏆 Achievement

- **Top 10 Finalist** across India in **AtomQuest 2025**
- Developed as part of the national robotics competition conducted by **Atomberg Technologies**

---

## 👩‍💻 Authors

This project was collaboratively developed by:

- **Nishalini B.A.**  
  GitHub: https://github.com/NishaliniBA

- **A Athul Krishna**  
  GitHub: https://github.com/Athull567

- **Suryaprakash TSS**  
  GitHub: https://github.com/surya4827h

---

## 🤝 Acknowledgement

This project was developed collaboratively as part of **AtomQuest 2025**. Each team member contributed to the design, development, testing, and integration of the autonomous cleaning robot.

## 📜 License

This project is licensed under the **MIT License**.
