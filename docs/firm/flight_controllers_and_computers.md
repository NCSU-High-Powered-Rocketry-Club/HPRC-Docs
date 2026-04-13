# Flight Controller or Flight Computer?
Although these terms are used interchangeably, there is an important distinction between flight controllers and flight computers. 

## Flight Controllers
In general, flight controllers are usually small devices programmed on a microcontroller, designed to run a very tight loop of general-purpose [data collection](firm_data.md) code.

Here are common examples of microcontrollers that are used in flight controllers:
- Arduino
- STM32
- ESP32

Flight controller software generally focuses on collecting [sensor](sensors.md) data, logging data, and transmitting data via USB, radio, UART, or similar protocols. The code loops quickly to ensure dependent systems can respond to real-time events fast enough.

A common example of a flight controller is an [altimeter](//docs/recovery/altimeters/altimeters.md), which has code running on a small microcontroller to read sensor data and determine in real-time when to fire the pyro channels to separate the rocket and [deploy parachutes](//docs/recovery/deployment.md).

## Flight Computers
Flight computers are devices that use a general-purpose operating system like Linux or Debian, and are designed to facilitate and command specific mission logic.

You might find these devices used as flight computers:
- Raspberry Pi
- NVIDIA Jetson
- Radxa ROCK

Because flight computers run on commonly used operating systems, they are more comfortable to work with and debug. Unlike flight controllers that run a defined set of code immediately when powered on, flight computers must be told what program to run, enabling you to write test scripts to help debug on the hardware.