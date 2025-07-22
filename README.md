# 🚀 Closed-Loop Stepper Motor Driver Design

This project presents the design, implementation, and evaluation of a closed-loop stepper motor driver system built for high-precision motion control applications. Unlike traditional open-loop drivers, this system integrates real-time feedback to enhance positioning accuracy, reduce vibrations, and eliminate missed steps under dynamic loads.

---

## 📌 Key Objectives

- ✅ Develop a **closed-loop driver** for a 2-phase **NEMA 17 stepper motor**
- ✅ Implement **Field-Oriented Control (FOC)** on a DSP-supported microcontroller
- ✅ Improve motion accuracy and efficiency under load variations
- ✅ Reduce power loss and vibration typically found in open-loop systems

---

## 🧠 System Overview

### 🔧 Hardware Components

- **Microcontroller Unit (MCU)**: TI **C2000 DSP** (real-time processing and motor control)
- **Driver IC**: Toshiba **TB67H400AFTGEL**
  - Dual H-Bridge output
  - Low ON-resistance
  - Built-in thermal shutdown, overcurrent protection
- **Motor**: 2-phase **NEMA 17** stepper motor
- **Feedback**:
  - Encoder (optional)
  - Sensorless current/EMF-based estimation
- **Power Supply**: 15–24 V regulated input
- **Current Sensing**: Low-side shunt resistors and differential amplifiers

---

## 🧪 Software and Control

- **Control Algorithm**: Field-Oriented Control (FOC)
  - Real-time current regulation
  - Position and speed estimation using feedback
- **PWM Generation**:
  - Sinewave PWM with configurable frequency
  - Dead-time insertion and protection
- **Closed-loop Logic**:
  - PID control loop for speed and position
  - Torque control using quadrature axis current
- **Platform**: Code Composer Studio (TI), C/C++

---

## 🛠️ Design Process

### 📐 Circuit Design

- Designed full schematic in [software name, e.g., EasyEDA/Altium]
- Included motor protection, logic-level shifting, power decoupling, and feedback interface

### 🔳 PCB Layout

- 2-layer custom PCB design
- Optimized trace width for motor currents
- Separate analog and digital ground planes for signal integrity

### 🧰 Prototype Setup

- Assembled testbench with:
  - Power supply
  - Stepper motor and driver PCB
  - Oscilloscope and logic analyzer for debugging
- Firmware testing and tuning via UART or onboard debug interface

---

## 📈 Performance Evaluation

| Category           | Metrics / Notes                                          |
|--------------------|-----------------------------------------------------------|
| **Accuracy**       | Improved micro-stepping and reduced positional error      |
| **Efficiency**     | Lower current draw under load due to dynamic adjustment   |
| **Stability**      | Minimal resonance and smoother acceleration/deceleration |
| **Thermal**        | Lower heat buildup due to current feedback regulation     |

---

## 💡 Applications

- CNC machines
- Robotics and automation arms
- 3D printers and plotters
- Precision positioning systems

---

## 📷 Media & Diagrams

> 📎 _[Insert schematic, PCB layout, and prototype images or upload them to the repo]_  
> 📽️ _[Optional: Add demo video or link to test run]_

---

## ⚠️ Notes

- PID parameters must be tuned based on motor characteristics and system load.

---



