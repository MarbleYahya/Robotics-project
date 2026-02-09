# Robotics-project
# Autonomous Ackermann Parking Vehicle
Instrumentation & Embedded Control Project

A small-scale autonomous ground vehicle capable of performing **automatic parallel parking** using ultrasonic perception, servo-based steering, and motor control driven by an Arduino Mega.

---

## 📌 Project Overview

This project demonstrates practical vehicle navigation and motion control in tight environments using low-cost hardware.

The robot follows an **Ackermann steering mechanism**, similar to real cars, and makes decisions based on distance measurements from multiple ultrasonic sensors placed around the vehicle.

The system detects a suitable parking space, performs maneuvering, and stops safely.

---

## 🎯 Objectives

- Design a miniature car-like robot with Ackermann steering.
- Sense surrounding obstacles using ultrasonic sensors.
- Detect free space for parking.
- Execute backward/forward maneuvers automatically.
- Demonstrate autonomous behavior without human intervention.

---

## 🚗 Mechanical & Control Concept

Unlike differential-drive robots, this vehicle uses:

- a **drive motor** for forward/backward motion  
- a **servo motor** to set the steering angle  

This reproduces real vehicle kinematics and makes parking control more realistic.

---

## ✨ Key Features

### 📏 Multi-Directional Distance Measurement
Ultrasonic sensors are mounted on:

- Right  
- Left  
- Front  
- Back  

They continuously measure the environment and help the controller understand available space.

### 🧠 Free Space Detection
The system identifies potential parking gaps by monitoring side distances while moving forward.

### 🔄 Automatic Parking Maneuver
Once a proper space is detected, the vehicle:

- adjusts steering angle  
- moves backward  
- corrects orientation  
- aligns inside the parking zone  

### 🛑 Collision Prevention
Front and rear sensors prevent the robot from hitting obstacles during maneuvers.

### 🎛 Servo-Based Steering
A servo motor dynamically changes the wheel angle to follow the parking trajectory.

---

## 🧠 Control Strategy

The controller operates as a **state-based decision system**.

Typical sequence:

1. Move forward and scan side distances.
2. Detect open space.
3. Trigger direction change.
4. Rotate steering via servo.
5. Move backward into the slot.
6. Use front/back sensors to stop safely.

---

## 🧱 Hardware Architecture

| Component | Description |
|----------|------------|
| Main Controller | Arduino Mega |
| Steering Actuator | Servo motor |
| Drive Actuator | DC motor |
| Distance Sensors | SRF04 ultrasonic modules |
| Motor Driver | PWM + H-bridge / relay |
| Feedback | Real-time distance measurement |

---

## 🔌 Pin Configuration (example)

- Ultrasonic sensors → Trigger/Echo pins  
- Servo → PWM pin  
- Motor driver → direction + enable pins  

(See source code for exact mapping.)

---

## 🛠 Technologies Used

- Arduino / Embedded C  
- Servo control  
- PWM motor driving  
- Ultrasonic ranging  
- Real-time decision making  

---

## 📂 Repository Structure (example)

