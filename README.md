# YD-2040-ZephyrRTOS-board-support

Support files for Zephyr RTOS to run on YD-2040 a chinese clone for Raspberry Pi Pico (RP2040) with better configurations
The board almost matches the pinout for raspberry pi pico, but it features the  following extras:

* USB Type-C connector (better alternative to micro-usb in original pico board)
* 16 Mega byte flash (8x more storage instaed of 2 mega bytes originaly used in Pico board) 
* Expose all ADC pins (ADC0, ADC1, ADC2, ADC3) 
* lower noise 3.3 voltage using LDO instead of DC-DC converter in orginal pico 
* User push-button connected to GPIO0_24 
* Extra RGB led (WS2812)

*NOTE:* board is matching all digital pins layout with original Pico board but it expose extra ADC pins and removed the AREF pin 

support file cloned from original Pico board and modified to use the extra 16MB flash, switch (you can test it on Zephyr RTOS using samples/basic/button/)

You can buy it from aliexpress, just search for yd-2040