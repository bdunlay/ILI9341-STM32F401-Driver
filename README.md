
# ABOUT

This is a ILI9341 driver and graphics library for the STM32F401RE, compatible with the ILI9341 shield from adafruit. The library is a port of the original Adafruit-GFX-Library and Adafruit_ILI9341 C++ libraries to pure C. Some features are missing, and no guarantees!

See the BSD license for borrowed code in license.txt

See the original implementations here:

* https://github.com/adafruit/Adafruit-GFX-Library
* https://github.com/adafruit/Adafruit_ILI9341

# SETUP

Use STMCube32MX to configure the HAL for use with the shield.

* SPI1: Full-Duplex Master
* GPIO PC7: Set to Output, give a name of "LCD_DC"
* GPIO PB6: Set to Output, give a name of "LCD_CS"

Pass the hspi1 handle by reference to the ILI9341_begin() function. Ex:

```
ILI9341_begin(&hspi1);
```

Make sure to compile with c99+ standard, or else some of it might fail to compile (e.g. initialize on declaration)

