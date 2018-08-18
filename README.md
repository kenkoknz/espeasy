# espeasy

Guide: https://www.letscontrolit.com/wiki/index.php/Basics,Tutorials_%26_Howto%27s#KIS_-_Keep_It_Simple.21

https://diyprojects.io/esp-easy-firmware-esp8266-create-connected-objects-smarthome-without-programming/#.WxPU9u6FN0w

Compatible board types: https://www.letscontrolit.com/wiki/index.php/Basics:_ESP8266_Types_and_Boards

vid for sonoff: https://www.youtube.com/watch?time_continue=662&v=_LeUUkYNgA4



There are several versions of the ESP01 on the market. They differ in pinout and memory size.

If your dealer offers ESP-01 with a blue PCB - do not buy! These have only 512KB of flash ram which is too low for ESPEasy-2.x.

The newer ESP-01 with a black PCB have 1MB flash, they can run with ESPEasy-2.x, but 4mb is reccomended for espeasy 2.x.

https://www.letscontrolit.com/wiki/index.php/Configuration  pin usage

--------------------------------------------------------------------
ESPEASY Install:

As of jul18: 2 versions, r120 (smaller size, to be replaced by v2.0) and teh Mega v2.0; have tested mega on wemos and sonoff.

install espeasy:https://www.letscontrolit.com/wiki/index.php/Tutorial_ESPEasy_Firmware_Upload

Flashing the module

Step 1 - Find the right flash size of your module

Step 2 - Download the zipfile here: ESPEasy - loading firmware and unpack to a folder of choice.

Step 3 - Double Click "flash.cmd". A command windows should start with three questions.

Step 4 - Select the com port that your module or FTDI module is using (use device mgr to find com port e.g 34)

Step 5 - Select the flash size, 512, 1024 or 4096

Step 6 - Select the build version like 120 or newer.

After successful uploading, reboot the ESP module (press reset if you have a button or power off/power on the module)

The ESP module should start a Wifi Access point named ESP_0 

connect to ESP_0



When a fresh ESP Easy module boots up, it has no Wifi config and it will start as an Access Point. Use a Wifi enabled device (Laptop, 

Tablet, Smartphone,..) to search for Wifi access and try to find an access point with the name ESP_Easy_0 (prior to 2.0 the AP was named 

ESP_0). 

ref: https://www.letscontrolit.com/wiki/index.php/EasySetup

**Connect to this access point with default password: configesp 


set wifi credentials

use http://192.168.4.1/setup if not redirected


Should get config screen


Change name "Newdevice" to a unique name


-----------------------
Notes on pin convention; esp uses eg d1 and d2; ard uses gpio, when using ide or espeasy  use gpio convention;

eg fo wemos oledshield

d1= clk = gpio5

d2=sda = gpio4 

eg D0 = gpio16


Pin	Function	ESP-8266 Pin

TX	TXD	=gpio 1
RX	RXD =gpio 3 
A0	Analog input, max 3.3V input	A0

D0	IO	GPIO16

D1	IO, SCL	GPIO5

D2	IO, SDA	GPIO4

D3	IO, 10k Pull-up	GPIO0

D4	IO, 10k Pull-up, BUILTIN_LED	GPIO2

D5	IO, SCK	GPIO14

D6	IO, MISO	GPIO12

D7	IO, MOSI	GPIO13

D8	IO, 10k Pull-down, SS	GPIO15

G	Ground	GND
5V	5V	-
3V3	3.3V	3.3V
RST	Reset	RST




---------------

pic:

![image](https://user-images.githubusercontent.com/6856411/42980656-ddd86ea2-8bc7-11e8-9639-03dd6e00fecd.jpg)

![image](https://user-images.githubusercontent.com/6856411/42979880-272bcf80-8bc4-11e8-95a9-1c4134e5956b.PNG)

![image](https://user-images.githubusercontent.com/6856411/42980669-ea6508f6-8bc7-11e8-9373-7da8a5740b1b.jpg)
