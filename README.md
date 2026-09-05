# EV Battery Safety Monitoring & Fault Detection

## Overview

This project demonstrates a MATLAB-based battery safety monitoring and fault detection system for an Electric Vehicle (EV) battery pack.

The model monitors important battery operating parameters such as:

- Battery Voltage
- Battery Current
- Battery Temperature
- State of Charge (SOC)

The system checks these parameters against predefined operating limits and identifies unsafe operating conditions.

## Objectives

The main objectives of this project are:

- Monitor EV battery operating parameters
- Detect abnormal battery conditions
- Identify specific battery safety faults
- Determine overall battery safety status
- Visualize safety test results using MATLAB plots

## Safety Conditions Monitored

The following conditions are monitored:

1. Over-Voltage
2. Under-Voltage
3. Over-Current
4. Over-Temperature
5. Overcharge

## System Logic

The battery parameters are compared with predefined safety limits.

If all parameters are within their limits:

SAFE

If any parameter exceeds its defined limit:

UNSAFE

The system also identifies the specific fault responsible for the unsafe condition.

## Example Safety Limits

| Parameter | Limit |
|-----------|-------|
| Maximum Voltage | 54 V |
| Minimum Voltage | 39 V |
| Maximum Current | 50 A |
| Maximum Temperature | 60 °C |
| Maximum SOC | 100 % |
| Minimum SOC | 0 % |

These values are example simulation limits used for demonstrating the safety-monitoring logic. Actual battery limits depend on battery chemistry, pack configuration, BMS design, and manufacturer specifications.

## Test Scenarios

The project evaluates multiple battery operating conditions:

| Scenario | Voltage | Current | Temperature | SOC | Expected Result |
|----------|---------|---------|-------------|-----|-----------------|
| Normal | 52 V | 40 A | 35 °C | 85 % | SAFE |
| Over-Voltage | 56 V | 40 A | 35 °C | 85 % | UNSAFE |
| Under-Voltage | 35 V | 40 A | 35 °C | 50 % | UNSAFE |
| Over-Current | 52 V | 65 A | 35 °C | 85 % | UNSAFE |
| Over-Temperature | 52 V | 40 A | 65 °C | 85 % | UNSAFE |
| Overcharge | 54 V | 40 A | 35 °C | 105 % | UNSAFE |

## MATLAB Implementation

The program performs the following steps:

1. Define battery operating parameters
2. Define safety limits
3. Create different test scenarios
4. Check voltage limits
5. Check current limits
6. Check temperature limits
7. Check SOC limits
8. Determine overall battery safety status
9. Identify the detected fault
10. Generate graphical results

## Results

### Overall Battery Safety Status

The first graph shows the overall safety status for each test scenario.

- SAFE indicates that all monitored parameters are within their defined limits.
- UNSAFE indicates that at least one safety condition has been violated.

- <img width="591" height="238" alt="image" src="https://github.com/user-attachments/assets/a86d23bf-6d3b-43ab-95cc-448b8c9078c1" />


### Fault Detection

The second graph identifies the specific fault detected during each test scenario.

The system can identify:

- Over-Voltage
- Under-Voltage
- Over-Current
- Over-Temperature
- Overcharge

  <img width="584" height="231" alt="image" src="https://github.com/user-attachments/assets/aabee36a-6e2b-4aee-a4af-0b2ad2494bc6" />


## Applications

This type of monitoring logic can be used as a basic concept for:

- EV battery monitoring
- Battery Management System (BMS) studies
- Battery safety analysis
- Fault detection
- MATLAB-based EV simulations
- Automotive electrical system development

## Tools Used

- MATLAB
- MATLAB Programming
- Conditional Logic
- Data Visualization
- Battery Safety Monitoring Concepts

## Project Outcome

The project demonstrates how battery operating parameters can be monitored and evaluated using MATLAB to identify potentially unsafe operating conditions.

## Disclaimer

This project is an educational/simulation implementation of battery safety monitoring logic. It is not intended to represent a production BMS or certified battery safety system. Actual battery protection thresholds and safety requirements must be defined according to the specific battery chemistry, pack configuration, BMS architecture, manufacturer specifications, and applicable standards.
