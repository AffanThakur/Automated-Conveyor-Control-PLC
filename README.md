# Automated Conveyor Control Using OpenPLC

## Project Overview

This project demonstrates a PLC-based automated conveyor control system developed and tested using OpenPLC software simulation.

The system incorporates motor start/stop control, motor seal-in logic, overload fault detection, fault latching and reset, product counting, batch completion control, and run/fault status indicators.

The PLC logic was evaluated through 14 documented software simulation checks covering normal operation, fault handling, and product counting.

**Development Environment:** OpenPLC Editor

**Programming Language:** Ladder Diagram (LD)

**Testing Method:** Software simulation only; no physical PLC hardware was used.


## PLC System Features

- **Motor Start/Stop Control:** Start and stop pushbutton logic with a motor seal-in circuit to maintain operation after the start signal is released.
- **Overload Protection:** Simulated overload conditions stop the conveyor motor and activate a latched fault.
- **Fault Reset:** The fault latch can be cleared using a reset command after the overload condition has been removed.
- **Product Counting:** A PLC counter tracks product sensor activation events.
- **Batch Completion:** The conveyor stops automatically when the product count reaches the preset batch quantity of 10.
- **Run Status Indicator:** A simulated run lamp indicates when the conveyor motor is operating.
- **Fault Status Indicator:** A simulated fault lamp indicates when an overload fault has been latched.


## PLC Ladder Logic Description

The conveyor control program was developed using six ladder logic rungs in OpenPLC Editor.

1. **Rung 1 – Motor Control:** Implements start/stop control, motor seal-in logic, overload permissive, fault interlock and batch completion interlock.
2. **Rung 2 – Fault Detection:** Detects an overload condition and sets the latched fault bit.
3. **Rung 3 – Fault Reset:** Clears the fault latch when the overload condition has been removed and the reset button is activated.
4. **Rung 4 – Product Counter:** Uses a CTU counter to count product sensor rising edges, with a preset batch quantity of 10 and reset functionality.
5. **Rung 5 – Run Indicator:** Activates the run lamp when the conveyor motor is running.
6. **Rung 6 – Fault Indicator:** Activates the fault lamp when the fault latch is set.


## Simulation Testing Results

The PLC control logic was evaluated using 14 documented software simulation checks across three functional areas:

- **Motor Start/Stop Control — 4 checks:** Verified motor start, seal-in operation, stop behaviour and restart control.
- **Overload Fault and Reset — 5 checks:** Verified overload detection, motor shutdown, fault latching, fault indication and reset behaviour.
- **Product Counting and Batch Completion — 5 checks:** Verified sensor-based counting, batch completion at 10 products, automatic motor shutdown and counter reset behaviour.

The recorded simulation checks passed under the tested conditions.

**Testing scope:** OpenPLC software simulation only. No physical PLC, conveyor motor or industrial hardware was tested.

**Detailed test evidence:** [PLC Simulation Test Log](02_Simulation_Test_Results/PLC_Simulation_Test_Log.txt)


## PLC Simulation Screenshots

The following screenshots document the ladder logic implementation and PLC variable configuration:

1. [Motor Start/Stop Control](01_PLC_Screenshots/PLC_Motor_Start_Stop_Control.png)
2. [Overload Fault and Reset](01_PLC_Screenshots/PLC_Overload_Fault_and_Reset.png)
3. [Product Counter and Batch Control](01_PLC_Screenshots/PLC_Product_Counter_Batch_Control.png)
4. [Run and Fault Indicators](01_PLC_Screenshots/PLC_Run_and_Fault_Indicators.png)
5. [PLC Variable Declarations](01_PLC_Screenshots/PLC_Variable_Declarations.png)

These screenshots were captured during development and software simulation using OpenPLC Editor.


## Project Files and Documentation

This repository contains the OpenPLC project files, simulation evidence, and technical documentation.

- **PLC Source Files:** [03_PLC_Source_Files](03_PLC_Source_Files) — OpenPLC project configuration and ladder logic source files.
- **Simulation Test Results:** [02_Simulation_Test_Results](02_Simulation_Test_Results) — Documented functional simulation checks.
- **PLC Screenshots:** [01_PLC_Screenshots](01_PLC_Screenshots) — Ladder logic and variable declaration screenshots.
- **Technical Project Overview (PDF):** [PLC_Project_Overview.pdf](04_Project_Documentation/PLC_Project_Overview.pdf) — Project objective, control logic, simulation results, and conclusions.
- **Technical Project Overview (TXT):** [PLC_Project_Overview.txt](04_Project_Documentation/PLC_Project_Overview.txt) — Plain-text version of the technical documentation.

**Note:** This project demonstrates PLC programming and control logic through software simulation. It has not been validated on physical industrial equipment.


## Technical Skills Demonstrated

Through the development and software simulation of this project, I gained practical experience in:

- **PLC Programming:** Developing ladder diagram logic using OpenPLC Editor.
- **Industrial Control Logic:** Implementing motor start/stop circuits, seal-in logic and interlocks.
- **Fault Handling:** Designing simulated overload protection, fault latching and reset logic.
- **PLC Counters:** Using a CTU counter for product counting and batch completion control.
- **Digital Inputs and Outputs:** Configuring and testing simulated PLC input and output variables.
- **System Testing:** Performing and documenting 14 functional software simulation checks.
- **Technical Documentation:** Preparing ladder logic screenshots, test records and project documentation.

This project provides foundational, simulation-based experience relevant to entry-level PLC, industrial automation and control systems engineering roles.


## Project Conclusion

This project demonstrates the development and software-based testing of an automated conveyor control system using PLC ladder logic in OpenPLC Editor.

The implemented control program combines motor start/stop operation, seal-in logic, overload fault protection, fault reset, product counting, automatic batch completion and status indication.

A total of 14 documented simulation checks were completed to evaluate the control logic under the tested operating conditions.

The project strengthened my foundational understanding of PLC programming, industrial automation sequences, control interlocks, fault handling and systematic testing.

**Future Development:** Potential extensions include an emergency-stop safety design, additional sensors, a human-machine interface (HMI), and validation using physical PLC hardware. These extensions have not been implemented or tested in the current project.


