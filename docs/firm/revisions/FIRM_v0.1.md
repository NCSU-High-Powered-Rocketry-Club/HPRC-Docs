# FIRM v0.1

This was the first PCB iteration of FIRM, finalized and ordered on October 17, 2025.

[Add pic here]

## Hardware Overview

The following sections describe the microcontroller, sensors, peripherals, and power components.

### Microcontroller and Related Components
- Microcontroller: STM32F405RGT6
- 12 MHz high-speed external crystal
- 32khz low-speed external crystal

### Sensors
- IMU: ICM45686
- Barometer: BMP581
- Magnetometer: MMC5983MA

### Storage
- Main logging storage: Micro-SD
- Device settings storage: W25Q128JV

### Power
- USB-C or PWR/GND pinouts to supply power
- MIC5219 voltage regulator (12V, 500mA max)
