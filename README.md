# nRFBox Firmware for WiFi Jammer, Bluetooth & Network Analyzer

## Overview
nRFBox is a powerful firmware designed for **WiFi jamming, Bluetooth analysis, and network scanning**. It leverages **nRF-based hardware** to execute wireless security assessments, penetration testing, and signal analysis.

## Features
- **WiFi Jammer**: Disrupts WiFi networks within range.
- **Bluetooth Scanner**: Detects and analyzes Bluetooth devices.
- **Network Analyzer**: Scans and monitors nearby networks.
- **Customizable Firmware**: Modify and extend functionalities.

## Installation
### **Prerequisites**
- Compatible **nRF-based hardware** (e.g., nRF52, nRF24, ESP8266 for WiFi capabilities).
- Flashing tool (e.g., **nRFConnect, OpenOCD, or J-Link**).
- Serial monitor software (e.g., **PuTTY, CoolTerm, or minicom**).

### **Flashing the Firmware**
1. Download the latest firmware release: **[3_nRFBox_v2.5.bin](Insert GitHub Link Here)**.
2. Connect the nRF device via **USB or SWD (Serial Wire Debug)**.
3. Use the following command to flash:
   ```bash
   nrfjprog --program 3_nRFBox_v2.5.bin --chiperase --reset
   ```
4. Verify the installation by checking the serial output:
   ```bash
   screen /dev/ttyUSB0 115200
   ```
5. The device should boot into **nRFBox mode**.

## Usage
- **WiFi Jamming**:
  - Activate using the command: `wifi_jam start`
  - Stop with: `wifi_jam stop`
  
- **Bluetooth Scanning**:
  - Scan for nearby devices: `bt_scan`
  - Get device details: `bt_info [MAC]`
  
- **Network Analysis**:
  - List available networks: `net_scan`
  - Monitor a specific network: `net_monitor [SSID]`

## Disclaimer
🚨 **For educational and security research purposes only!** Unauthorized use of this tool for malicious activities is illegal. The developers are **not responsible** for any misuse.

## Contributing
Feel free to **fork this repository** and submit **pull requests** with improvements. Contributions are always welcome!

## License
This project is open-source and available under the **MIT License**.

