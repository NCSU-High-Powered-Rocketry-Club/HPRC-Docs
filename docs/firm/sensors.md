# FIRM Sensors
FIRM's purpose is to collect, process, log, and send information about the rocket during flight, and this [data](firm_data.md) comes from sensors. Each sensor on FIRM was chosen for its high accuracy and fast output data rate (ODR).

## ICM45686
The main accelerometer and gyroscope of FIRM is the ICM45686. This device by TDK InvenSense is called an Inertial Measurement Unit (IMU) and combines a 3-axis accelerometer and 3-axis gyroscope into a single package. This is the sensor with the biggest impact on the data quality, due to the importance of acceleration and angular rate in estimating the state of the rocket at any time. Rockets also experience high acceleration and angular rates during the motor burn phase of flight, so high ranges were required. 

Specs Overview:
- Full range: $\pm 32g$, $\pm 4000 \frac{deg}{s}$
- Maximum ODR: $6400$ Hz
- Supported Protocols: SPI, I2C, I3C
- Output Resolution: $20$ bits
- Initial Zero-Rate/Zero-g offset: $\pm 0.3 \frac{deg}{s}$, $\pm 0.01g$
- Accelerometer Noise Spectral Density: $110 \mu g/\sqrt{Hz}$
- Gyroscope Noise Spectral Density: $0.005 \frac{deg}{s}/\sqrt{Hz}$

Unfortunately, the ICM45686 has two major issues. The 32g range is misleading; even when configured correctly, the sensor will not measure higher than around 19g on each axis. It is also increasingly difficult to source due to extremely high demand. Despite this, the ICM45686 is the highest-performance consumer-grade IMU available given FIRM's requirements, making it worth using despite availability concerns. FIRM uses SPI to communicate with this sensor.

## BMP581
To record pressure and temperature, the BMP581 was chosen for its high accuracy and brand familiarity. Bosch is probably the biggest developer of consumer-grade barometric pressure sensors, and the BMP581 is their newest high-accuracy model. It also boasts an impressive maximum ODR. The BMP581 records temperature, which can be useful at times, but note that the recorded temperature is higher than the surrounding air due to the circuit board itself being warm.

Specs Overview:
- Pressure operating range: $30$ - $125$ kPa
- Temperature operating range: $-40$ - $85 \degree C$
- Maximum ODR: $480$ Hz
- Supported Protocols: SPI, I2C, I3C
- Output Resolution: $24$ bits
- Absolute Accuracy: $\pm 30$ Pa
- Relative Accuracy ($1$ kPa steps): $\pm 0.4$ Pa
- Relative Accuracy ($10$ kPa steps): $\pm 6$ Pa

FIRM uses SPI to communicate with this sensor.

## MMC5983MA
MEMSIC's MMC5983MA is the chosen magnetometer for FIRM, selected for its high accuracy and high ODR. From a code perspective, this sensor is relatively simple and has very few configuration registers compared to the two sensors listed above. Note that for this sensor to operate as intended, you must perform the SET/RESET function periodically (on startup, at minimum) as the datasheet describes. Failure to do this will cause the device to become polarized over time and record useless data.

Note that for the specifications listed below, $G$ is in units of Gauss, not gravitational acceleration, $g$

Specs Overview:
- Full Range: $\pm 8G$
- Maximum ODR: $1000 Hz$
- Supported Protocols: SPI, I2C
- Output Resolution: $18$ bits
- Total RMS Noise: $0.6 mG$

The Total RMS Noise specification is dependent on the selected bandwidth. FIRM uses SPI to communicate with this sensor.

## ADXL371
While the ICM45686 has a high maximum acceleration range, some rockets exceed 32g during motor burn. This causes the sensor to "saturate" and be unable to read the true acceleration achieved during flight. The ADXL371 from Analog Devices acts as a backup accelerometer; while it has much lower resolution and higher noise, it offers an extremely high acceleration range. Referred to as the "high-g accelerometer," it was included on FIRM to allow precision on the main IMU while handling the brief motor burn phase. Note that the ADXL is an accelerometer only, not an IMU; the ICM45686 is the only gyroscope on FIRM.

Specs Overview:
- Full Range: $\pm 200g$
- Maximum ODR: $5120 Hz$
- Supported Protocols: SPI, I2C
- Output Resolution: $12$ bits
- Initial Zero-g Offset: $\pm 1g$
- Noise Spectral Density: $5.5 mg/\sqrt{Hz}$

Note that the initial offset is substantial at $1g$; when looking at data from this sensor while sitting still on a table, expect around $\pm 2g$ of noise and be aware it will *not* be centered around $[0, 0, 1]g$. FIRM uses SPI to communicate with this sensor.

## INA219
For monitoring FIRM's power, we chose Texas Instruments' INA219 to record the input voltage and current. Since voltage and current do not need to be sampled as quickly as other sensors, they are only collected at around 10 - 20 Hz.

Specs Overview:
- Full Range: $0 - 26V$
- Maximum ODR: $1880 Hz$ (for max resolution)
- Supported Protocols: I2C
- Output Resolution: $12$ bits
- Voltage Offset: $\pm 10 \mu V$

FIRM uses I2C to communicate with this sensor.