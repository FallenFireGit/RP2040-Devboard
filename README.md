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

# BOM
Designator,Quantity,Value,Component,Footprint,Notes

# --- Microcontroller & ICs ---

U1,1,RP2040,Microcontroller,QFN-56,Main MCU
U2,1,MCP73831-2-OT,LiPo Charger,SOT-23-5,Battery charging IC
U3,1,W25Q64JVZPIQ,Flash Memory,SOIC-8,8MB external flash
U5,1,AP2112K-3.3,Voltage Regulator,SOT-23-5,3.3V regulator

# --- Clock ---

Y1,1,12MHz,Crystal,3225 SMD,Main clock

# --- Capacitors ---

C1 C10,2,1uF,Capacitor,0402,General decoupling
C2 C3 C4 C5 C6 C7 C8 C11 C12 C17,10,0.1uF,Capacitor,0402,Decoupling
C13 C14 C19 C20 C21,5,10uF,Capacitor,0805,Power filtering
C15 C16,2,22pF,Capacitor,0402,Crystal caps
C18,1,0.5uF,Capacitor,0402,Special use
C22,1,100nF,Capacitor,0402,Decoupling

# --- Resistors ---

R1 R2,2,5.1kΩ,Resistor,0603,Pull resistors
R3 R4,2,27.4Ω,Resistor,0402,USB data lines
R5 R11,2,100kΩ,Resistor,0603,Pull-up/down
R6 R9 R14,3,1kΩ,Resistor,0603,General purpose
R7 R17,2,10kΩ,Resistor,0603,Pull-up/down
R8 R12 R13,3,47kΩ,Resistor,0603,General purpose
R10,1,200kΩ,Resistor,0603,Voltage divider
R15,1,2kΩ,Resistor,0603,General purpose

# --- Diodes ---

D1 D3 D4,3,SS14,Schottky Diode,SOD-123,Power protection
D2,1,SB0603WC,Diode,SOD-323,Signal diode

# --- Connectors ---

J1,1,USB-C,Connector,USB-C-SMD,Power + data
J2 J3,2,Pin Header 1x20,Connector,2.54mm,GPIO breakout
J4,1,Pin Header 1x3,Connector,2.54mm,Aux connection
J5,1,MicroSD Slot,Connector,MicroSD,External storage
J6,1,JST-PH 2-pin,Connector,JST-PH,Battery connector

# --- Switches ---

SW1,1,Tactile Switch,Button,SPST,Reset
SW2,1,Slide Switch,Switch,SMD,Power switch
SW3,1,Tactile Switch,Button,SPST,Boot
