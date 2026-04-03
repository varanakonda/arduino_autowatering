# Arduino Autowatering System 🌱

Automated plant watering controller built with Arduino UNO R3.
Waters plants for **10 seconds every 20 minutes**, with live 
countdown on LCD display.

## Hardware

| Component | Model |
|---|---|
| Microcontroller | Arduino UNO R3 |
| Display | LCD Shield 1602 (16x2) |
| Real-time clock | RTC DS1302 |
| Output | Relay module (active LOW) |

## How it works

1. Relay activates → waters for 10 seconds with LCD countdown
2. LCD shows loop number and remaining delay (MM:SS)
3. Cycle repeats every 20 minutes
4. Serial debug output available (set `is_debug = true`)

## Wiring
LCD Shield:  RS=8, EN=9, D4=4, D5=5, D6=6, D7=7
Relay:       Pin 3 (active LOW — HIGH = disabled)

## Flash & Run

1. Open `autowatering.ino` in Arduino IDE
2. Select board: **Arduino UNO**
3. Upload → done

## Notes

- Relay is **active LOW**: `LOW` = water on, `HIGH` = water off
- Loop counter displayed on LCD — useful for uptime tracking
- Timer via `millis()` is prepared in code (commented out) — 
  can be enabled for precise interval control without blocking

## Author

[@varanakonda](https://github.com/varanakonda)
