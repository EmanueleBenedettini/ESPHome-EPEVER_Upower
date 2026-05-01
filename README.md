# ESPHome-EPEVER_Upower

Code and instructions for the integration of EPEVER Upower inverters in Home Assistant.

## Configuration

In `upower.yaml`, update the following values to match your setup:

- **Line 19**: `YOURAPIENCRYPTIONKEY` - Your API encryption key
- **Line 22**: `YOUROTAPASSWORD` - Your OTA password
- **Line 31**: `YOURPASSWORD` - Your device password

## Firmware Size

The code is optimized to fit on an ESP01_1M module while maintaining OTA update capability.

## Board Design

A custom PCB design is included (created with Eagle). To manufacture your board:

1. Go to a site like [jlcpcb.com](https://jlcpcb.com)
2. Upload the `Gerber.zip` file

### Components to Solder

| Designator | Value | Package |
|---|---|---|
| R5, R6 | 3.3kΩ | M1206 |
| R1, R2 | 10kΩ | M1206 |
| R4 | 120Ω | M1206 |
| U2 | AMS1117-3.3 | SOT229P700X180-4N |
| Q1 | 2N7002 N-Channel MOSFET | SOT23 |
| IC1 | MAX485 | SO08 |
| C1, C2 | 100µF | 6mm diameter |

### Notes

- **U1** (ESP01): In most cases, this does not need to be soldered. It should fit snugly in the socket.
