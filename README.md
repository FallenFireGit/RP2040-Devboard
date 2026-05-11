# RP2040 Board

## NOTE TO REVIEWER

I didn’t end up recording a timelapse or keeping super consistent journal entries while working on this. Most of the project was done in longer sessions where I was focused on getting things working rather than documenting everything as I went (documenting is boring, and I got lazy). I realize now that I should’ve tracked progress better, but I’ve tried to reconstruct the main steps and decisions afterward as accurately as possible (In the 12-hour journal entry). In the future, I will remember to document more of my work as I go because I've now learned the importance of documenting. Also, this was my first project ever where I had to document, so now I understand how much I have documented moving forward. 

---

A custom-designed RP2040 development board built for expanded storage, improved power delivery, and practical usability in embedded and DIY CNC applications.

## Overview

This project is a fully custom PCB based on the RP2040 microcontroller, designed as an upgraded alternative to standard dev boards like the Raspberry Pi Pico.

The goal was to create a board that is:

* More powerful
* Easier to use during development
* Capable of handling real-world applications (data logging, robotics, etc.)

---

## Key Features

### Storage

* 8MB Flash (upgraded from 2MB)
* MicroSD Card Slot

  * Supports data logging and large file storage
  * Can be used for applications like G-code handling

---

### Interface & Controls

* Boot Button – Easy entry into bootloader mode
* Reset Button – Quick system reset during development
* Status LED (Bi-color)

  * Indicates power / charging state
* Master Power Switch

  * Fully cuts power to the board

---

### Power System

* LiPo Battery Support

  * Onboard charging circuit
* ~600mA Current Capacity

  * Supports more demanding peripherals
* 3.3V Enable Control (3V3_EN)

  * Allows software-controlled power management
* Optimized Power Traces

  * Wider 3.3V and GND lines for:

    * Reduced resistance
    * Lower heat
    * Improved stability

---

## Design Decisions

* Switched to a higher current voltage regulator for better performance
* Removed unnecessary components after redesign
* Standardized passive components to 0603:

  * Easier assembly
  * Cheaper sourcing
  * Better repairability

---

## PCB Design

* 4-Layer PCB

  * Dedicated ground plane for cleaner routing
  * Improved signal integrity and stability
* Double-sided component placement

  * Maximizes space efficiency

---

## Images

<img width="1779" height="1238" alt="image" src="https://github.com/user-attachments/assets/17c60ec4-21b2-4e94-b2b9-38b5601b4ae7" />
<img width="425" height="867" alt="Screenshot 2026-04-14 121702" src="https://github.com/user-attachments/assets/0ccb834a-0bc2-49e2-bfba-cd1b4306bee7" />
<img width="511" height="872" alt="Screenshot 2026-04-14 121847" src="https://github.com/user-attachments/assets/7f866901-f4d2-4c7f-ad0b-941493905d06" />

---

## Tools Used

* PCB Design: KiCad (or replace with your tool)
* Microcontroller: RP2040

---

## Status

* Schematic Complete
* PCB Layout Complete
* Manufacturing / Testing (Next Step)

---

## Goals

* Create a more capable RP2040 board than standard dev boards
* Support battery-powered applications
* Enable expandability through external storage

---

## Acknowledgments

* Inspired by the Raspberry Pi Pico
* Built as part of Hack Club Stasis

## BOM

Capacitors
* 0.1uF capacitors 402 – 10
* 1uF capacitors 402 – 2
* 10uF capacitors 805 – 5
* 22pF capacitors 402 – 2
* 0.5uF capacitor 402 – 1
* 100nF capacitor 402 – 1

Resistors
* 5.1k resistors 603 – 2
* 27.4 resistors 603 – 2 
* 100k resistors 603 – 2
* 1k resistors 603 – 3
* 10k resistors 603 – 2
* 47k resistors 603 – 3
* 200k resistor 603 – 1
* 2k resistor 603 – 1

Total Price of Passive Components ~ $1.90 (Depends on who you buy it from)

Diodes & Clock ~ $1.16
* SS14 diodes – 3 ~ $0.50 each
* SB0603W diode – 1 ~ $0.40 
* * 12MHz crystal – 1 ~ 0.70

Connectors / I/O ~ $4.75
* USB-C receptacle (HRO TYPE-C-31-M-12) – 1
* 1x20 pin headers (2.54mm) – 2
* 1x3 pin header (2.54mm) – 1
* 1x2 pin JST connector (PH series) – 1
* MicroSD card slot – 1

Switches ~ $1.20
* Push buttons (SPST) – 2
* Slider switch – 1

ICs / Chips 
* RP2040 – 1 $0.92
* MCP73831-2-OT (battery charger) – 1 $0.76
* W25Q64JVZPIQ (flash memory) – 1 $1.44
* AP2112K-3.3 (voltage regulator) – 1 $0.57

ComponentQuantityPrice (Est.)Passives (Capacitors & Resistors)38$1.90Diodes (SS14, SB0603W)4$0.90Clock (12MHz Crystal)1$0.70Connectors / I/O (USB-C, Headers, JST, MicroSD)6$4.75Switches (Push buttons, Slider)3$1.20RP2040 (Microcontroller)1$0.92MCP73831-2-OT (Battery Charger)1$0.76W25Q64JVZPIQ (Flash Memory)1$1.44AP2112K-3.3 (Voltage Regulator)1$0.57TOTAL56$13.14
