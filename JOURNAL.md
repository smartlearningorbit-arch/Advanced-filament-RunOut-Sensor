# Total Time So far 12.5 HR


# Date/log -  12 March, 2026 / 1.1 hr 
## CAD DESIGNING
After everything is completed I start building the Assembly file of the project I export the 3d Model of the PCB And open it on fusion 360 
then I Start making the case And I finally build the case <br/>
### CASE ASSEMBLY
<img width="935" height="665" alt="image" src="https://github.com/user-attachments/assets/8b840fd2-e5a8-4b32-9b81-67730ab519b2" />
<img width="528" height="511" alt="image" src="https://github.com/user-attachments/assets/cdd82c41-13c7-4de4-8e59-99143523da6a" />
<img width="654" height="726" alt="image" src="https://github.com/user-attachments/assets/47f5cca4-a744-40b6-bb06-009363a3a14a" />

### What I learn : 
- How to export the 3d model 
- Cad designing 

 -----------------------------------------------------------------


# Date/log - wednesday, 11 March, 2026 / 5.6 hr 
## Systematic + routing
So after Selected all the component I start connecting the component <br/>
### Systematic <br/>
<img width="1190" height="845" alt="SCH_Filament runoff sensor_1-P1_2026-03-12" src="https://github.com/user-attachments/assets/0669222d-4d35-4d96-a5dd-b6252f8adb4d" /> <br/>

### PCB <br/>
then Routed the PCB it ready take time cuz i want to make it compactact <br/>
<img width="621" height="590" alt="image" src="https://github.com/user-attachments/assets/f327bb87-032b-4afd-b7bd-dba2a64fd00b" />
<img width="882" height="722" alt="image" src="https://github.com/user-attachments/assets/4eaf8852-ea10-4715-8b6d-66a52b9c04a0" />

### Problems : 
There are few component Whose symbol and footprint are not available, And many whose 3D model is not available 
### Resolution :
 For the symbol I design the Symbol by own And for For the 3D model I Find it on grabcad website
### What I learn :
- How to make the own symbol
- How to Upload and Adjust the 3D model Perfectly on the footprint 

 -----------------------------------------------------------------

 
# Date/log - wednesday, 11 March, 2026 / 1.5 hr 
## Hardware selection 

- Filament present sensor  <br/> 
 Photoelectric Infrared Count Slot Sensor Module 10 mm ( Suitable for my model )

- Encoder  <br/> 
EC11 A basic cheap Rotary encoder ( From manufacture side it have Mechanism which produce click Tactile But for this case it is not needed So I just to remove that spring Mechanism )  

- MCU  <br/> 
  ESP32 wroom 32D Module the Best cheap Board with Wifi  

### Problems : 
The Rotary encoder have The click the mechanism which Which reduces the smoothness and increase the friction
### Resolution :
 I open the Rotary encoder and Remove Spring type structure That creating the click Tactile
### What I learn :
- How to convert the Normal encoder into smooth encoder

-----------------------------------------------------------------------



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

Idea is simple but powerful.
| Printer State | Filament Present | Encoder    | Result |
| ------------- | ---------------- | ---------- | ------ |
| Idle          | Yes              | No         | Normal |
| Printing      | Yes              | Moving     | Normal |
| Printing      | Yes              | Not moving | Jam    |
| Printing      | No               | Not moving | Runout |

### Problems : 
First I only using a encoder Which don't know the filament is there or not , Means No jam detection
### Resolution :
 I added A Ir sensor Before the Encoder to know whether the Filament is there or not
### What I learn :
- How to check the presence Of filament
- How does the jam detection work 
------------------------------------------------------------------------------

# Date/log - Saturday, 7 March, 2026 / 2.4 hr  
## Research & plan  
After conducting a deep research I decided to build a **Filament Run Out Sensor**.  
But not a simple one like most printer have.  
Instead the idea is to make a **smart filament sensor** which uses:
- encoder sensor instead of button switch  
- WiFi enabled ESP32  
- data monitoring system  

So basically it will not just detect filament end, it will also provide **extra useful information**.
### What this system can do
- Filament run out detection  
- Calculate the **filament used** during printing  
- Jam detection  
- ESP32 send data over internet so it can be **monitored from anywhere**
