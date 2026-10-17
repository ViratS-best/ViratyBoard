# ViratyBoard

A RP2040 board! My second ever PCB!!!

[![View PCB on KiCanvas](https://hack.club/pcb-badge)](https://kicanvas.org/?repo=https://github.com/ViratS-best/ViratyBoard)

<img width="459" height="528" alt="image" src="https://github.com/user-attachments/assets/52d1dd4a-474a-41f9-a41c-60574e132774" />
<img width="813" height="1143" alt="image" src="https://github.com/user-attachments/assets/28f2eee1-4f94-4383-abea-95747b253da9" />

## Features

* **Dual Power Input:** Accepts both USB power and a battery connection. Plugging in USB automatically turns the MOSFET off to completely disconnect the AA batteries so they don't get accidentally charged or drained.
* **RP2040 MCU:** Built around the Raspberry Pi RP2040 microcontroller with decoupling capacitors, crystal oscillator, and flash storage.
* **4-Layer Stackup:** Designed with a 4-layer configuration for clean power and signal routing.

## Project Structure

```text
├── README.md
├── devboard.kicad_pcb
├── devboard.kicad_pro
├── devboard.kicad_sch
├── devboard.zip         # Fabrication files
├── bom.csv
└── submit.ino
```
| Part | Qty | Unit | Total | Vendor |
| :--- | :---: | :---: | :---: | :--- |
| [PCB Devboard](https://www.jlcpcb.com) | 1 | $66.63 | $66.63 | [JLCPCB](https://www.jlcpcb.com) |
| Tax & shipping for the whole order | – | – | $0.05 | – |
| **Total** | | | **$66.68** | |
