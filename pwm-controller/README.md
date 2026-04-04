# PWM Controller Board
![KiCad](https://img.shields.io/badge/KiCad-design-blue)
![PCB](https://img.shields.io/badge/PCB-prototype-orange)
![Raspberry%20Pi](https://img.shields.io/badge/Raspberry%20Pi-compatible-red)
![License](https://img.shields.io/badge/License-MIT-green)

This is a simple PWM fan controller with optocoupler input.

To keep the design compact and allow single-sided PCB etching, solder pads are used for wiring.

A ZIP archive containing Gerber files is included for PCB fabrication.

## Solder Pads

- J1 → +5V input  
- J2 → FAN + output  
- J3 → PWM signal input  
- J4 → GND  

## Wiring

- Connect J1 directly to Raspberry Pi +5V (Header pin 2 or 4, not a GPIO pin)
- Connect J2 to the positive terminal of the fan
- Connect J3 to Raspberry Pi GPIO18 (Header pin 12)
- Connect J4 to GND

## Notes

The electrical design is relatively robust and supports a wide input range.

- Input voltage: up to 24 V / 1.5 A  
- PWM input signal: 5 V to 12 V compatible  

This design can also be used for other applications.

## Recommended operating limits

| Voltage | Max Current |
|---------|------------|
| 5 V     | 3 A        |
| 9 V     | 2.5 A      |
| 12 V    | 2 A        |
| 15 V    | 1.8 A      |
| 24 V    | 1.5 A      |
