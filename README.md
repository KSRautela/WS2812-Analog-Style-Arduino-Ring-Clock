# WS2812 Analog-Style Arduino Ring Clock

An Arduino-powered LED ring clock that displays time in an **analog style** using a WS2812 (NeoPixel) LED ring. The clock includes multiple display modes, a 24-hour alarm, a countdown feature, and a demo mode. Hours, minutes, and seconds are shown in different colors using the LED ring — all built with easily sourced components and Arduino code. :contentReference[oaicite:0]{index=0}

## Features

- 🕒 **Analog-style clock display** using a 60-LED NeoPixel ring  
- ⏰ **24-hour alarm** with visual indication  
- ⌛ **Countdown timer** mode  
- 💡 **Multiple visual modes** and demo effects  
- 🔧 Adjustable via **rotary encoder with push button**  
- ⚙️ Runs on Arduino (Nano or equivalent)  
- 📦 3D-printed enclosure optional  

## Components

You’ll need the following hardware: :contentReference[oaicite:1]{index=1}

- Arduino Nano microcontroller  
- WS2812 NeoPixel ring (60 LEDs)  
- DS3231 Real Time Clock (RTC) module  
- Rotary encoder with push button  
- 220 Ω resistor  
- 2 × 1N4007 diodes  
- Slide switch  
- 5 V / 3 A power supply  
- Optionally: 3D-printed ring mount or case

## Software Requirements

- **Arduino IDE** (or compatible environment)  
- Libraries:  
  - FastLED  
  - RTClib  
  - Bounce (for button debouncing)  
  - Encoder (for rotary input)  

## Wiring Overview

Connect the components as shown in the schematic diagram (refer to your project folder’s schematic). Typical connections include:  

- WS2812 data pin → Arduino digital pin (configured in code)  
- RTC SDA / SCL → Arduino A4 / A5  
- Rotary encoder → two digital pins + push button  
- Power and ground must be shared across components  

## How It Works

1. **Bootup** – After power on, the clock defaults to the main display.  
2. **Clock Display** – Shows current time using colored LEDs:  
   - Hours, minutes, and seconds are distinguished by color.  
3. **Mode Change** – Rotate the encoder to switch between different display modes.  
4. **Time & Alarm Setting** – Press and hold the encoder button to enter setting modes.  
5. **Countdown Timer** – Set and start a countdown from the menu.  
6. **Demo Mode** – Shows preset visual patterns automatically. :contentReference[oaicite:2]{index=2}

## Installation

1. Clone this repository.  
2. Open the Arduino sketch (`.ino`) in the Arduino IDE.  
3. Install all required libraries via the Library Manager.  
4. Connect your board and upload the sketch.  
5. Power the system with a stable 5 V source capable of supplying enough current for the LEDs.

## Use & Controls

| Action | Result |
|--------|--------|
| Click encoder once | Change display mode |
| Long press encoder | Enter time/alarm setting mode |
| Rotate encoder | Adjust values |
| Long press in countdown | Start/reset countdown |

_(Control behavior may vary slightly depending on firmware settings.)_ :contentReference[oaicite:3]{index=3}

