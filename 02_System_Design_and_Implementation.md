# System Design & Implementation

This document provides a detailed explanation of the architecture, hardware integration, embedded software design, and implementation methodology of the AtomQuest Autonomous Cleaning Robot.

The project follows a modular embedded systems approach where each hardware component performs a dedicated task while communicating with the ESP32 microcontroller, which acts as the central processing unit of the robot.

---

# System Architecture

The autonomous cleaning robot is designed around a centralized embedded control architecture.

The ESP32 continuously acquires data from the ultrasonic sensor, processes the measured distance, and determines the appropriate movement of the robot.

Based on the sensor readings, the ESP32 generates control signals for the motor driver, which in turn drives the DC motors responsible for robot movement.

The complete control loop executes continuously during operation, enabling autonomous navigation without external intervention.
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/7ebf8b86-3c63-4e33-b0ba-59b2558923be" />


# Hardware Architecture

The hardware architecture consists of five primary modules.
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/822f6ae9-e7aa-4f2a-8b3c-2a89eb4dfb3c" />


## ESP32 Development Board

The ESP32 acts as the central controller of the robot.

Responsibilities include:

- Reading sensor data
- Processing navigation decisions
- Controlling motor movement
- Executing obstacle avoidance logic

The ESP32 was selected because of its high processing capability, multiple GPIO pins, PWM peripherals, low power consumption, and future support for wireless communication.

Insert ESP32 image here.

---

## Ultrasonic Sensor

The ultrasonic sensor continuously measures the distance between the robot and nearby obstacles.

The sensor transmits ultrasonic waves and calculates the distance by measuring the time required for the reflected signal to return.

The measured distance is transmitted to the ESP32 for further processing.

Insert ultrasonic sensor image.

---

## Motor Driver

Since the ESP32 cannot directly drive high-current DC motors, a motor driver module is used.

The motor driver receives low-power control signals from the ESP32 and supplies sufficient current to operate the motors safely.

Its responsibilities include:

- Motor direction control
- Speed control
- Current amplification
- Electrical isolation

Insert motor driver image.

---

## DC Geared Motors

Two DC geared motors are used to provide differential drive locomotion.

The differential drive mechanism enables:

- Forward movement
- Reverse movement
- Left turn
- Right turn

The use of geared motors provides higher torque and smoother low-speed operation, which is essential for stable autonomous navigation.

Insert motor image.

---

## Robot Chassis

The robot chassis serves as the mechanical platform that supports all electronic components.

The design considerations include:

- Weight distribution
- Structural rigidity
- Battery placement
- Sensor positioning
- Ease of maintenance

Insert robot chassis image.

---

# Embedded Software Design

The software is organized into multiple logical stages.

1. Hardware Initialization
2. GPIO Configuration
3. Sensor Reading
4. Distance Calculation
5. Decision Making
6. Motor Control
7. Continuous Navigation

Each stage executes repeatedly within the main program loop.

---

# Working Principle

The robot operates using a closed-loop obstacle avoidance algorithm.

The workflow is as follows:

1. Power is supplied to the ESP32.
2. The ultrasonic sensor measures the distance to nearby objects.
3. The ESP32 compares the measured distance with a predefined threshold.
4. If the path is clear, the robot moves forward.
5. If an obstacle is detected, the robot immediately stops.
6. The ESP32 commands the motors to turn the robot.
7. After changing direction, the robot resumes forward movement.
8. This process repeats continuously.
-
                   ┌────────────────────────────────────────────┐
                   │          Embedded Control Loop             │
                   └────────────────────────────────────────────┘
         Ultrasonic Sensor
              │
              │ Trigger Pulse
              ▼
      Distance Measurement
              │
              │ Echo Pulse Width
              ▼
      ESP32 GPIO Input Capture
              │
              │
              ▼
   Distance Calculation Algorithm
              │
              ▼
      Obstacle Detection Logic
              │
              ▼
     Navigation Decision Module
              │
     ┌────────┴────────┐
     │                 │
     ▼                 ▼
 Move Forward      Obstacle Found
     │                 │
     │                 ▼
     │         Stop Robot
     │                 │
     │                 ▼
     │         Turn Left / Right
     │                 │
     └─────────┬───────┘
               ▼
      PWM Motor Control
               │
               ▼
        L298N Driver
               │
               ▼
     Left Motor / Right Motor
               │
               ▼
      Robot Navigation

---

# Signal Flow

           Obstacle
              ↓
        Ultrasonic Wave
              ↓
         Echo Pulse
              ↓
        GPIO Capture
              ↓
      Distance Computation
              ↓
        Decision Algorithm
              ↓
    Motor Command Generation
              ↓
          PWM Output
              ↓
        Motor Driver
              ↓
        Wheel Rotation
              ↓
       Robot Movement
---

# Testing Procedure

Several experiments were conducted to validate the robot's performance.

The testing process included:

- Straight-line movement
- Obstacle detection
- Left-turn validation
- Right-turn validation
- Continuous navigation
- Battery endurance

Testing ensured reliable movement under different indoor conditions.

Insert testing images.

---

# Challenges Faced

During development, several practical challenges were encountered.

## Sensor Noise

Ultrasonic sensors occasionally produced unstable readings.

Solution:

Multiple readings were averaged before making navigation decisions.

---

## Motor Speed Difference

The left and right motors did not rotate at identical speeds.

Solution:

Motor control parameters were adjusted to improve straight-line movement.

---

## Mechanical Alignment

Incorrect wheel alignment caused slight directional drift.

Solution:

Mechanical adjustments were performed to improve stability.

---

## Power Stability

Voltage fluctuations affected sensor readings during motor startup.

Solution:

Power distribution and wiring were improved to ensure stable operation.

---

# Implementation Outcome

The implemented prototype successfully demonstrated:

- Autonomous navigation
- Obstacle detection
- Autonomous obstacle avoidance
- Stable embedded control
- Continuous autonomous operation

The project validates the feasibility of designing an embedded autonomous robotic platform using low-cost hardware while providing a scalable foundation for future intelligent robotic systems.
