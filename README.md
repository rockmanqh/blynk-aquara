# blynk-aquara

- The source code is from the project homebridge-aqara
  Thanks to @snOOrz

- Get data from aqara devices 
  + Xiaomi Temperature-Humidity
  + Xiaomi Contact sensor

- Create a blynk project and put the token key in the udpserver.js file
  + Add 3 label in the project
  + Set the virtual pin for each label : V0, V1, V2
                                
- Put the token key in the udpserver.js file
  + var AUTH = 'yourtokenkeyhere';
  + var v_temp = 'V0';
  + var v_hum = 'V1';
  + var v_door = 'V2';

- Run the project
  + install plugin request:
    npm install request -g 
  
  + test code:  
    node udpserver.js
 
  + run code on reboot:
    @reboot /usr/loca/bin/node /home/pi/udpserver.js

