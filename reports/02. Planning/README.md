# Building I2C-PPS. Part 2 - Planning

<img src="../../I2C-PPS Sketch.Diagram.png" alt="I2C-PPS Sketch Device Diagram" width="720">

Continuing from the idea published a couple of days before - Building a programmable DC-DC Power Supply with I2C Interface [(I2C-PPS). Part 1 - Idea.](https://github.com/condevtion/i2c-pps/tree/main/reports/01.%20Idea)

I decided to get some intuition about overall device structure before gathering its schematics. As I sketched it in the picture the buck-boost converter can be seen as the set of several blocks - a power stage, input and output filters with respective current sensors, a set of programming resistors, a digital I/O plus indication circuit, and a master switch. The power stage consist of 4 power MOSFETs and the inductor. The input and output filters are sets of capacitors mixed with current sensing resistors. The converter's operation mode and HW limits on voltage and current are set by programming resistors. And digital I/O with indication circuit provides interface for RPI and some leds for us - humans. The master switch makes it possible to start or shutdown the thing as it needed independently by RPI as it's needed. Normally, it should stay off and should go off if RPI goes down turning the converter off when input voltage is here without running RPI.

For the switcher TI provides a design calculator in form of an excel spreadsheet and schematic design checklist which allow to select values for main components with desired input and output specs in mind. As for now I decided to go with 4-6V input window but it really should stay at 5V and set HW input and output current limits at 5A. With 250kHz switching frequency many 10uH inductors with Isat > 7A and DCR in recommended range should work along with set of recommended power MOSFETs. More details you can find in the project repo - [github.com/condevtion/i2c-pps](https://github.com/condevtion/i2c-pps).

Looks like it's time to pull KiCAD into the project.
