# 🚦 Real-Time Traffic Light Controller Based on Density

<p align="center">
  <img src="traffic-system.png" alt="Traffic Light Controller" width="500"/>
</p>

---

## 📌 Project Overview

This project addresses the persistent problem of urban traffic congestion by replacing outdated fixed-time traffic light systems with an intelligent, **density-based control system**.

The system utilizes Infrared (IR) sensors and an **Arduino Mega 2560** microcontroller to dynamically adjust signal timing based on the real-time number of vehicles waiting at an intersection.

By optimizing green light durations, the system aims to:
- Reduce vehicle idling  
- Minimize fuel consumption  
- Improve overall urban mobility  

---

## ✨ Key Features and Objectives

### 🎯 General Objectives
- Develop a density-based traffic light control system  
- Dynamically adjust signal durations based on real-time vehicle density  
- Reduce congestion and pollution  

### ⚙️ Specific Features
- 🚗 **Real-Time Density Detection:** IR sensors detect vehicles  
- 🔄 **Dynamic Signal Adjustment:** Green time increases based on congestion  
- ⏱️ **Countdown Timer:** 7-segment display shows remaining time  
- 📈 **Scalable System:** Can be extended to real-world intersections  

---

## 🧱 Hardware Requirements

| Component | Function | Description |
|----------|--------|------------|
| **Arduino Mega 2560** | Control Unit | Processes sensor data and controls signals |
| **IR Sensors** | Sensor Unit | Detect vehicle presence |
| **LEDs (Red, Yellow, Green)** | Indicator | Simulate traffic lights |
| **7-Segment Display** | Display | Shows countdown timer |
| **Power Supply** | Power | Provides stable voltage |

---

## ⚙️ System Working Principle

### 🔹 Initialization
- Configure LEDs as outputs  
- Configure IR sensors (A0–A7) as inputs  

### 🔹 Normal Operation
- System follows default traffic sequence  
- Each lane gets fixed green time  

### 🔹 Dynamic Adjustment
Based on traffic density:

- ✅ **1 IR Sensor Active → +5 seconds**
- ✅ **2 IR Sensors Active → +10 seconds**

This ensures:
- Faster clearance of congested lanes  
- Reduced waiting time  

### 🔹 Cycle Completion
- System switches to next lane after timer ends  
- Process repeats continuously  

---

## 🛠️ Technologies Used

- Embedded C  
- Arduino IDE  
- IR Sensors  
- Digital Electronics (FSM Logic)  

---

## 📂 Project Structure

```bash
Density-based-traffic-control/
│── traffic-system.png
│── code/
│   ├── traffic_controller.ino
│── README.md
