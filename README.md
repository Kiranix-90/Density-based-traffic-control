# 🚦 Real-Time Traffic Light Controller Based on Density

<p align="center">
  <img src="images/traffic-system.png" alt="Traffic Light Controller" width="500"/>
</p>

---

## 📌 Project Overview

This project addresses the persistent problem of urban traffic congestion by replacing outdated fixed-time traffic light systems with an intelligent, **density-based control system**.  

The system utilizes Infrared (IR) sensors and an **Arduino Mega 2560** microcontroller to dynamically adjust signal timing based on the real-time number of vehicles waiting at an intersection.

By optimizing green light durations, the system aims to:
- Reduce vehicle idling  
- Minimize fuel consumption  
- Improve overall traffic flow  

---

## ✨ Key Features and Objectives

### 🎯 General Objectives
- Develop a density-based traffic light control system  
- Dynamically adjust signal durations based on real-time vehicle density  
- Reduce congestion and environmental pollution  

### ⚙️ Specific Features
- 🚗 **Real-Time Density Detection:** IR sensors detect vehicle presence  
- 🔄 **Dynamic Signal Adjustment:** Arduino adjusts green time based on density  
- ⏱️ **Countdown Timer Display:** 7-segment display shows signal timing  
- 📈 **Scalable Design:** Can be extended to larger intersections  

---

## 🧱 Hardware Requirements

| Component | Function | Description |
|----------|--------|------------|
| **Arduino Mega 2560** | Control Unit | Processes sensor data and controls signals |
| **IR Sensors** | Sensor Unit | Detect vehicle presence and density |
| **LEDs (R/Y/G)** | Indicator | Simulate traffic signals |
| **7-Segment Display** | Display | Shows countdown timer |
| **Power Supply** | Power | Provides stable voltage |

---

## ⚙️ System Working Principle

### 🔹 Initialization
- Configure LED pins as outputs  
- Configure IR sensors (A0–A7) as inputs  

### 🔹 Normal Operation
- System runs with default traffic signal sequence  
- Each lane gets fixed green time  

### 🔹 Dynamic Adjustment
Based on IR sensor input:

- ✅ **1 Sensor Active → +5 seconds**
- ✅ **2 Sensors Active → +10 seconds (heavy traffic)**

This ensures:
- More time for congested lanes  
- Less waiting for vehicles  

### 🔹 Cycle Completion
- After time expires, system switches to next lane  
- Process repeats continuously  

---

## 🛠️ Technologies Used

- Embedded C  
- Arduino IDE  
- IR Sensor Modules  
- Digital Electronics (FSM logic)  

---

## 📂 Project Structure

```bash
Traffic-Control-System/
│── code/
│   ├── traffic_controller.ino
│── images/
│   ├── traffic-system.png
│── README.md
