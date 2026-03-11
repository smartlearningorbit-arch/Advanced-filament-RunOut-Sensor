# Advanced-filament-RunOut-Sensor
<img width="935" height="665" alt="image" src="https://github.com/user-attachments/assets/b2233b12-f2bb-46f3-8386-72662646c1be" />

## About the Filament Run Out Sensor

This project is about making a **smart Filament Run Out Sensor** for 3D printers.<br/>
Normally printers have a very simple sensor which only detect when the filament finished and then it pause the printer. But that type of sensor is very basic and it does not give any extra information.<br/>
So the idea here is to make a **better and smarter version** of that sensor.<br/>
Instead of using a simple switch, this system uses a **filament presence sensor + rotary encoder** to detect the movement of filament. The encoder helps measure how much filament is moving through the system.<br/>
An **ESP32 module** is used as the main controller because it have built-in WiFi which allows the device to send data over internet. <br/>

### Features
- Filament run out detection  
- Filament jam detection  
- Calculate the filament used during print  
- Monitor the data over WiFi  
- Simple dashboard to check printer status  

### Why we are making this
The main reason is to make a **more intelligent filament monitoring system** for 3D printers. <br/>
This helps to:
- avoid print failure due to filament run out  
- detect filament jam early  
- track filament usage  
- monitor printer remotely  

So overall this project makes the printer **more reliable and smarter** compared to normal run out sensors. <br/>

### PCB 
<img width="884" height="727" alt="image" src="https://github.com/user-attachments/assets/1b9201da-8737-472a-9c68-eacecbd32225" />
<img width="825" height="708" alt="image" src="https://github.com/user-attachments/assets/7d12fb92-b5bb-4c75-9d62-31fc98504910" />

### Systematic
<img width="1190" height="845" alt="SCH_Filament runoff sensor_1-P1_2026-03-12" src="https://github.com/user-attachments/assets/ccf5aaaa-d9f5-4039-a2f3-069cefdceb79" />

### CAD
<img width="528" height="511" alt="Screenshot 2026-03-12 034915" src="https://github.com/user-attachments/assets/cd4af574-947a-49ce-a00e-01c64bb253eb" />
<img width="654" height="726" alt="Screenshot 2026-03-12 034937" src="https://github.com/user-attachments/assets/12177b84-24b6-47e1-966e-7e493240c90d" />
<img width="935" height="665" alt="image" src="https://github.com/user-attachments/assets/0789deca-30cc-4b76-8dcb-28f720aba6ec" />


### BOM
|NAME                                               |QTY|PRICE (INR)|TOTAL PRICE (INR)|TOTAL (USD)|LINK                                                                                                               |
|---------------------------------------------------|---|-----------|-----------------|-----------|-------------------------------------------------------------------------------------------------------------------|
|ESP32-WROOM-32 8M                                  |1  |349        |349              |3.772972973|https://robu.in/product/espressif-esp32-wroom-32-8m-64mbit-wifi-flash-bluetooth-module/                            |
|5mm Infrared Slot Photoelectric Count Sensor Module|1  |72         |72               |0.778378378|https://robu.in/product/correlation-photoelectric-infrared-count-sensor-module/                                    |
|Rotary encoder                                     |1  |58         |58               |0.627027027|https://robu.in/product/hongyan-ec11h-7ce20p1zy20-rotary-encoder-with-push-button-switch-vertical-plug-in-5-pin/   |
|TP4056 1A Li-Ion Battery Charging Board            |1  |16         |16               |0.172972973|https://robu.in/product/tp4056-1a-li-ion-battery-charging-board-micro-usb-with-current-protection-type-c-connector/|
|PCB Fabrication                                    |1  |1200       |1200             |12.97297297|https://www.lioncircuits.com/                                                                                      |
|Resitor & Capacitor                                |1  |400        |400              |4.324324324|https://robu.in/                                                                                                   |
|battery                                            |1  |300        |300              |3.243243243|https://robu.in/product/1500mah-pcm-protected-micro-li-po-battery/                                                 |
|TOTAL                                              |   |           |2395             |25.89189189|                                                                                                                   |


