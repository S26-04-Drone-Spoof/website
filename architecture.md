---
title: System Architecture
nav_order: 3
---


# System Architecture


## High-Level Design
The system consists of three major subsystems:
1. **Ground Station (UE5 Virtual Environment)**
   ![System Architecture](/assets/Ground_station.png)
3. **Simulink Bridge (Middleware + Timing Control)**
   ![System Architecture](/assets/Simulink.png)
5. **UAV Edge Device (Neural Network + Sensor Emulation)**
   ![System Architecture](/assets/Edge.png)


## Data Flow

## Control Flow
- Operator configures spoof parameters from GCS
- Simulink synchronizes system timing
- Edge device reports inference status and health


## Power Flow
- Ground Station powered by AC system
- Edge Device powered by 10,000mAh portable battery
- HAL and sensors powered via regulated 5V/12V rails


## Design Principles
- Deterministic timing
- Modular testing
- Hardware-agnostic interfaces
- Safety-first spoof isolation
