
# DC Motor Controller Project with Linear Guide System

## Project Overview

This project involves the design and implementation of a control system for a DC motor with brushes, aimed at moving a 5 kg load along a motorized linear guide. The goal is to achieve optimal movement from a starting position \(x_0\) to a final position \(x_f\) in the shortest time possible, with a final velocity of 0 m/s, using a time-optimal control approach.

### Key Features
- **Linear Guide Selection**: The project utilizes the AK42 linear guide developed by C.T.S., selected based on the required load capacity and maximum speed of 1 m/s.
- **Motor Selection**: The motor chosen is a DC motor with brushes, model ROK 311M, coupled with a reduction gear. This motor meets the project's torque and speed specifications.
- **Control Strategy**: A Proportional-Integral (PI) controller was implemented to ensure precise speed control, coupled with a Feed-Forward component to handle speed ramp references and reduce steady-state errors.
- **Simulation**: The system was modeled and simulated in MATLAB/Simulink to verify its performance, including the motor model, current limiter, and feedback components.

## Components

### 1. Linear Guide
- **Specifications**:
  - Maximum Speed: 1 m/s
  - Maximum Acceleration: 0.8 m/s²
  - Load Capacity: 5 kg
  - Model: AK42 by C.T.S.

### 2. DC Motor
- **Model**: ROK 311M
- **Power**: 70 W
- **Nominal Speed**: 429 rpm
- **Nominal Torque**: 1.2 Nm
- **Reduction Ratio**: 7:1

### 3. Control System
- **PI Controller**: Designed for speed control, ensuring stability and zero steady-state error.
- **Feed-Forward**: Integrated to improve tracking of speed ramp references.
- **Current Limiter**: Protects the motor from high startup currents.
- **Simulink Models**: Complete system simulations were carried out to test and optimize performance.

## Simulations and Results

MATLAB/Simulink was used to simulate the motor, linear guide, and control system behavior. The simulations confirmed that the control system could efficiently move the load along the linear guide while meeting the specified constraints for speed, position, and current ripple.

The final results show:
- Accurate speed and position control.
- Respect for the imposed current limits.
- Robust response to disturbances, such as additional load mass.

## Getting Started

### Prerequisites
- MATLAB and Simulink installed.
- Basic knowledge of control systems and DC motor operation.

### How to Run
1. Open the provided Simulink models in MATLAB.
2. Run the simulation and observe the output graphs for speed, position, and current.
3. Modify the input parameters (e.g., mass or speed) to test different scenarios.

## Future Improvements
- Enhance the controller by adding adaptive control to handle varying load conditions.
- Implement real-time testing using a physical setup with sensors and a microcontroller.
