
# STM32-Based Autonomous Line-Following Robot

**Embedded Systems Project | The University of Manchester**  
**Project Duration:** October 2025 – May 2026  
**Role:** Team Leader

## 1. Project Overview

This project involved the design, development, and experimental optimisation of an STM32-based autonomous mobile robot capable of navigating a challenging line-following course.

The robot was designed to handle continuous curves, downhill sections, broken-line segments, 90-degree turns, and U-turns while maintaining stable autonomous motion.

The project integrated hardware design, infrared sensing, embedded control, motor actuation, and wireless communication.

## 2. Hardware Design

### Drivetrain Optimisation
- Conducted motor and gearbox experiments to evaluate different gear-ratio configurations.
- Selected a drivetrain configuration that maximised wheel speed under the required payload.

### Infrared Sensing System
- Experimentally compared infrared sensors based on signal contrast between black and white surfaces.
- Selected TCRT5000 infrared sensors for reliable line detection.
- Designed a six-sensor PCB array with 20 mm spacing.
- Implemented switched infrared illumination and ambient-light subtraction to reduce interference from environmental lighting.

## 3. Embedded Control System

The embedded control architecture integrates the following components:

### Weighted Line-Position Estimation
- Processes measurements from six infrared sensors.
- Estimates the position of the detected line relative to the robot centre.

### PD Steering Control
- Uses proportional and derivative feedback to regulate steering based on line-position error.
- Supports stable navigation through straight sections and curves.

### Closed-Loop Wheel-Speed Control
- Uses wheel encoder feedback to estimate rotational speed.
- Adjusts motor actuation through PWM to regulate wheel speed.

### Finite-State Machine (FSM)
Implements different navigation behaviours for:
- Normal line following
- Line-loss recovery
- Braking
- Slope traversal
- 90-degree turns and U-turns

### Bluetooth Communication
- Integrated BLE-based supervisory control.
- Supports remote start/stop and operating-mode selection.

## 4. Experimental Validation and Results

The complete robotic system was evaluated on a challenging course incorporating continuous curves, downhill sections, broken-line segments, 90-degree turns, and U-turns.

**Key Results:**
- Increased maximum stable operating speed from **1.51 m/s to 1.81 m/s**, representing an improvement of approximately **20%**.
- Maintained reliable autonomous navigation across different course sections.
- Achieved **4th place among 52 competing teams** in the final competition.

## 5. Source Code

The final embedded control implementation is available here:

[View final.cpp](final.cpp)

## 6. Team and Contributions

This project was completed as part of a team-based Embedded Systems course project at The University of Manchester.

**Role: Team Leader**

Participated in and coordinated hardware optimisation, sensor-system development, embedded control implementation, system integration, and experimental testing.

The source code originated from a collaborative team repository.

**Original Team Repository:**  
https://github.com/WajihaShamsi/ESP_Buggy_TDs
