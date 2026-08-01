# Automated-Tank-Process-Control-System
Designed and simulated an industrial tank process using CODESYS and Factory I/O. The PLC monitors tank level and discharge flow using analog process variables (PV) and setpoints (SP), while operator controls manage fill, discharge, emergency stop, and system reset functions through ladder logic.

---

## Overview
This project simulates an industrial tank process using **CODESYS** and **Factory I/O**, demonstrating PLC-based process automation and closed-loop control. The PLC continuously monitors tank level and discharge flow using real-time process variables (PV) and compares them to operator-defined setpoints (SP).

Custom ladder logic implements an **error-based control algorithm**, continuously calculating the difference between the process variable and setpoint to modulate a **0–100% discharge valve**. This enables the system to automatically regulate tank level and discharge flow without relying on a built-in PID controller.

The system also includes operator controls for fill, discharge, emergency stop, and system reset, along with process interlocks to ensure safe and reliable operation. Communication between CODESYS and Factory I/O is established using **Modbus TCP/IP**, providing real-time interaction between the PLC logic and the simulated process.

---

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

---

## Technologies

- **CODESYS**
- **Factory I/O**
- **Modbus TCP/IP**
- **IEC 61131-3 Ladder Diagram (LD)**

---

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

### Inputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IX20.0 | At Exit | Retroreflective Sensor | Detects when product exits the conveyor system |
| %IX20.1 | Start | White Pushbutton | Activates the automatic conveyor sorting system |
| %IX20.2 | Stop | Gray Pushbutton | Deactivates the automatic conveyor sorting system |
| %IX20.3 | Reset | Blue Pushbutton | Resets the product sorting counter |

### Outputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QX20.0 | EntryConveyor | Conveyor Motor | Controls entry conveyor |
| %QX20.1 | StopBlade | Pneumatic Stopper | Ensures product positioning prior to sorting |
| %QX20.2 | ExitConveyor | Conveyor Motor | Controls exit conveyor |
| %QX20.3 | Sorter1Turn | Sorting Conveyor Motor | Controls product 1 diversion |
| %QX20.4 | Sorter1Belt | Conveyor Motor | Controls product 1 conveyor |
| %QX20.5 | Sorter2Turn | Sorting Conveyor Motor | Controls product 2 diversion |
| %QX20.7 | Sorter2Belt | Conveyor Motor | Controls product 2 conveyor |
| %QX20.8 | Sorter3Turn | Sorting Conveyor Motor | Controls product 3 diversion |
| %QX21.0 | Sorter3Belt | Conveyor Motor | Controls product 3 conveyor |
| %QX21.1 | StartLight | White Pilot Light | Indicates system start |
| %QX21.2 | StopLight | Gray Pilot Light | Indicates system stop |
| %QX21.3 | ResetLight | Blue Pilot Light | Indicates counter reset operation |

### Register Inputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Counter1 | Digital Display | Displays product 1 sorted item count |
| %QW1 | Counter2 | Digital Display | Displays product 2 sorted item count |
| %QW2 | Counter3 | Digital Display | Displays product 3 sorted item count |

### Holding Registers
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IW0 | VisionSensor | Vision Sensor | Detects and temporarily stores product color and type |
