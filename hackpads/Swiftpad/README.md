# SwiftPad — a minimal productivity macropad

> A compact 9-key macropad with a rotary encoder and OLED, built to speed up an iPad-centred workflow.

## Stack

- **Firmware:** [KMK](https://github.com/KMKfw/kmk_firmware) (CircuitPython / Python)
- **Microcontroller:** Seeed XIAO RP2040
- **Hardware:** custom PCB + 3D-printed case (see `PCB/` and `CAD/`)

## Description

SwiftPad ("Swift") is a small macropad I built to make my workflow easier, mainly paired with my
iPad. It keeps a minimal footprint while still giving quick access to shortcuts, layers, and
media/scroll control through a rotary encoder.

## Features

- **Rotary encoder** with a built-in push switch for changing layers.
- **0.91" OLED screen** — small, but enough to show the active layer/status.
- **9 MX-style key switches.**
- **4 orange single-colour LEDs** (low-powered, currently unused — reserved for future use).
- **Truchet-tiles case pattern** (pattern credited to the creator of Macroboard).
- Runs on **KMK firmware**, so the layout is configured in Python.

## Bill of Materials

| Part | Qty |
|------|-----|
| Seeed XIAO RP2040 | 1 |
| MX-style key switches | 9 |
| Rotary encoder (with push switch) | 1 |
| 0.91" I2C OLED display | 1 |
| Orange LEDs | 4 |
| Custom PCB (see `PCB/`) | 1 |
| 3D-printed case (see `CAD/`) | 1 |

## How to Build / Flash

1. **Fabricate the hardware** from the design files in `PCB/` (gerbers/schematic) and `CAD/`
   (case), then solder the switches, encoder, OLED, and LEDs to the board.
2. **Install CircuitPython** on the XIAO RP2040.
3. **Add KMK** to the board's `lib/` folder (see the KMK docs).
4. **Copy the firmware** — drop `firmware/code.py` onto the board's `CIRCUITPY` drive. It loads on
   boot; edit it to remap keys or layers.

## Images

![SwiftPad build photo 1](https://cloud-362soi2pi-hack-club-bot.vercel.app/0image.png)
![SwiftPad build photo 2](https://cloud-362soi2pi-hack-club-bot.vercel.app/1image.png)
![SwiftPad build photo 3](https://cloud-362soi2pi-hack-club-bot.vercel.app/2image.png)
![SwiftPad build photo 4](https://cloud-362soi2pi-hack-club-bot.vercel.app/3image.png)
![SwiftPad build photo 5](https://cloud-362soi2pi-hack-club-bot.vercel.app/4image.png)

---

_Built for the [Hack Club](https://hackclub.com/) Hackpad YSWS._
