# Programmable DC-DC Power Supply with I2C Interface

## About
The repository gathers hardware, software, and management artifacts of the power supply development.

## Purpose
Compact Bench Power Supply controllable by [Raspberry Pi Zero 2 W](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/) and powered by the same AC-DC supply with enough power budged (for example, [MEAN WELL RS-35-5](https://www.meanwellusa.com/webapp/product/search.aspx?prod=RS-35)).

<img src="./I2C-PPS Sketch.Usage.png" alt="I2C-PPS Sketch" width="512">

## Specifications
- Controller: Texas Instruments [BQ25758S](https://www.ti.com/product/BQ25758S)
- Input voltage: 5V (4-6V - hardware power good window)
- Input current: up to 5A (hardware limited)
- Output voltage: programmable by I2C in controller defined range (3.3 - 26V)
- Output current: up to 5A (hardware limited)
- Switching frequency: 250kHz

## Components
Using calculator spreadsheets ([BQ25756_DESIGN-CALC-V01X4 (Low, 250).xlsx](BQ25756_DESIGN-CALC-V01X4%20(Low%2C%20250).xlsx) for lower and [BQ25756_DESIGN-CALC-V01X4 (High, 250).xlsx](BQ25756_DESIGN-CALC-V01X4%20(High%2C%20250).xlsx) for higher output voltage) selected following power stage components and programming resistor values.
- Power Stage:
  - Inductor: 10uH, Isat > 4.07A, DCR 1.75 - 60mOhm (for example, [SRP1038A-100M](https://www.bourns.com/docs/Product-Datasheets/SRP1038A.pdf))
  - Power MOSFETs: [SiR880BDP](https://www.vishay.com/docs/63031/sir880bdp.pdf) (TI Recommended)
- Input Sensor and Current Limit:
  - Sense Resistor: 5mOhm
  - Input Pull-down: 4k (limit 5A)
- Input Under/Over-voltage Programming Resistors (for 4-6V with 4.4V DPM limit):
  - Top: 1000k
  - Middle: 103k
  - Bottom: 276k
- Output Sensor and Current Limit:
  - Sense Resistor: 5mOhm
  - Output Pull-down: 10k (limit 5A)
- Mode Resistor: 3k (sets Buck-Boost mode)
- Input/Output Capacitors: TBD
