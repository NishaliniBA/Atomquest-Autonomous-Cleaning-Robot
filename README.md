# ESP32-Based Autonomous Cleaning Robot
### AtomQuest 2025 – Top 10 Finalist Across India

## 📌 Overview

Floorbie is a prototype autonomous cleaning robot developed for **AtomQuest 2025**, conducted by **Atomberg Technologies**.

The project demonstrates the design and implementation of an embedded autonomous mobile robot using an **ESP32 microcontroller**. The robot navigates autonomously by detecting obstacles through distance sensors and controls its movement using a differential drive mechanism.

The primary objective of this project was to develop a reliable embedded control system capable of autonomous navigation while serving as a foundation for future AI-based cleaning systems.

---

## 🚀 Features

- ESP32-based embedded controller
- Autonomous obstacle avoidance
- Differential drive motor control
- Sensor-based navigation
- Embedded C / Arduino programming
- Prototype autonomous mobile robot

---

## 🛠 Hardware Components

| Component | Purpose |
|-----------|---------|
| ESP32 | Main Controller |
| Ultrasonic Sensor | Obstacle Detection |
| Motor Driver | DC Motor Control |
| DC Geared Motors | Robot Movement |
| Robot Chassis | Mechanical Platform |
| Battery Pack | Power Supply |

> Update this table if your actual hardware differs.

---

## 💻 Software Used

- Arduino IDE
- Embedded C
- ESP32 Framework

---

## ⚙️ Working Principle

1. ESP32 continuously reads data from the distance sensor.
2. If no obstacle is detected, the robot moves forward.
3. If an obstacle is detected within a predefined threshold:
   - Stop
   - Turn left or right
   - Continue moving forward
4. The process repeats continuously for autonomous navigation.

---

## 📂 Repository Structure

```
Floorbie/

│── README.md
│── LICENSE
│── .gitignore
│
├── esp32_code/
├── hardware/
├── images/
├── videos/
└── docs/
```

---

## 📷 Project Images

Images of the robot, hardware setup, wiring, and testing are available inside the **images/** folder.

---

## 🎥 Demonstration

A demonstration video is available in the **videos/** directory.

---

## ⚡ Challenges

- Motor speed calibration
- Sensor accuracy
- Stable power distribution
- Obstacle detection tuning
- Mechanical alignment of the robot chassis

---

## 🔮 Future Enhancements

The following features were planned as future improvements but were **not implemented** in the current prototype:

- Raspberry Pi integration
- Camera-based object detection
- YOLOv8 waste classification
- ROS2 middleware
- LiDAR-based SLAM
- Autonomous path planning
- Intelligent cleaning decisions
- Automatic charging dock

---

## 🏆 Achievement

This project was developed as part of **AtomQuest 2025** conducted by **Atomberg Technologies**, where it was selected among the **Top 10 Finalists across India**.

---

## 📜 License

This project is released under the MIT License.

---

## 👤 Author

**Nishalini B.A.**

GitHub: https://github.com/NishaliniBA
