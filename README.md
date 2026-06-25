# Self-Balancing Robot

An autonomous two-wheeled robot designed to maintain balance using PID control and real-time sensor feedback.
---

## 🚀 Overview
This project is a high-performance self-balancing robot utilizing advanced control theory. It is designed for stability, responsive movement, and mechanical precision.

## 🛠 Hardware
The robot is built with a custom-designed chassis, optimized for weight distribution and motor torque.

* **Microcontroller:** Teensy 4.0 / Arduino-compatible
* **IMU:** 6-axis IMU (e.g., MPU6050)
* **Motors:** High-torque N20 gear motors
* **Power:** 2S LiPo battery
* **Chassis:** Custom 3D-printed components

## 📂 CAD Models
The mechanical design was developed using OnShape and exported as STL/STEP files for 3D printing.
* **Chassis Components:** Located in the `/cad` directory.
* **Assembly:** Designed for precision fits to reduce mechanical vibration during high-speed balancing.

## 🔌 Electronics & Wiring
* **IMU:** Connected via I2C to the microcontroller.
* **Motor Driver:** Bridges the microcontroller and motors, utilizing PWM for speed control.
* **Grounding:** All components share a common ground to ensure signal integrity.

## 💻 Software
The firmware is written in C++ and utilizes:
* **Sensor Fusion:** Complementary filter for IMU data.
* **Control Loop:** PID algorithm running at a high frequency to maintain the center of gravity.

## ⚙️ PID Tuning
The stability of the robot relies on precise tuning of the PID constants:
* **Kp (Proportional):** Adjusts the reaction force based on the current angle error.
* **Ki (Integral):** Eliminates steady-state error over time.
* **Kd (Derivative):** Provides damping to prevent overshoot and oscillations.
