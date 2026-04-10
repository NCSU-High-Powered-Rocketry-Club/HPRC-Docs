# Contributing to FIRM
Whether you want work on the hardware design of FIRM, the code that runs on the microcontroller, the front-end website code, or even the CAD design, this page will go over how get started.

## Git
To contribute to FIRM, its important to be familiar with [git](/docs/git/git.md) and [github](/docs/git/github.md), as this is how develop the hardware and the software, and manage new features.

Here's the link to FIRM's GitHub repositories:
- [FIRM](https://github.com/NCSU-High-Powered-Rocketry-Club/FIRM)
- [FIRM-Web-App](https://github.com/NCSU-High-Powered-Rocketry-Club/FIRM-Web-App)
- [FIRM-KiCad](https://github.com/NCSU-High-Powered-Rocketry-Club/FIRM-KiCad)

## Programming Environment Setup
We will assume that you are already slightly familiar with [VS Code](https://code.visualstudio.com/). Both the FIRM repository and the FIRM-Web-App repository will have specific instructions on how to set up the environment.

### FIRM (STM32 and Client)
This repository contains all of the code that gets compiled onto each FIRM device, and is written in C. It also contains FIRM-Client, which handles parsing live FIRM data, file management, and sending commands to the FIRM device. Its core is written in Rust, with libraries for Python and JavaScript/TypeScript.

### FIRM Web App
The FIRM Web App lets users configure the device and view live data directly in the browser. It also hosts the user-end documentation for FIRM. It's written in TypeScript and uses React and Tailwind CSS.

---

If you're unsure which area to start with, look at each repo's Issues page to see what's currently being worked on, and what you think you can help with/would be interested in.

## Hardware Environment Setup
This is for contributors who want to work on the electrical design of the FIRM board itself, using KiCad.

You can follow the setup instructions on the [FIRM-KiCad repo](https://github.com/NCSU-High-Powered-Rocketry-Club/FIRM-KiCad)
