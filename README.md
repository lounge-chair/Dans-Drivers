# Dan's Drivers
Hello! You've reached my personal collection of drivers I've written for various components and microcontrollers. 
Below you will find descriptions of the drivers and links to the components.

*Note: Many of these drivers also initialize a designated serial communication peripheral. These peripherals were chosen based on the schematics of the daughterboards utilized in my projects, as well as peripheral availability. While I'm certain you can get something out of this code even if you choose to use a different peripheral (if only as a "jumping-off point" for your own approach), you may need to edit the code (mainly the inits) to make it work for your microcontroller.*

## MSP432 Drivers
These drivers were written with TI's MSP432P401R microcontroller in mind, but they should work with any MSP432-family microcontroller.
### HY28B - Touchscreen TFT LCD (SPI)
Driver for the [HY28B touchscreen TFT LCD](https://www.hotmcu.com/28-touch-screen-tft-lcd-with-all-interface-p-63.html), which uses a ILI9325 LCD Controller and a XPT2046 Touchscreen Controller. 

Includes code to initialize/use the EUSCI_B3 peripheral in SPI mode.

### LP3943 - LED Controller (I2C)
Driver for the [LP3943 LED Controller](https://www.ti.com/product/LP3943). No PWM in this current version as I did not require it for the project I was working on, but the function prototype is there. 

Includes code to initialize/use the EUSCI_B2 peripheral in I2C mode.


## F2837xD Drivers
These drivers were written with the TI TMS320F28379D DSP in mind, but they should work with any F2837xD-family DSP.
### 2 x IS62WVS2568GBLL-45NLI-TR - 2 x (256k x 8) SRAMs (SPI)
Driver for a dual [IS62WVS2568GBLL-45NLI-TR](https://www.mouser.com/ProductDetail/ISSI/IS62WVS2568GBLL-45NLI-TR?qs=F5EMLAvA7IDi1b3lWvG69A%3D%3D) board. Combines two 256k x 8 SRAMs to "create" a 256k x 16 SRAM. 

Includes code to initialize/use the SPIB peripheral.

### LCD1602 - 16x2 Serial LCD (I2C)
Driver for the [LCD1602 16x2 LCD](https://www.addicore.com/1602-16x2-Character-LCD-with-I2C-backpack-p/156.htm), utilizing a PCF8574T serial-to-parallel I2C expander. 

An I2C library is also included, although I did not write this one.
