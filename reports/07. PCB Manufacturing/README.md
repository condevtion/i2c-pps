# Building I2C-PPS. Part 7 - PCB Manufacturing

<img src="../../i2c-pps-hw-pcb-top.png" alt="I2C-PPS PCB Top" width="860">

<img src="../../i2c-pps-hw-pcb-bot.png" alt="I2C-PPS PCB Bottom" width="860">

<img src="../../i2c-pps-hw-stencil.png" alt="I2C-PPS Stencil" width="860">

Initially planned to order PCB and stencil manufacturing at PCBWay factory. They offer design rules in KiCAD format which is really convenient as there are too many of them and they vary depending on different factors like, for example, copper weight. However, it appeared that the batch would cost there more than $200 only for manufacturing besides taxes and delivery for a 4-layer board with 2oz outer/1oz inner copper and via-in-pad requirements. The most surprising thing was that the price went from about $100 as initial estimation to more than $200 after review. So I went to JLCPBC and they asked just $63.32 with the same requirements. Also it looks like they have more modern equipment which results in better capabilities. While you need to setup design rules manually (or find KiCAD files composed by someone else and just check them) price and capabilities difference is huge.

Also I chose DHL Express Priority shipment with DPP to skip hassle on custom clearance which unfortunately added 50% to the price. But I got my order within 2 days after the merchandise left the factory. What an awesome experience!

Final product looks great to me. I’m surprised by silkscreen quality as pushed font size to the minimum. Still everything is sharp and very readable. Interestingly, there is a difference between how KiCAD and factory measure text size. KiCAD doesn’t take into account line width and measures distance between centerlines while factory measures full letter. So 0.8mm KiCAD letters get almost 1mm height with 0.16mm line width.

The next step would be to attempt manual assembly.
