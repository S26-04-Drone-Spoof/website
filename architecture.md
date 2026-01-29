---
title: System Architecture
nav_order: 3
---

# System Architecture
{: .no_toc }

This section documents the system-level architecture, data pathways, and design principles for the **Low-Cost Smart Sensor Spoofer on UAV** platform. The design emphasizes modularity, deterministic timing, and hardware abstraction to support both simulation-based validation and edge deployment.

---

## High-Level Architecture Overview

The system is composed of three tightly-coupled subsystems that form a closed-loop digital thread:

**Virtual sensing → Middleware → Edge inference → Telemetry feedback**

---

## 1. Ground Station — UE5 Virtual Environment

**Role:** Virtual sensor generator and operator control interface

![Ground Station Architecture](/assets/Ground_station.png)

### Functions
- Generates synthetic LiDAR point clouds using raycasting and scene geometry  
- Injects configurable spoofing profiles (range shift, ghost targets, dropout)  
- Streams time-tagged frames to Simulink over TCP  
- Provides operator control for attack parameters and scenario selection  

---

## 2. Simulink Bridge — Middleware & Timing Control

**Role:** System synchronization and protocol translation layer

![Simulink Bridge Architecture](/assets/Simulink.png)

### Functions
- Validates incoming frames using CRC and sequence counters  
- Enforces deterministic timing and buffering  
- Converts virtual frames into sensor-accurate message formats  
- Routes telemetry and inference results back to the GCS  

---

## 3. UAV Edge Device — Neural Inference & Sensor Emulation

**Role:** Real-time spoof detection and hardware abstraction

![Edge Device Architecture](/assets/Edge.png)

### Hardware Stack
- **Jetson Nano / Orin Nano** — Edge AI inference  
- **Raspberry Pi / MCU HAL** — Sensor bus emulation  
- **Livox LiDAR** — Real-world signal validation  

### Functions
- Runs quantized neural network for spoof classification  
- Emulates sensor buses (UART, I²C, SPI)  
- Publishes telemetry, health, and confidence metrics  
- Engages fallback logic under real-time constraint violations  

---

## System Data Flow

**UE5 Virtual LiDAR + Spoof Profiles** -> TCP (Frame + CRC + Timestamp) -> **Simulink Middleware** -> Sensor-Accurate Packets -> **Edge Device (Jetson + HAL)** -> Inference + Health Metrics -> Telemetry Feedback → Ground Station

### Data Characteristics
- Data Characteristics
- Frame-based point cloud transport
- Time-tagged packets with integrity verification
- Bounded queues for real-time determinism

## Control Flow
### Operator-in-the-Loop Execution Model
1. Operator configures spoof parameters in the Ground Station
2. Simulink synchronizes global timing and validates frames
3. Edge device executes inference and decision logic
4. Status, confidence, and system health are returned to the operator

