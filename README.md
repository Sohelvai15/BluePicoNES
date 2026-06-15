# BluePicoNES

> BluePicoNES is an open-source DIY retro gaming console based on Raspberry Pi Pico, PicoNES and BlueRetro with Bluetooth, USB and original NES/SNES controller support.

## Features

* NES Emulator (PicoNES)
* Bluetooth Controller Support (BlueRetro)
* Generic USB Controller Support
* Xbox 360 Wired Controller Support
* Xbox One Wired Controller Support
* Genuine NES Controller Support
* Genuine SNES Controller Support
* PS3 Controller Support
* PS4 Controller Support
* Dual Player Support
* HDMI/DVI Video Output
* microSD ROM Storage
* USB-C Power Input
* Custom Clear Case
* Fully Open-Source Hardware Project
* DIY Friendly Design
* Power Switch
* Bluetooth Enable/Disable Switch
## Hardware Used

* Raspberry Pi Pico
* ESP32-WROOM-32
* Adafruit DVI Breakout
* Adafruit MicroSD Breakout
* USB-C PD Power Module
* USB-A Controller Port
* SNES Controller Connector
* Schottky Diode
* Capacitors

## Project Status

✅ Fully Working

## Gallery

Project photos will be added soon.

## Wiring Diagrams

Wiring diagrams will be uploaded soon.

## License

MIT License

# Complete Wiring Table

## Power Connections

| Pico RP2040 | Connection |
|-------------|------------|
| VSYS | USB-C PD 5V Input |
| 3V3 | microSD VCC |
| 3V3 | NES/SNES Controller VCC |
| 3V3 | ESP32 3V3 |
| GND | Common Ground |

---

## microSD Breakout (SPI)

| Pico RP2040 | microSD Breakout |
|-------------|------------------|
| GP2 | CLK |
| GP3 | SI (MOSI) |
| GP4 | SO (MISO) |
| GP5 | CS |
| 3V3 | VCC |
| GND | GND |

---

## NES / SNES Controller Ports

### Player 1

| Pico RP2040 | Signal |
|-------------|--------|
| GP6 | Clock (P1) |
| GP7 | Data (P1) |
| GP8 | Latch (P1) |

### Player 2

| Pico RP2040 | Signal |
|-------------|--------|
| GP9 | Clock (P2) |
| GP10 | Data (P2) |
| GP11 | Latch (P2) |

---

## DVI Breakout

| Pico RP2040 | DVI Signal |
|-------------|------------|
| GP12 | O+ |
| GP13 | O− |
| GP14 | TXC+ |
| GP15 | TXC− |
| GP16 | TX2+ |
| GP17 | TX2− |
| GP18 | TX1+ |
| GP19 | TX1− |
| GND | GND |

---

## USB Host Port

| Pico RP2040 | USB-A |
|-------------|--------|
| TP2 | D− |
| TP3 | D+ |
| VSYS | VBUS (via Schottky Diode) |
| GND | GND |

### Additional Components

- SS14 Schottky Diode
- 100nF Ceramic Capacitor
- 47uF Electrolytic Capacitor

---

## ESP32 BlueRetro Interface

| ESP32 | Pico RP2040 |
|--------|-------------|
| IO5 | GP6 (Clock P1) |
| IO19 | GP7 (Data P1) |
| IO32 | GP8 (Latch P1) |
| IO18 | GP9 (Clock P2) |
| IO22 | GP10 (Data P2) |
| 3V3 | 3V3 |
| GND | GND |

---

## Switches

### Main Power Switch

USB-C PD 5V → Power Switch → Pico VSYS

### Bluetooth Switch

3V3 → Bluetooth Switch → ESP32 3V3

---

## Tested Features

- PicoNES
- BlueRetro
- Bluetooth Controller Support
- Generic USB Controller Support
- Xbox Wired Controller Support
- Genuine NES Controller Support
- Genuine SNES Controller Support
- PS3 Controller Support
- PS4 Controller Support
- Dual Player Support
- HDMI/DVI Output
- microSD ROM Loading
