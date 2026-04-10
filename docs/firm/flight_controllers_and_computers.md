# Flight Controller or Flight Computer?
Although these terms are used interchangebly, there is a distinction to be made between flight controllers and flight computers. 

## Flight Controllers
In general, flight controllers are usually small devices programmed on a microcontroller, designed to run a very tight loop of general-purpose data collection code.

Here are common examples of microcontrollers that are used in flight controllers:
- Arduino
- STM32
- ESP32

Flight controller software generally revolves around collecting sensor data, logging data, and/or transmitting data. (using USB, radio, UART, etc.) The code is designed to loop quickly to help ensure that dependent systems can respond to real-time events fast enough.

A common example of a flight controller is an altimeter, which has code running on a small microcontroller to read sensor data and determine in real-time when to fire the pyro channels to separate the rocket and deploy parachutes.

## Flight Computers
Flight computers are devices that use a general-purpose operating system like Linux or Debian, and are designed to facilitate and command specific mission logic.

You might find these devices used for flight computers:
- Raspberry Pi
- NVIDIA Jetson
- Radxa ROCK

Because flight computers run on commonly-used operating systems, they make it more comfortable to work with and debug on. Unlike flight controllers that run a defined set of code immediately when powered on, flight computers must be told what program to run, enabling you to write test scripts to help debug on the hardware.