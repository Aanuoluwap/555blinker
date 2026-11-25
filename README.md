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

### 2. Project 2: ESP32 Build ✅ Complete

Located in `Priject_2__ESP32_build/`.

A compact 2-layer ESP32 temperature & humidity sensor board (55.3 × 34.5 mm). An ESP32-WROOM-32 module reads an AM2302 (DHT22) sensor, powered from a 2-pin input through an AMS1117-3.3 regulator. The module's PCB antenna overhangs the board edge, as Espressif recommends, so there is no copper beneath it.

**Components:**
- **U2**: ESP32-WROOM-32 module
- **U1**: AMS1117-3.3 LDO regulator (SOT-223)
- **U3**: AM2302 / DHT22 temperature & humidity sensor, data on **IO15**
- **R1**: 4.7kΩ pull-up on the sensor data line (1206)
- **R2, C3**: 10kΩ pull-up + 1µF cap on **EN** (reset RC)
- **R3**: 10kΩ pull-up on **IO0** (boot strap)
- **SW1 / SW2**: RESET and BOOT tactile buttons (TL3342)
- **C1 / C2**: 10µF input and 22µF output tantalum capacitors (EIA-3216-18)
- **J1**: 1x02 power input header (pin 1 = VIN, pin 2 = GND)

**Design status:**
- ERC: 0 errors, 0 warnings
- DRC: 0 errors, 0 unconnected items, PCB matches schematic. The only warnings are for the module's silkscreen, which is intentionally clipped where the antenna overhangs the edge.
- Solid GND pour on both layers with stitching vias; 0.5–0.6 mm power tracks, 0.25 mm signal tracks, 0.2 mm clearance (fits JLCPCB standard 2-layer rules)

**Manufacturing files** (`Priject_2__ESP32_build/fab/`):
- `Priject_2__ESP32_build-gerbers.zip`: Gerbers + Excellon drill files, ready to upload to a PCB fab
- `Priject_2__ESP32_build-BOM.csv`: bill of materials
- `Priject_2__ESP32_build-top-pos.csv`: pick-and-place positions for assembly

To flash the ESP32: hold **BOOT** (SW2), tap **RESET** (SW1), then release BOOT.

## Directory Structure

```
.
├── 555 blinker.kicad_pro    # 555 Blinker Project File
├── 555 blinker.kicad_sch    # Schematic
├── 555 blinker.kicad_pcb    # PCB Layout
└── Priject_2__ESP32_build/  # ESP32 Project Folder
    ├── Priject_2__ESP32_build.kicad_sch
    ├── Priject_2__ESP32_build.kicad_pcb
    └── fab/                 # Gerber zip, BOM, placement file
```

## Tools Used

- **KiCad EDA**: [https://www.kicad.org/](https://www.kicad.org/) (Version 8.0 or later recommended)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
