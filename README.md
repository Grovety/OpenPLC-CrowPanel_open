# OpenPLC CrowPanel - Hardware v1.2

This package is for the **CrowPanel Advanced 7" ESP32-P4, hardware version 1.2**. The demo runs entirely on the panel. Wi-Fi, an OPC UA server, and configuration are not required.

## Quick installation

1. [Download the ZIP package](OpenPLC-Crowpanel%20v1.4.zip).
2. Extract the entire ZIP to a folder on your Windows PC. Do not run it from inside the ZIP.
3. Connect the CrowPanel with a **USB data cable**.
4. Close serial monitors and other programs using the panel's COM port.
5. Run `Firmware_Flasher.exe` from the extracted folder.
6. Confirm that the detected COM port belongs to the CrowPanel.
7. Keep the cable connected until `Flashing completed successfully` appears.
8. Press Enter to close the flasher. The panel restarts and opens the demo automatically.

Windows may ask you to confirm the downloaded application. Continue only if the package came from this repository.

## If the panel is not detected

- Make sure the cable supports data, not charging only.
- Try another USB cable or port.
- Close any application using the same COM port.
- Reconnect the panel and run the flasher again.

## Using the demo

The opening presentation explains the architecture. Select **SHOW DEMO** to open the live HMI, then use the bottom bar to switch between Overview, Equipment, Controls, Trends, and Alarms.

Read the [System Overview](SYSTEM_OVERVIEW.md) to understand the station, screens, controls, alarms, and connected OPC UA design.
