# YD-2040-ZephyrRTOS-board-support

![Alt text](yd_2040_16mb/doc/img/yd_2040_16mb.jpg?raw=true "YD-2040(16MB)")


Support files for Zephyr RTOS to run on YD-2040 a Chinese clone for Raspberry Pi Pico (RP2040) with better configurations
The board almost matches the pinout for raspberry pi pico, but it features the  following extras:

* USB Type-C connector (better alternative to micro-usb in original pico board)
* 16 Mega byte flash (8x more storage instead of 2 megabytes originally used in Pico board) 
* Expose all ADC pins (ADC0, ADC1, ADC2, ADC3) 
* lower noise 3.3 voltage using LDO instead of DC-DC converter in original pico 
* User push-button connected to GPIO0_24 
* Extra RGB LED (WS2812)

# Installation 

Just copy the folder named "yd_2040_16mb" to zephyr ARM board definitions folder "zephyr/boards/arm"

now you can build any sample with flag **-b yd_2040_16mb**, For example you can start with hello world blinking led 
**west build -p always -b yd_2040_16mb samples/basic/blinky**

also, you can test the onboard user button with the following example (led will turn on when user presses the button)
**west build -p always -b yd_2040_16mb samples/basic/button/**


# Notes

* board is matching all digital pins layout with original Pico board, but it exposes extra ADC pins and remove the AREF pin
* You can buy it from AliExpress, just search for yd-2040
* 16 Mb flash is huge for firmware development, maybe you can utilize it to create a partition for file system, store multiple firmware images, load it with some reto games ...etc (use your imagination)