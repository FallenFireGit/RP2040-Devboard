# RP2040-Devboard

This project is a fully custom PCB based on the RP2040 microcontroller, designed as an upgraded alternative to standard dev boards like the Raspberry Pi Pico.

The goal was to create a board that is:

More powerful
Easier to use during development
Capable of handling real-world applications (data logging, robotics, etc.)
🔧 Key Features
💾 Storage
8MB Flash (upgraded from 2MB)
MicroSD Card Slot
Supports data logging and large file storage
Can be used for applications like G-code handling
🎛️ Interface & Controls
Boot Button – Easy entry into bootloader mode
Reset Button – Quick system reset during development
Status LED (Bi-color)
Indicates power / charging state
Master Power Switch
Fully cuts power to the board
🔋 Power System
LiPo Battery Support
Onboard charging circuit
~600mA Current Capacity
Supports more demanding peripherals
3.3V Enable Control (3V3_EN)
Allows software-controlled power management
Optimized Power Traces
Wider 3.3V and GND lines for:
Reduced resistance
Lower heat
Improved stability
🧠 Design Decisions
Switched to a higher current voltage regulator for better performance
Removed unnecessary components (like MOSFET-based control) after redesign
Standardized passive components to 0603:
Easier assembly
Cheaper sourcing
Better repairability
🖥️ PCB Design
4-Layer PCB
Dedicated ground plane for cleaner routing
Improved signal integrity and stability
Double-sided component placement
Maximizes space efficiency
Increases design complexity but enables more features
📸 Images

Add your images here (schematic, PCB, 3D views, etc.)

🛠️ Tools Used
PCB Design: (KiCad / Altium / etc — replace with what you used)
Microcontroller: RP2040
Firmware: (if applicable)
