# OpenPLC CrowPanel - User Manual

This version is designed for **CrowPanel Advanced ESP32-P4, 7-10 inch models, hardware version 1.2**. It presents a complete compressed-air station with live equipment behavior, controls, trends, and alarms. All process values are generated and updated directly on the panel, so the system is ready to use immediately after startup.

## Getting started

1. Wait for the startup presentation to appear.
2. Select **SHOW DEMO** to open the live HMI.
3. Use the bottom navigation bar to switch between **Overview**, **Equipment**, **Controls**, **Trends**, and **Alarms**.
4. Use the gear icon in the top-right corner to adjust the panel settings.

The values change continuously. Compressors start and stop according to air demand, while pressure, power, temperature, motor current, runtime, equipment states, trends, and alarms update automatically.

## What you can do

- Monitor the complete station and its current operating state.
- Open individual equipment to inspect detailed measurements.
- Switch compressors between automatic and manual operation.
- Start or stop a compressor manually.
- Inject a sensor fault to observe alarm behavior.
- Follow live values on rolling trend charts.
- Review active alarms and reset them.
- Adjust screen brightness, audio volume, and automatic sleep time.

## Screens

### Overview

Use **Overview** for a quick summary of the whole station. It shows system health, active alarms, running equipment, equipment states, network pressure, air demand, and total power.

### Equipment

Use **Equipment** to inspect a specific asset. Select a compressor, dryer, or receiver to see its available measurements and states, including details that are not shown on Overview.

### Controls

The Controls page contains the available operator commands:

- **Automatic mode** lets the system start or stop a compressor according to air demand.
- **Run command** starts or stops a compressor when automatic mode is disabled.
- **Inject sensor fault** makes temperature and current readings unreliable and creates an alarm.
- **Reset all alarms** clears resettable alarms and removes injected sensor faults.

Control changes are applied immediately and the rest of the interface updates to match the new system state.

### Trends

Trends display rolling charts for numeric process values. Each chart shows its equipment source, metric, current value, Y-axis range, and approximately the latest 60 seconds of history.

### Alarms

Alarms show each active condition with its source, reason, and severity. The system can report sensor faults, high compressor temperature, and high receiver pressure. After an alarm is reset, it can appear again if the condition that caused it is still active.

## System settings

Select the gear icon to open **System** settings. The following options are available:

- **Brightness** - adjust the display brightness from 1% to 100%.
- **Volume** - adjust the panel audio level from 0% to 100%.
- **Sleep after** - disable automatic sleep or select 1, 3, 5, 10, or 30 minutes, or 1 hour.

Changes are applied immediately and saved for the next startup. Select **Back** to return to the HMI.

## Station equipment

- **Compressor 1, 2, and 3** produce compressed air and report operating state, discharge temperature, motor current, accumulated runtime, and alarm status.
- **Air Dryer** removes moisture and runs whenever at least one compressor is operating.
- **Air Receiver** stores compressed air and helps stabilize pressure as demand changes.
- **Air Network** represents the distribution system and provides network pressure, air demand, and total power.

## System logic

Air demand changes automatically over time. In automatic mode, compressors are dispatched as demand rises and are stopped as demand falls. Running compressors add air to the receiver, consume power, warm up, and accumulate operating hours. The dryer follows the compressor operating state, while receiver and network pressure respond to the balance between supply and demand.

Manual mode gives the operator direct control of an individual compressor. Fault injection and alarm reset make it possible to check how abnormal conditions are presented across Overview, Equipment, Trends, and Alarms.

## Things to try

1. Watch automatic compressor dispatch as air demand changes.
2. Compare compressor temperature, current, and runtime in **Equipment**.
3. Disable automatic mode for one compressor and use its **Run command**.
4. Enable **Inject sensor fault** and inspect the result on every screen.
5. Use **Reset all alarms**, then confirm that the active alarm list clears.
