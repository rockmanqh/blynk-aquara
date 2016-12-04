# blynk-aquara
=========

- The source code is from the project [homebridge-aqara](https://github.com/snOOrz/homebridge-aqara)
  Thanks to @snOOrz

![Blynk project](https://raw.githubusercontent.com/rockmanqh/blynk-aquara/master/blynk-aqara.png)
![Xiaomi devices - aqara](http://xiaomi-mi.com/uploads/CatalogueImage/fgfg%20(1)_13743_1435134515.jpg)

## Installation
- Enable LAN mode of xiaomi gateway ```http://bbs.xiaomi.cn/t-13198850```, you must upgrade to lastest version. 
  + On **`about page`** of Xiaomi Gateway, click on version number (1.2.6) a couple times to active developper mode.
  + Two others options will appear, then click on the option *with longest words in chinese just appeared* and active LAN mode.

- Get data from aqara devices 
  + Xiaomi Temperature-Humidity
  + Xiaomi Contact sensor
  + Xiaomi Human Body Sensor
  + Xiaomi Bulblight, ...
  
- Create a blynk project and put the token key in the udpserver.js file
  + Add 3 label in the project
  + Set the virtual pin for each label : V0, V1, V2

Label 1 | Label 2 | Label 3
--- | --- | ---
V0 | V1 | V2


## Usage                                
- Put the token key in the udpserver.js file
  + var AUTH = 'yourtokenkeyhere';
  + var v_temp = 'V0';
  + var v_hum = 'V1';
  + var v_door = 'V2';

## Tests
- Run the project
  + install plugin request:
  ```npm install request -g```
 
  + test code:  
    ```node udpserver.js```
 
  + run code on reboot:
    ```@reboot /usr/local/bin/node /home/pi/udpserver.js```
