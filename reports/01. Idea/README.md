# Building a programmable DC-DC Power Supply with I2C Interface (I2C-PPS). Part 1 - Idea

<img src="../../I2C-PPS Sketch.Usage.png" alt="I2C-PPS Sketch" width="512">

I was lurking through DigiKey catalog and found a TI buck-boost controller with I²C interface - [BQ25758S](https://www.ti.com/product/BQ25758S). The controller allows to create a programmable power supply with quite impressive output specs - voltage 3.3-26V and current up to 20A. Decided to give it a try and create a compact board for my RPI Zero. I don't think I'll go above 3A input (which means only 500mA@26V give or take some efficiency) and it's a bit of a shame that the controller doesn't go below 3.3V (much better would be at least 1.8V). For starter created an umbrella repository - [github.com/condevtion/i2c-pps](https://github.com/condevtion/i2c-pps). This is a first post in a series where I'd like to share live process of the device creation.
