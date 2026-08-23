# weatherStation
![enter image description here](https://i.imgur.com/7wUpwVc.png)
### Overview
This is a simple Weather Station having the following sensors:

 - Temperature sensor
 - Humidity sensor
 - Wind Speed sensor

Currently the Station uses the **NodeMCU V3**, with the embedded **ESP8266** `WiFi Module.`
For this reason, the station can only have **one** `Analog Input`, and the port is wired to the `Wind Speed sensor`.

The next version will use the `ESP32`, that has **18** Analog Inputs, yes, a lot of pins!
Having such a number of `analog inputs` i'll be able to connect a lot of analog sensors, and i'm planning to add:

 - Light sensor
 - Rain sensor
 - Barometer
 - Pyranometer 
 - CO2 sensor
### The UI
![WeatherStation](https://i.imgur.com/GxdUQAs.png)
The **UI** was built using [ThingSpeak](https://thingspeak.com/) that offers an **API** to populate the various **Widgets**
![enter image description here](https://i.imgur.com/3Vg22i2.png)




---
### Parts used

 - `NodeMCU V3` with `ESP8266` **WiFi Module**
 - One `10k Ohm resistor`
 - `DHT11` Temperature/Humidity sensor (I don't like this sensor, if you are planning to build something like this, use another sensor)
 - `5V DC motor` (Used for the Wind Speed Sensor, agin, do not use this method. The next version will use a `Magnetic Sensor` to compute the wind speed)
 - `A 3D Printer` (mh, that's crucial)

---
### 3D Project
The project is available on [Thingiverse](https://www.thingiverse.com/thing:4937362), or there is a [Folder](https://github.com/follen99/weatherStation/tree/main/3D_Models) where all files are uploaded.
The project consists of **two main parts**:

#### Arduino case
The case only has room for the `NodeMCU` and the `DHT11 sensor`.
Moreover, the case has an hole on the left side for the external `Wind Sensor` and a vent on the right for the `DHT11 sensor`.
![front](https://i.imgur.com/TjuZdAM.png)

![back](https://i.imgur.com/WKYXUVF.png)


#### Wind Speed Support
The wind speed sensor is supported by a 3D printed part mounted on the wall.
This part should be printed in a weather resistant material, such as PETG or ABS, don't use PLA.
Moreover, the "blades" are 3D printed too.
![enter image description here](https://i.imgur.com/YaZVVCU.png)

## MATLAB
We can use **MATLAB** scripts to analyze our data:
### Histograms
![histogram](https://i.imgur.com/JxM5i7b.png)
That computes: 

![enter image description here](https://i.imgur.com/kTzertz.png)

---
### Some Pics
![enter image description here](https://i.imgur.com/qeI81sg.jpg)

![enter image description here](https://i.imgur.com/XHGKIaL.jpg)



https://user-images.githubusercontent.com/74026278/130363595-80cdf6d4-ce8a-403d-b3db-37c81fa7ad7b.mp4
