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

- ## Observation

During the experiment, LOGO! Soft Comfort software was used to design and simulate PLC ladder logic for motor control operations. The software interface allowed the input and output conditions to be clearly observed during simulation.

In the first problem, a start-stop motor control circuit was simulated. When the start push button was pressed, the motor output became active. After releasing the start button, the motor continued running because of the latching condition. When the stop push button was pressed, the latch was broken and the motor stopped successfully.

In the second problem, two motor control circuits were simulated using interlocking logic. When Start-1 was pressed, Motor Q1 started and Motor Q2 remained inactive. Similarly, when Start-2 was pressed, Motor Q2 started and Motor Q1 remained inactive. This confirmed that the interlocking logic prevented both motors from running at the same time.

The OMRON PLC Trainer was also used to test the motor control logic practically. The start and stop push buttons were connected with the PLC input terminals, and the motor output was controlled through the PLC output terminal. The ladder logic worked properly in the hardware setup. A timer function was used to start the second motor after a limited time delay.

Overall, both the software simulation and hardware implementation showed correct operation according to the given problem conditions.

## Discussion

This experiment provided practical knowledge about PLC-based motor control using ladder logic. LOGO! Soft Comfort software was helpful for understanding how input contacts, output coils, latching circuits, interlocking circuits, and timer functions work in a PLC system.

The first problem demonstrated the basic concept of a latching circuit. In industrial motor control, a motor should continue running after the start button is released. This was achieved by using a holding contact parallel to the start push button. The stop button was used to disconnect the circuit and stop the motor safely.

The second problem demonstrated the importance of interlocking in motor control. Interlocking is necessary when two motors or two outputs should not operate at the same time. By using the normally closed contact of one motor in the circuit of the other motor, simultaneous operation was prevented. This type of logic is very useful in industrial automation systems where safety and proper sequence control are required.

The OMRON PLC Trainer helped to verify the practical application of the simulated logic. The connection between software logic and physical hardware was observed clearly. The use of a timer also showed how PLCs can control operations based on time delay. This is important for sequential motor starting and other automation processes.

The experiment successfully connected theoretical PLC logic with real hardware operation. It improved understanding of PLC programming, simulation, wiring, and troubleshooting.

## Conclusion

In this experiment, PLC ladder logic was designed, simulated, and tested using LOGO! Soft Comfort software and an OMRON PLC Trainer. The start-stop motor control circuit operated successfully using latch logic. The two-motor control circuit also worked properly using interlocking logic, which prevented both motors from running at the same time.

The OMRON PLC Trainer implementation confirmed that the simulated ladder logic could also operate correctly in a practical hardware system. The timer-based control also worked as expected.

Therefore, the experiment was successful. It helped to develop a clear understanding of PLC ladder logic, motor control, latching operation, interlocking system, timer operation, and practical PLC trainer connection.
