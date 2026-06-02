# PLC Logic Simulation and Motor Control using LOGO! Soft Comfort and OMRON PLC Trainer

## Project Overview

This repository contains an experiment-based PLC automation project focused on logical simulation and motor control using **LOGO! Soft Comfort** software and an **OMRON PLC Trainer**.  

The main objective of this project is to understand basic PLC programming, ladder logic simulation, motor start-stop control, interlocking operation, and practical PLC trainer implementation.

This project demonstrates how PLC logic can be designed, simulated, and tested for real-world industrial automation applications.



## Experiment Information

**Experiment No:** 01  
**Experiment Name:**  
Logical simulation and problem solving on **LOGO! Soft Comfort** and introduction to **OMRON PLC Trainer**



## Objectives

The objectives of this experiment are:

- To get introduced to **LOGO! Soft Comfort** software.
- To explore the software user interface.
- To design and simulate basic PLC ladder logic.
- To understand motor control using start and stop push buttons.
- To implement interlocking logic between two motors.
- To simulate and test logic on an **OMRON PLC Trainer**.
- To control a physical system using PLC-based logic.



## Tools and Software Used

### Software
- LOGO! Soft Comfort
- OMRON PLC Programming Software

### Hardware
- OMRON PLC Trainer
- Start Push Button
- Stop Push Button
- Induction Motor
- Relay/Output Module
- 24V DC Power Supply
- Connecting Wires



## Problem 1: Single Motor Start-Stop Control

### Input

- One start push button normally open
- One stop push button normally open

### Output

- One induction motor

### Operation

When the start button is pressed, the motor starts running.  
After releasing the start button, the motor continues running due to the latch condition.  
When the stop button is pressed, the motor stops.

### Logic Description

This problem uses a basic **latching circuit**.  
The start button energizes the motor output coil.  
A parallel contact of the motor output is used to hold the circuit after the start button is released.  
The stop button breaks the circuit and turns the motor off.



## Problem 2: Two Motor Interlocking Control

### Input

- Start push button for Motor Q1
- Start push button for Motor Q2
- Stop push button

### Output

- Motor Q1
- Motor Q2

### Operation

- When Start-1 is pressed, Motor Q1 starts.
- When Start-2 is pressed, Motor Q2 starts.
- When the stop button is pressed, the running motor stops.
- When Q1 is running, Q2 circuit remains inactive.
- When Q2 is running, Q1 circuit remains inactive.
- The motors are considered to have no inertia.

### Logic Description

This problem uses an **interlocking control system**.  
The purpose of interlocking is to prevent both motors from running at the same time.  

When Motor Q1 is active, the normally closed contact of Q1 blocks the Q2 circuit.  
Similarly, when Motor Q2 is active, the normally closed contact of Q2 blocks the Q1 circuit.

This type of logic is commonly used in industrial applications where two devices must not operate simultaneously.

---

## OMRON PLC Trainer Implementation

### Input

- One start push button normally open
- One stop push button normally open

### Output

- Induction motor

### Operation

When the start button is pressed, the first motor starts.  
After a limited time delay, the second motor starts automatically.  
When the stop button is pressed, the motor stops.

### Logic Description

The OMRON PLC Trainer was used to test the ladder logic practically.  
A timer was used to introduce delay between the operation of the first and second motor.

This helped to verify the practical behavior of PLC logic after simulation.



## Ladder Logic Concepts Used

This experiment covers the following PLC ladder logic concepts:

- Normally Open Contact
- Normally Closed Contact
- Output Coil
- Latching Circuit
- Motor Start-Stop Control
- Interlocking Logic
- Timer Operation
- PLC Input and Output Mapping
- Practical PLC Trainer Wiring

