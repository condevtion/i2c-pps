# Programmable DC-DC Power Supply with I2C Interface

## About
The repository gathers hardware, software, and management artifacts of the power supply development.

## Purpose
Compact Bench Power Supply controllable by [Raspberry Pi Zero 2 W](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/) and powered by the same AC-DC supply with enough power budged (for example, [MEAN WELL RS-35-5](https://www.meanwellusa.com/webapp/product/search.aspx?prod=RS-35)).

## Specifications
- Controller: Texas Instruments [BQ25758S](https://www.ti.com/product/BQ25758S)
- Input voltage: 5V
- Input current: up to 3A
- Output voltage: programmable by I2C in controller defined range (3.3 - 26V)
- Output current: up to 3A (limited by input)
