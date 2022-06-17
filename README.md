# RP2040-GC9A01

![image](https://github.com/01Space/RP2040-GC9A01/blob/main/image/2.jpg)

![image](https://github.com/01Space/RP2040-GC9A01/blob/main/image/4.jpg)

# GC9A01

 BL   - pin 2
 
 DC   - pin 8
 
 CS   - pin 9
 
 RST  - pin 12
 
 MOSI - pin 11
 
 SCK  - pin 10

 # SD card 

 MISO - pin 16
 
 MOSI - pin 19
 
 CS   - pin 17
 
 SCK  - pin 18
 
 # other
 
 LED  - pin 14
 
 RGB  - pin 15 
 
 button 0 - pin 0
 
 button 1 - pin 1
 
 Buzzer   - pin 7
 

# General Flashing Instructions:

# Using arduinocore mbed

With ArduinoCore-mbed Release 2.0.0, Arduino now support Raspberry Pi Pico officially. To program Raspberry Pi Pico in Arduino framework, install Arduino Mbed OS RP2040 Boards in Arduino IDE's Library Manager.

![image](https://github.com/01Space/RP2040-0.42LCD/blob/main/image/Arduino%20Mbed%20OS%20RP2040%20Boards.jpg)

# Using earlephilhower/arduino-pico
https://github.com/earlephilhower/arduino-pico This link has a very detailed description

Install Arduino IDE and install pico resources by adding line "https://github.com/earlephilhower/arduino-pico/releases/download/global/package_rp2040_index.json" to Additional Boards Manager URLs in Arduino IDE Files / Preferences.
Via Arduino IDE Tools/Board / Board Manager search for pico and choose Raspberry Pi Pico/RP2040 version 2.0.1 to install it.

# Upload sketch from Arduino IDE:

Uploading Sketches
To upload your first sketch, you will need to hold the BOOTSEL button down while plugging in the Pico to your computer. Then hit the upload button and the sketch should be transferred and start to run.

After the first upload, this should not be necessary as the core has auto-reset support. Select the appropriate serial port shown in the Arduino Tools->Port->Serial Port menu once (this setting will stick and does not need to be touched for multiple uploads). This selection allows the auto-reset tool to identify the proper device to reset. Them hit the upload button and your sketch should upload and run.arduino-pico

In some cases the Pico will encounter a hard hang and its USB port will not respond to the auto-reset request. Should this happen, just follow the initial procedure of holding the BOOTSEL button down while plugging in the Pico to enter the ROM bootloader.

# The following libraries need to be installed

TFT_eSPI （https://github.com/Bodmer/TFT_eSPI）

If TFT is used_ The ESPI library needs to modify the following 7 lines

C:\Users\86186\Documents\Arduino\libraries\TFT_eSPI

# Setup200_GC9A01.h  

#define TFT_MOSI 11 

#define TFT_SCLK 10

#define TFT_CS   9 

#define TFT_DC   8 

#define TFT_RST  12 

#define TFT_BL   2  

# User_Setup_Select.h

Only ONE line below should be uncommented

#include <User_Setups/Setup200_GC9A01.h> 

# You can also use Arduino_ Gfx Library

Arduino_GFX(https://github.com/moononournation/Arduino_GFX)

# Open Source / Contributors



And many many others who haven't been mentioned....



# Contact 01Space
facebook:Jiale Xu

twitter:yongxiangxu251

E-mail：759315223@qq.com
