# Project Overview

# AtomQuest Autonomous Cleaning Robot

## Competition Background

The **AtomQuest Autonomous Cleaning Robot** was developed as part of **AtomQuest 2025**, a national-level robotics competition organized by **Atomberg Technologies**. The competition encouraged engineering students to design innovative robotic systems capable of addressing practical real-world challenges using embedded systems, autonomous control, and intelligent decision-making.

The project was successfully shortlisted among the **Top 10 Finalists across India**, demonstrating the team's ability to design and implement a functional autonomous robotic prototype within the given development timeline.

Unlike conventional academic projects that primarily focus on simulation or theoretical concepts, this project involved the complete development of a working robotic prototype, including hardware integration, embedded software development, mechanical assembly, sensor interfacing, motor control, system testing, and iterative performance improvements.

---

# Introduction

Automation has significantly transformed modern industries by replacing repetitive manual operations with intelligent and autonomous systems. Mobile robots are increasingly being deployed in warehouses, hospitals, airports, educational institutions, shopping malls, office buildings, and manufacturing facilities to perform repetitive tasks efficiently while reducing human intervention.

Cleaning is one such repetitive operation that requires continuous effort and consumes considerable time and manpower. Although commercial robotic vacuum cleaners are available, they are often expensive, proprietary, and difficult to customize for research or educational purposes.

The motivation behind this project was to develop a low-cost autonomous robotic platform capable of independently navigating an indoor environment while detecting and avoiding obstacles using embedded hardware. The developed platform also serves as a modular foundation for integrating advanced perception systems such as computer vision, LiDAR, simultaneous localization and mapping (SLAM), and intelligent navigation in future versions.

The primary focus of the implemented prototype was to design a reliable embedded control system capable of autonomous movement using an ESP32 microcontroller and distance sensors.

---

# Motivation

Developing autonomous robots requires the integration of multiple engineering disciplines, including embedded systems, electronics, control systems, mechanical design, and software development.

Instead of developing an isolated software application or a standalone hardware circuit, this project aimed to integrate multiple hardware components into a complete embedded robotic system capable of making real-time navigation decisions.

The project provided practical exposure to:

- Embedded programming
- Hardware-software integration
- Sensor interfacing
- Motor control
- Autonomous decision making
- Robotic system design
- Prototype development
- System testing and debugging

The experience gained during this project closely resembles real-world embedded system development where hardware and software must work together reliably under real-time constraints.

---

# Problem Statement

Indoor cleaning is predominantly performed either manually or using commercially available robotic cleaners. While commercial robotic cleaners offer automation, they generally function as closed systems with limited customization capabilities and are often expensive for educational and research applications.

The objective of this project was to design and develop an autonomous mobile robot capable of navigating indoor environments without continuous human intervention.

The robot should be capable of:

- Detecting obstacles in its surroundings
- Making navigation decisions in real time
- Avoiding collisions autonomously
- Controlling its motors using an embedded controller
- Operating continuously using onboard power

The developed system should also provide a scalable hardware architecture that allows future integration of advanced robotic technologies without requiring complete redesign of the platform.

---

# Project Objectives

The major objectives established before the development phase were:

### Primary Objectives

- Design an embedded autonomous mobile robot.
- Implement reliable obstacle detection.
- Develop autonomous obstacle avoidance logic.
- Interface sensors with the ESP32.
- Control differential drive motors.
- Demonstrate autonomous indoor navigation.

### Secondary Objectives

- Design a modular hardware architecture.
- Improve system reliability.
- Optimize navigation behaviour.
- Prepare the platform for future AI integration.

---

# Proposed Solution

The proposed solution involves designing an embedded autonomous robot using an ESP32 development board as the primary controller responsible for processing sensor information and controlling robot movement.

Distance sensors continuously monitor the environment in front of the robot. Sensor readings are periodically acquired by the ESP32 and compared against a predefined safety threshold.

Whenever the measured distance exceeds the threshold, the controller commands the motors to move forward. If an obstacle is detected within the threshold distance, the controller immediately stops the robot, executes an avoidance maneuver by changing its direction, and resumes forward motion after a safe path is identified.

This decision-making process continues continuously during operation, enabling autonomous navigation without external supervision.

The modular system architecture allows additional sensors and processing units to be incorporated in future versions without major modifications to the embedded control logic.

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/1f9ff192-d591-4def-8b8c-039fe8bcf6a3" />

---


# Scope of the Project

The implemented prototype focuses on:

- Embedded control system development
- Sensor interfacing
- Autonomous navigation
- Obstacle avoidance
- Motor control
- Prototype validation

The project does not currently include:

- Camera-based object detection
- Autonomous cleaning mechanism
- LiDAR-based mapping
- ROS2 middleware
- SLAM algorithms
- Autonomous path planning

These features are considered future enhancements.

---

# Development Methodology

The project was developed using an incremental engineering approach consisting of the following phases:

1. Problem Analysis
2. System Design
3. Hardware Selection
4. Mechanical Assembly
5. Sensor Integration
6. Motor Driver Integration
7. Embedded Software Development
8. Testing
9. Debugging
10. Prototype Validation

Each phase was completed after verifying the successful operation of the previous stage to ensure stable system integration.

---

# Project Outcome

The developed robot successfully demonstrated:

- Autonomous forward movement
- Obstacle detection
- Autonomous obstacle avoidance
- Stable embedded motor control
- Continuous autonomous operation

The prototype validates the feasibility of developing a low-cost embedded autonomous robotic platform suitable for further research and feature expansion.

---

# Team Members

This project was collaboratively developed by:

- **Nishalini B.A.**
- **A Athul Krishna**
- **Suryaprakash TSS**

