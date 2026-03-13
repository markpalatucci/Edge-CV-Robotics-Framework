# Edge-CV-Robotics-Framework

![Robotics](https://img.shields.io/badge/Robotics-Edge-blue)
![Computer Vision](https://img.shields.io/badge/CV-RealTime-green)
![On-Device ML](https://img.shields.io/badge/ML-OnDevice-orange)

## Overview

**Edge-CV-Robotics-Framework** is a modular software stack designed for robots that require high-speed visual processing and precise motion control on resource-constrained hardware (e.g., ARM-based embedded systems). This project draws on experience from mass-produced consumer robots to provide a stable, low-latency foundation for modern robotics development.

## Key Features

- **Asynchronous Vision Pipeline:** Decouples frame acquisition from ML inference to maintain high control loop frequency.
- **On-Device Inference:** Optimized for CoreML, TensorFlow Lite, and ONNX backends.
- **Lightweight Kinematics:** Efficient C++/Python implementations for forward and inverse kinematics.
- **Proactive Navigation:** Predictive path planning based on visual odometry and SLAM data.

## Architecture

`mermaid
graph TD
    Sensor[Camera/IMU] --> Pipeline[Async Vision Pipeline]
    Pipeline --> Inference[ML Inference: Detection/Pose]
    Inference --> Logic[Behavioral Logic]
    Logic --> Controller[Motion Controller]
    Controller --> Actuators[Motors/LEDs]
`

## Getting Started

`ash
git clone https://github.com/markpalatucci/Edge-CV-Robotics-Framework.git
cd Edge-CV-Robotics-Framework
pip install -r requirements.txt
`

## Related to My Background

This framework is built with the same philosophy used to develop **Cozmo** and **Anki Overdrive**: making complex AI feel seamless and reactive in a small, consumer-friendly package. It also integrates modern on-device ML practices essential for proactive intelligent systems.

---
**Maintained by Mark Palatucci, PhD**