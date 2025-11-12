# 🚦 Real-Time Traffic Light Controller Based on Density

## Project Overview

This project addresses the persistent problem of urban traffic congestion by replacing outdated fixed-time traffic light systems with an intelligent, **density-based control system**[cite: 118]. [cite_start]The system utilizes Infrared (IR) sensors and an **Arduino Mega 2560** microcontroller to dynamically adjust signal timing based on the real-time number of vehicles waiting at an intersection.

By optimizing green light durations, the system aims to reduce vehicle idling, minimize fuel consumption, and improve overall urban mobility.

## ✨ Key Features and Objectives

The system is designed to be a cost-effective, scalable, and adaptable solution.

### General Objectives
* To develop a density-based traffic light control system that dynamically adjusts signal durations based on real-time vehicle density.
* To optimize traffic flow, reduce congestion, and minimize fuel consumption and environmental pollution.

### Specific Features
* **Real-Time Density Detection:** Uses IR sensors to accurately detect the presence and density of vehicles in each lane.
* **Dynamic Signal Adjustment:** The Arduino Mega 2560 processes sensor data to dynamically allocate longer green-light durations to heavily congested lanes.
* **Local Indication:** Uses LEDs to simulate traffic lights and 7-segment displays to show the countdown timer for signal duration.
* **Scalability:** Designed to be suitable for various intersections, from small to complex urban road networks.

## 🧱 Hardware Requirements

| Component | Function | Detail/Connection |
| :--- | :--- | :--- |
| **Arduino Mega 2560**  | [cite_start]**Control Unit.** Processes sensor data and controls traffic light LEDs and displays[cite: 131]. | [cite_start]Features 54 digital and 16 analog I/O pins required for a multi-lane system[cite: 431]. |
| **Infrared (IR) Sensor** | [cite_start]**Sensor Unit.** Detects vehicle presence and measures density in real-time[cite: 130]. | [cite_start]Chosen for its affordability, high reliability, non-intrusiveness, and resistance to adverse weather conditions. |
| **LEDs (Red, Yellow, Green)** | [cite_start]**Indicator Unit.** Simulates the traffic light signals[cite: 747]. | Standard traffic light representation. |
| **Double 7-Segment Display** | [cite_start]Displays the countdown timer for signal durations[cite: 477]. | [cite_start]Displays two-digit numeric time remaining for drivers[cite: 477]. |
| **Power Supply** | [cite_start]Provides stable power to the system. | N/A |

## ⚙️ System Working Principle

### Initialization
[cite_start]The system starts, configuring the traffic light LEDs as outputs and IR sensor pins (Analog A0 - A7) as inputs.

### Normal Operation
[cite_start]The lights initially cycle on a predefined sequence with fixed green times.

### Dynamic Adjustment
The Arduino checks sensor input for density:
* If **one IR sensor** is activated, the green light duration for that lane receives an additional **5 seconds**.
* If **two IR sensors** are activated (heavy congestion), the green light duration receives an additional **10 seconds** (or a maximum time like 20 seconds).

### Cycle Completion
After the dynamically adjusted time elapses, the system returns to the normal sequence, serving the next road.
