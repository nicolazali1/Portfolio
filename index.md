# Nicola Zali

Master student in Mechanical Engineering at EPFL, with a strong interest in robotics, control systems, prototyping, and experimental engineering.

This page presents a selection of academic projects developed during my studies. For each project, I provide a short overview of the objective, my personal contribution, the main challenges, and the project material.

---

## Morphing Structure for Soft Underwater Swimmer using SMAs

**Semester project — EPFL CREATE Lab**  
**Supervisor:** Prof. Josie Hughes  
**Project mentor:** Nana Obayashi  
**Workload:** 10 ECTS  

### Overview

This project explores the use of shape memory alloys (SMA) to dynamically modify the geometry of a robotic fish caudal fin. Instead of using SMA actuators to directly generate thrust, the goal was to adapt the fin surface area in order to optimize propulsion efficiency under different operating conditions.

### My work

- Designed a morphing caudal fin inspired by a hand-fan mechanism with adjustable surface area
- Built a complete experimental setup to measure thrust and energy consumption
- Integrated a Dynamixel motor, load cell, stepper motor and Arduino into a synchronized test system
- Developed Python software to control the experiment and log sensor data

### Challenges

The main challenge was using SMA actuators in water, where thermal losses significantly increase the required activation energy. This required actuator characterization and iterative prototyping to evaluate feasible solutions.

### What I learned

This project allowed me to gain practical experience in experimental robotics, rapid mechanical prototyping, actuator characterization and hardware control using Python.

### Project material

- [Report](files/SP_report.pdf)
- [Video / Photos](files/sma_fin_media.pdf)

---

## OmniSense: Wearable Haptic Guidance System for Visually Impaired Individuals

**Project in collaboration with the EPFL RRL Lab**  
**Supervisor:** Prof. Jamie Paik  
**Workload:** Group project (6 members, 5 ECTS)

### Overview

The goal of this project was to design and build a wearable device capable of assisting visually impaired individuals during everyday navigation. The system detects nearby obstacles and provides haptic feedback to guide the user safely through the environment.

### My work

- Designed and assembled the electronic system of the device
- Built and soldered the hardware components
- Designed the haptic feedback modules integrated into the wearable system
- Contributed to the implementation of a PI controller for feedback regulation

### Challenges

This project involved several real-world engineering challenges, including hardware integration, reliable sensing, and compact wearable design. Working in a multidisciplinary team required effective communication and coordination between mechanical, electronic, and control components.

### What I learned

Through this project I gained practical experience in electronics prototyping, hardware integration, and embedded system development. I also improved my ability to collaborate in a team and to approach engineering problems in a structured and practical way.

### Project material

- [Report](files/ME410_report.pdf)
- [Video](files/omnisense_video.mp4)
- [Poster](files/ME410_poster.pdf)
- [Presentation](files/ME410_presentation.pdf)

---

## Autonomous Vehicle Control Using Model Predictive Control (EPFL, ME-425)

**Group project (4 students, 4 weeks)**

### Overview

Final project of the Model Predictive Control course. The objective was to implement an MPC controller based on a provided vehicle model in MATLAB, allowing the simulated car to perform several driving maneuvers including cruise control, safe car following, and overtaking.

### My contribution

- Implemented and tuned the MPC controller in MATLAB
- Defined constraints and cost function for safe vehicle behavior
- Tested and validated the controller in simulation

### Outcome

The final controller successfully performed cruise control, safe distance tracking, and overtaking maneuvers in the simulation environment.

### Project material

- [Report](files/mpc_vehicle_control_report.pdf)

---

## Sudoku Game for Nintendo DS (EPFL, EE-310)

**Group project (2 students, 4 weeks)**

### Overview

In this project we developed a Sudoku game for the Nintendo DS using C. The program had to make use of the console’s hardware capabilities, including graphics, sound effects, and multiple input peripherals.

### My contribution

- Implemented core game logic and memory management
- Optimized the code to work within the limited hardware resources of the console
- Contributed to the integration of graphics, user input, and audio

### Outcome

The final game ran smoothly both in the emulator and on a physical Nintendo DS console.

---

## Navigation Program for Thymio Robot (EPFL, MICRO-452)

**Group project (4 students, 4 weeks)**

### Overview

The objective of this project was to implement global navigation and obstacle avoidance for a Thymio robot. A camera mounted above the environment was used to detect the robot, the terrain boundaries, and obstacles.

The detected obstacles were expanded and converted into polygons. A global path was then computed using Dijkstra’s algorithm between the polygon vertices to determine the shortest path to the goal.

During navigation, a Kalman filter estimated the robot’s state. If the robot detected obstacles not visible to the camera using its onboard proximity sensors, it switched to local navigation to avoid the obstacle and then returned to global navigation once the path was clear.

The system was also designed to handle two failure cases:

- kidnapping, where the robot is moved to a new position and must recompute the path
- camera occlusion, where the robot relies temporarily on the Kalman filter state estimation

### My contribution

- Implemented the computer vision pipeline used to detect the robot, environment boundaries, and obstacles
- Extracted polygon nodes from detected obstacles
- Estimated robot position and orientation at each frame
- Computed the distance matrix and implemented the Dijkstra path-planning algorithm

### Outcome

The final system successfully performed global navigation, obstacle avoidance, and path replanning during disturbances.

### Project material

- [Video](files/thymio_navigation_video.mp4)

---

## 2D CFD Simulation of a VTOL Aircraft (EPFL, ME-474)

**Group project (4 students, 7 weeks)**

### Overview

In this project we performed a 2D computational fluid dynamics (CFD) simulation of a VTOL aircraft using ANSYS Fluent. The objective was to analyze the aerodynamic behavior of the vehicle during the transition from vertical to horizontal flight.

The study focused on the evolution of lift and thrust as the vehicle changes orientation, as well as the interaction between the propeller flow and the wing.

### My contribution

- Set up the CFD simulation in ANSYS Fluent
- Generated and refined the computational mesh
- Ran simulations for different transition angles
- Analyzed aerodynamic forces and flow behavior

### Outcome

The simulations provided insight into how the aerodynamic forces evolve during the transition phase and helped identify configurations that improve flight stability.

### Project material

- [Report](files/vtol_cfd_report.pdf)
