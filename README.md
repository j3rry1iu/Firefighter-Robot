# 🤖 Firefighter Robot

A professional autonomous robot project developed using **Great Cow BASIC** for the **PIC16F18875** microcontroller. This robot is designed to navigate a structured environment (rooms), detect fire (flames), and extinguish them using an onboard fan system.

## 🚀 Features

- **Autonomous Navigation:** Uses ultrasonic sensors for wall-hugging and obstacle avoidance.
- **Fire Detection:** Precision flame sensor integration with configurable thresholds.
- **Active Extinguishing:** Automated fan activation with scanning sweeps for reliable suppression.
- **Room Tracking:** Line detection system to track progress through a multi-room environment.
- **LCD Feedback:** Real-time distance and status reporting via a 16x2 LCD display.

## 🛠️ Hardware Stack

- **Microcontroller:** PIC16F18875 (32 MHz Internal Oscillator)
- **Sensors:**
  - Infrared Flame Sensor (Analog)
  - Wall Distance Sensors (Analog)
  - Line Detection Sensor (Digital)
- **Actuators:**
  - Dual-Motor Drive System
  - High-Speed Extinguishing Fan
- **Display:** 16x2 LCD (4-bit Interface)

## 📂 Project Structure

- `main.gcb`: Core logic, sensor processing, and movement routines.
- `.gitignore`: Standard exclusions for GCB compilation artifacts.
- `README.md`: Project documentation and overview.

## ⚙️ Logic Overview

The robot operates on a "Sense-Think-Act" loop:
1. **Sense:** Polls analog inputs for wall distance and flame intensity.
2. **Think:** Processes room count via line detection and determines navigation maneuvers.
3. **Act:** Executes motor commands (Forward, Pivot, etc.) or engages the fire suppression sequence.

### Navigation Decision Matrix
- **Close Front:** Reverse and re-adjust.
- **Far Left:** Pivot left to maintain wall contact.
- **Too Close Left:** Pull right.
- **Obstacle Detected:** Execute right-hand pivot.

## 📝 License

This project is open-source. Feel free to use and modify for educational purposes.

---

*Developed as a Grade 12 Engineering Project.*
