# PylontechTasmota
### Pylontech using Tasmota

The purpose of this repository is to help you to read the status of Pylontech battery using Tasmota <br />
Unfortunately there is not a STD tasmote firmware which has all the required features we need, which means you have to compile a fresh one with the right features <br />
Start a new workspace in Gitpod here: https://gitpod.io/new#https://github.com/arendst/Tasmota <br />
Open /tasmota/user_config_override.h <br />
Edit this file with the parts from the Mods_user_config_override.h Simply cut and paste from this page<br />
https://github.com/krulkip/PylontechTasmota/blob/f4eebe08689806caace1d27da7f744459dc9891e/Mods_user_config_override#L1-L29
This file you can find here https://github.com/krulkip/PylontechTasmota/blob/main/Mods_user_config_override <br />
After the following prompt at the bottom of the page /workspace/Tasmota (development) $ type platformio run -e tasmota <br />
After the compile has completed a file will appear under build_output/firmware called firmware.bin<br />
Program your ESP8266 with that code. I use tasmotiser for that. You simply select this bin file and make sure the settings for self resetting device is set correctly <br />
The firmware activates Display-LCD and Scripting language amongst other things. <br />
After the upload is complete the firmware is restarted and after a short wait you can click on the Get IP button to reveal the IP.
Go to this IP in a webbrowser.<br />
Click on the configuration button and then configure template. This will take you to a new page with possibilities. <br />
Edit these until you get the below settings.
<img src="/Tasmota10.jpg" width="200" height="300">
Now go to configure other. Please change the friendly name to Pylontech etc. <br /> <br />
Dont forget to click on the activate button <br />
After completing this part your screen will look something like below. <br /> <br />
<img src="/Tasmota7.jpg" width="200" height="300">
<img src="/PylontechLCD.jpg" width="200" height="200"><br /><br />
<img src="/PylontechSchematic.jpg" width="1000" height="500"><br /><br />
There are several commands in the Console you need to enter.
 - DisplayModel 1
 - DisplayMode 0
 - DisplayRefresh 2
 - DisplayAddress 63
 - Teleperiod 12
 - DisplayCols 16 according to your LCD
 - DisplayRows 4  according to your LCD
 - WebButton1 LED
 - WebButton2 LCD
