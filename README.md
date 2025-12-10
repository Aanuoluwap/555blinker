# 555 Blinker & ESP32 Projects

This repository contains electronics design projects created using KiCad.

## Projects

### 1. 555 Blinker (Root)

A classic Astable Multivibrator circuit using the NE555 timer IC.

**Components:**
- **U1**: NE555D (SOIC-8)
- **R1**: 1kΩ Resistor (1206)
- **R2**: 68kΩ Resistor (1206)
- **R3**: 8.2kΩ Resistor (1206)
- **C2**: 10µF Tantalum Capacitor (EIA-3216-18)
- **D1**: LED (1206)
- **J1**: 1x02 Pin Header (2.54mm)

**Function:**
The circuit is configured as an astable multivibrator, flashing the LED (D1). The frequency is determined by R2, R3, and C2.

### 2. Project 2: ESP32 Build

Located in `Priject_2__ESP32_build/`.

This project involves an ESP32 microcontroller.
*(Further details to be added)*

## Directory Structure

```
.
├── 555 blinker.kicad_pro    # 555 Blinker Project File
├── 555 blinker.kicad_sch    # Schematic
├── 555 blinker.kicad_pcb    # PCB Layout
└── Priject_2__ESP32_build/  # ESP32 Project Folder
```

## Tools Used

- **KiCad EDA**: [https://www.kicad.org/](https://www.kicad.org/) (Version 8.0 or later recommended)

## License

[Add License Here]
