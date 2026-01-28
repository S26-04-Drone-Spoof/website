---
layout: home
title: Home
nav_order: 1
---


# Low-Cost Smart Sensor Spoofer on UAV


This project develops a **real-time, hardware-in-the-loop (HIL) test platform** for simulating and detecting spoofed UAV sensor data. The system combines a virtual sensing environment, a real-time middleware bridge, and an onboard neural network to evaluate how LiDAR, GPS, and multi-sensor data can be manipulated and reliably identified in adversarial conditions.

<div style="text-align:center; margin-bottom: 30px;">
  <iframe 
    width="100%" 
    height="450"
    src="https://www.youtube.com/embed/VIDEO_ID"
    title="Project Demo"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>


## Project Goals
- Simulate realistic and adversarial UAV sensor environments
- Generate spoofed and authentic LiDAR/GPS data streams
- Detect spoofing using embedded neural networks
- Support SIL and HIL validation workflows
- Provide scalable, low-cost research platform


## System Overview
The platform integrates:
- **Unreal Engine 5** for virtual LiDAR generation and spoofing
- **Simulink Bridge** for real-time data synchronization
- **UAV Edge Device (Jetson)** for neural inference
- **Ground Control Station** for configuration and monitoring


Use this site to explore the architecture, schedule, testing strategy, and project resources.
