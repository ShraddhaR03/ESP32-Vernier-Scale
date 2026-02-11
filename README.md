   # ESP32 Digital Vernier Scale

This project interfaces an ESP32 with a 24-bit Digital Vernier Scale to provide high-precision measurements displayed on an OLED screen.

## Features
- **Dynamic Direction Toggle**: Wire connected to **D5** (GPIO 5). 
  - Touching **GND**: Measurement increases.
  - **Open**: Measurement decreases.
- **Auto-Sync**: Automatically calibrates to target 'D' on startup to prevent garbage values.
- **Bluetooth Control**: Update target distance (D) and Error tolerance (Err) via Bluetooth Serial.
- **Symmetric Tolerance**: Visual feedback via LEDs when measurement is within `D ± Err`.

## Hardware Pinout
| Component | ESP32 Pin |
|-----------|-----------|
| Scale CLK | GPIO 18   |
| Scale DAT | GPIO 19   |
| Toggle Wire| GPIO 5    |
| Green LED | GPIO 4    |
| Red LED   | GPIO 2    |
| OLED SDA  | GPIO 21   |
| OLED SCL  | GPIO 22   |

## Usage
1. Press `#` on the keypad to set the current physical position as the reference point for value `D`.
2. Use the keypad to edit target distance and error thresholds.
