---
title: Project Schedule
nav_order: 4
---


# Project Schedule


## Development Phases


| Phase | Dates | Focus | Subsystems |
|-------|-------|-------|------------|
| 1a | Oct–Nov | Virtual Environment + Communication | UE5, Simulink |
| 1b | Nov–Dec | Jetson Setup + NN Training | Edge Device, GCS |
| 2 | Jan–Feb | LiDAR Vector Training + Procurement | Full System |
| 3 | Feb–Mar | Dynamic Spoofing Simulations | Full System |
| 4 | Mar–Apr | Physical System Testing | UAV Platform |
| Final | Late April | Presentation & Reporting | Full System |


## Phase 1A – Virtual System Foundation (Jan 20 – Feb 2)
- UE5 LiDAR generation
- TCP communication to Simulink
- Data schema + CRC validation
- GitHub Pages site launch

**Milestone:** End-to-end UE5 → Simulink → Jetson pipeline operational

## Phase 1B – Edge AI Bring-Up (Feb 3 – Feb 13)
- Jetson setup and inference engine
- HAL protocol stub
- Baseline NN model

**Milestone:** Real-time inference at ≥20 Hz

## Phase 2 – Dataset & Procurement (Feb 14 – Mar 1)
- Spoof dataset generation
- Livox sensor configuration
- Training pipeline

**Milestone:** Labeled spoof/real LiDAR dataset complete

## Phase 3 – Dynamic Spoofing (Mar 2 – Mar 20)
- Selective spoofing
- Adaptive attack simulation
- NN accuracy testing

**Milestone:** ≥90% detection accuracy

## Phase 4 – HIL Validation (Mar 21 – Apr 10)
- Simulated UAV flight in UE5
- Telemetry and failover testing
- Verification documentation

**Milestone:** Stable inference under motion and fault conditions

## Final – Expo & Handoff (Apr 11 – Apr 23)
- Poster and presentation
- Sponsor handoff
- Final system archive
