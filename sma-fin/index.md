# Morphing Structure for a Soft Underwater Swimmer Using SMA

**Semester project at EPFL CREATE Lab**  
**Author:** Nicola Zali  
**Supervisor:** Prof. Josie Hughes  
**Project mentor:** Nana Obayashi

---

## Overview

This project explores the use of shape memory alloys (SMAs) to modify the geometry of a robotic fish caudal fin.

Instead of using SMA actuators to directly generate thrust, the goal is to use them to adapt the fin geometry in order to optimize propulsion efficiency.

This approach aims to let the robot switch between:
- high-thrust configurations
- more energy-efficient cruising configurations

The project investigates whether morphing geometry can expand the achievable performance envelope of underwater propulsion systems.

---

## Morphing Fin Design

The fin was designed as a hand-fan-inspired mechanism composed of rigid segments connected by flexible hinges.

The opening angle of the fin can vary between **30° and 60°**, changing the effective surface area from approximately **37.7 cm² to 75.4 cm²**.

This allows dynamic control of the propulsion surface during operation.

---

## Actuator Study

Several actuator configurations were tested:
- straight NiTiCu wire
- straight Nitinol wire
- NiTiCu coil
- Flexinol

Each actuator was evaluated based on:
- activation energy
- output force
- actuation speed
- range of motion

Among the tested solutions, the **NiTiCu coil** provided the best compromise between force, displacement, speed, and energy consumption.

---

## Experimental Setup

A custom experimental setup was built to test the fin in water. The system includes:
- a Dynamixel motor to oscillate the fin
- a load cell to measure thrust
- a stepper motor to adjust fin geometry
- an Arduino for load cell acquisition and stepper control
- a Python script for synchronized control and data logging

The fin oscillates with a sinusoidal motion while the opening angle can be adjusted during operation.

Tested input ranges:
- **Oscillation range:** 80°–120°
- **Frequency:** 0.3–0.6 Hz
- **Fin opening angle:** 30°, 45°, 60°

---

## Results

### Test 1 — Dynamic Surface-Area Sweep

The first test was performed at fixed motor conditions while gradually reducing the fin opening angle.

The results confirmed the expected trend:
- decreasing fin area reduced thrust
- decreasing fin area also reduced power consumption

This validated both the morphing fin concept and the ability to control geometry reliably during motion.

### Test 2 — Performance Envelope Exploration

The second test explored the combined effect of:
- oscillation range
- oscillation frequency
- fin opening angle

A total of **63 configurations** were planned, and **46 valid results** were obtained.

The results showed that adding fin geometry as a control parameter expands the achievable performance space of the system. However, the relationship between fin area and efficiency was more complex than initially expected.

---

## SMA Actuation Results

The SMA actuator was successfully integrated and tested in air.

Key observations:
- it could close the fin effectively
- it was faster than the stepper motor during activation
- it could not reliably maintain intermediate positions
- cooling and reopening were significantly slower

When tested in water, the SMA actuator required more current than the available power supply could provide, which prevented successful underwater operation.

This highlighted one of the main limitations of SMA actuation in underwater environments: high energy demand and thermal losses.

---

## Software and Control

The project also involved the development of a custom control and acquisition framework including:
- Python code for Dynamixel motor control
- synchronized load-cell data acquisition
- Arduino code for stepper motor actuation
- CSV logging of motor and thrust data

The system was designed to:
- oscillate the fin at controlled frequency and amplitude
- update fin geometry during motion
- log thrust, position, velocity, current, and PWM data

---

## Files

- [Project report](../semester_project.pdf)

You can also add:
- code files
- figures
- photos of the prototype
- plots from the experiments

---

## Future Work

Possible next steps include:
- improved thermal insulation for SMA wires
- mechanical locking mechanisms to hold fin positions without continuous heating
- direct measurement of fin-specific efficiency
- testing under real swimming conditions instead of in a stationary tank
