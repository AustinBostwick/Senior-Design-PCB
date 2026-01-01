# Senior Design Project Summary

## Project Overview

For my senior design project, I worked with one other person to create a **handheld electrochemical diagnostics device**. The project consisted of two major components:

1. A **printed circuit board (PCB)** with high-voltage drivers used to control liquid movement
2. A **glass chip** used for electrochemical diagnostics

---

## Glass Chip Fabrication

The glass chip was created using a process called **photolithography**. Photolithography involves printing a pattern onto a material using a photosensitive layer, followed by metal evaporation onto the chip. Any excess metal is then washed away.

This fabrication process required **over nine months** to develop a fully functional chip.
![Glass chip fabrication process](Final%20Diagram.jpg)

### Glass Chip Composition
- Chromium
- Silver
- SU-8
- ITO Glass
- Two layers of double-sided tape

## PCB Design and Control System

The PCB was designed and produced alongside the glass chip. It was built around an **Arduino-based system**.

A **high-voltage driver circuit** was integrated into the PCB and controlled via an **SPI communication line** connected directly to the Arduino.
<p align="center">
  <img src="https://github.com/AustinBostwick/Senior-Design-PCB/blob/main/PCB%20Diagram.png">
</p>

My technical expertise in high-voltage PCB design is demonstrated by my development of an adjustable boost converter for an Electrowetting-on-Dielectric (EWOD) system, which successfully stepped up a 3–5 V input to over 300 V DC. I integrated a serial-to-parallel shift register using MOSI signals to control high-voltage output pins, utilizing logic level shifters to bridge the communication gap between the 3.3 V Teensy 4.0 microcontroller and 5 V hardware requirements. To ensure precision, I designed a resistor feedback network with a multiplexer that allowed for fine-tuned voltage adjustments necessary for creating the electric fields that drive liquid movement.

In terms of layout, I applied rigorous signal integrity principles to minimize noise and ensure system stability. This included calculating specific trace widths to accommodate higher current flows and utilizing dedicated ground and power planes to act as decoupling capacitance for smoothing the main power signal. I specifically focused on the physical layout of the boost converter section to mitigate electromagnetic interference and ringing—a challenge I identified and solved by testing various makes and models of inductors and MOSFETs during the prototyping phase.

My debugging process is systematic and data-driven, involving both hardware-level troubleshooting and architectural optimization. For the second iteration of the PCB, I significantly improved serviceability by adding numerous test points and migrating the architecture to a Teensy 4.0, which streamlined the programming environment and allowed for live serial debugging. When the output voltage exceeded the limits of standard lab oscilloscopes, I utilized multimeters to accurately validate outputs of up to 311 V DC. These iterative design choices resulted in a verified high-voltage system that operated reliably within the intended 60–126 V range, providing a stable foundation for the device's core functionality.


---

## Closing Statement

This document provides a brief overview of the project. I would be happy to discuss the project further over the phone or via email.
