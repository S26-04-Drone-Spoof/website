---
title: Verification & Validation
nav_order: 5
---


# Verification & Validation Strategy


## Testing Philosophy
The system is validated using a **layered SIL/HIL testing strategy**:


- Virtual sensor testing (UE5)
- Middleware timing verification (Simulink)
- Embedded inference validation (Jetson)
- End-to-end spoof detection performance


## Subsystem Tests


### Spoofing Module
- Baseline real signal transmission
- Spoofed signal injection
- Mixed real/spoof validation


### Neural Network Module
- Classification accuracy testing
- Overfitting detection
- Real-time performance benchmarking


### Control System
- Flight stability under spoof drift
- Failsafe activation testing


### Ground Station
- Range testing
- Data integrity validation


## Metrics
- Accuracy > 90%
- Latency < 80 ms end-to-end
- Frame rate 20–30 Hz
- Packet integrity > 95%
