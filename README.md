# RP2040 Board

A custom-designed RP2040 development board built for expanded storage, improved power delivery, and practical usability in embedded and DIY CNC applications.

---

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

(<img width="1779" height="1238" alt="image" src="https://github.com/user-attachments/assets/17c60ec4-21b2-4e94-b2b9-38b5601b4ae7" />)
(<img width="425" height="867" alt="Screenshot 2026-04-14 121702" src="https://github.com/user-attachments/assets/0ccb834a-0bc2-49e2-bfba-cd1b4306bee7" />)
(<img width="511" height="872" alt="Screenshot 2026-04-14 121847" src="https://github.com/user-attachments/assets/7f866901-f4d2-4c7f-ad0b-941493905d06" />)

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
