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

### Register Inputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IW0 | Level_PV | Level Meter | Measures current tank fluid level |
| %IW1 | Flow_PV | Flow Meter | Measures current discharge flow rate |
| %IW2 | Level_SP | Potentiometer | Sets desired tank fill level setpoint |
| %IW3 | Flow_SP | Potentiometer | Sets desired discharge flow rate setpoint |

### Register Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Fill_Level_SP_Display | Digital Display | Displays operator-defined tank fill level setpoint |
| %QW1 | Fill_Level_PV_Display | Digital Display | Displays current measured tank fill level |
| %QW2 | Discharge_Flow_SP_Display | Digital Display | Displays operator-defined discharge flow setpoint |
| %QW3 | Discharge_Flow_PV_Display | Digital Display | Displays current measured discharge flow rate |
| %QW4 | Fill_Valve_CMD | Valve | Controls fill valve opening percentage |
| %QW5 | Discharge_Valve_CMD | Valve | Controls discharge valve opening percentage |
