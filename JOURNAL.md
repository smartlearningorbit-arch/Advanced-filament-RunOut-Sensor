
# Date/log - wednesday, 11 March, 2026 / 5.6 hr 
## Systematic + routing
So after Selected all the component I start connecting the component <br/>
### Systematic <br/>
<img width="1190" height="845" alt="SCH_Filament runoff sensor_1-P1_2026-03-12" src="https://github.com/user-attachments/assets/0669222d-4d35-4d96-a5dd-b6252f8adb4d" /> <br/>
then Routed the PCB it ready take time cuz i want to make it compactact <br/>
### PCB <br/>
<img width="621" height="590" alt="image" src="https://github.com/user-attachments/assets/f327bb87-032b-4afd-b7bd-dba2a64fd00b" />
<img width="882" height="722" alt="image" src="https://github.com/user-attachments/assets/4eaf8852-ea10-4715-8b6d-66a52b9c04a0" />


# Date/log - wednesday, 11 March, 2026 / 1.8 hr 
## Hardware selection 

- Filament present sensor  <br/> 
 Photoelectric Infrared Count Slot Sensor Module 10 mm ( Suitable for my model )

- Encoder  <br/> 
EC11 A basic cheap Rotary encoder ( From manufacture side it have Mechanism which produce click Tactile But for this case it is not needed So I just to remove that spring Mechanism )  

- MCU  <br/> 
  ESP32 wroom 32D Module the Best cheap Board with Wifi  

# Date/log - wednesday, 11 March, 2026 / 1.8 hr 
## Plan
<img width="707" height="698" alt="image" src="https://github.com/user-attachments/assets/87fea69e-bdf1-4362-b397-723bb61f47f2" /> <br/> 
```
Filament Presence Sensor
          │
          ▼
Encoder Motion Sensor
          │
          ▼
         ESP32
          │
          ├── Filament Analytics
          ├── Jam Detection Logic
          ├── Runout Detection Logic
          │
          ▼
        WiFi → Dashboard
```


# Date/log - Saturday, 7 March, 2026 / 3.6 hr 
## Research & plan 
After Conducting a deep research I plan to make a Filament Run Out Sensor {Not a simple one as we see} <br/>
but rather than the smart Filament Run Out in Which the uses the encoder sensor insead of button and wifi embled ESP32 <br/>
So what it help <br/>
- Filament run out
- Calculate the felament uses
- jam Detection
- Esp32 help Monitor the data anywere via help of internet 
