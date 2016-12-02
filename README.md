# blynk-aquara

- Get data from aqara devices 
  + Xiaomi Temperature-Humidity
  + Xiaomi Contact sensor

- Create a blynk project and put the token key in the udpserver.js file
  + Add 3 label in the project
  + Set the virtual pin for each as following

 ------    ------    ------ 
|      |  |      |  |      |
|  V0  |  |  V1  |  |  V2  |
|      |  |      |  |      |
 -----     ------    -----

var AUTH = 'yourtokenkeyhere';
var v_temp = 'V0';
var v_hum = 'V1';
var v_door = 'V2';

- Run the project
  + install plugin request
    npm install request -g 
  
  + run  
    node udpserver.js
