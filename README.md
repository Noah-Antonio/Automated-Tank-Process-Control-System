# Automated Tank Process Control System
Designed and simulated an industrial tank process using CODESYS and Factory I/O. Implemented PLC-based closed-loop control with error-based logic to regulate tank level and discharge flow through automatic valve modulation.



## Overview
This project simulates an industrial tank process using **CODESYS** and **Factory I/O**, demonstrating PLC-based process automation and closed-loop control. The PLC continuously monitors tank level and discharge flow using real-time process variables (PV) and compares them to operator-defined setpoints (SP).

Custom ladder logic implements an **error-based control algorithm**, continuously calculating the difference between the process variable and setpoint to modulate a **0–100% discharge valve**. This enables the system to automatically regulate tank level and discharge flow without relying on a built-in PID controller.

The system also includes operator controls for fill, discharge, emergency stop, and system reset, along with process interlocks to ensure safe and reliable operation. Communication between CODESYS and Factory I/O is established using **Modbus TCP/IP**, providing real-time interaction between the PLC logic and the simulated process.



## Features

- PLC ladder logic developed in **CODESYS**
- Industrial process simulation using **Factory I/O**
- Closed-loop tank level and discharge flow control
- Continuous 0–100% discharge valve modulation
- Operator-adjustable tank level and flow rate setpoints (SP)
- Real-time monitoring of process variables (PV)
- Fill, discharge, emergency stop, and system reset controls
- Process interlocks for safe operation
- Real-time process visualization and validation
- Error-based valve control logic for process regulation
  


## Technologies

- **CODESYS**
- **Factory I/O**
- **- Modbus TCP/IP Communication**
- **IEC 61131-3 Ladder Diagram (LD)**



## Engineering Concepts Demonstrated

- PLC Programming
- Process Automation
- Closed-Loop Control
- Error-Based Control Logic
- Analog Instrumentation
- Process Variable (PV) & Setpoint (SP) Control
- Continuous Valve Control
- Ladder Logic Development
- Industrial Communications (Modbus TCP/IP)
- Process Interlocks
- Real-Time Process Monitoring
- Automation System Testing & Validation



## I/O List

### Digital Inputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IX32.0 | Fill_CMD | White Pushbutton | Activates automatic tank fill mode |
| %IX32.1 | Discharge_CMD | Gray Pushbutton | Activates automatic discharge flow control mode |
| %IX32.2 | Reset_CMD | Blue Pushbutton | Resets system operation after emergency stop |
| %IX32.3 | Emergency_Stop | Emergency Stop Button | Stops system operation during emergency condition |

### Digital Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QX32.0 | Fill_Status_Light | White Light Indicator | Indicates active tank fill operation |
| %QX32.1 | Discharge_Status_Light | Gray Light Indicator | Indicates active discharge control operation |
| %QX32.2 | Reset_Status_Light | Blue Light Indicator | Indicates system reset status |

### Analog Inputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IW0 | Level_PV | Level Meter | Measures current tank fluid level |
| %IW1 | Flow_PV | Flow Meter | Measures current discharge flow rate |
| %IW2 | Level_SP | Potentiometer | Sets desired tank fill level setpoint |
| %IW3 | Flow_SP | Potentiometer | Sets desired discharge flow rate setpoint |

### Analog Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Fill_Level_SP_Display | Digital Display | Displays operator-defined tank fill level setpoint |
| %QW1 | Fill_Level_PV_Display | Digital Display | Displays current measured tank fill level |
| %QW2 | Discharge_Flow_SP_Display | Digital Display | Displays operator-defined discharge flow setpoint |
| %QW3 | Discharge_Flow_PV_Display | Digital Display | Displays current measured discharge flow rate |
| %QW4 | Fill_Valve_CMD | Valve | Controls fill valve opening percentage |
| %QW5 | Discharge_Valve_CMD | Valve | Controls discharge valve opening percentage |
