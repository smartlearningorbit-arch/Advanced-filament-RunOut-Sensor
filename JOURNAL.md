# Total Time So far 12.5 HR


# Date/log - 12 March, 2026 / 1.1 hr 
## CAD DESIGNING
After completing the PCB design I started working on the **mechanical side of the project**, which is designing the **case for the sensor**.
First I exported the **3D model of the PCB** from the PCB software and then imported it into **Fusion 360**. This helped me design the enclosure while seeing the exact position of the components.

### Case Designing Process
While designing the case I had to consider a few things:
- Proper **space for PCB components**
- Mounting holes for the PCB
- Opening for the **sensor module**
- Enough tolerance so the PCB fits properly
- Making the design **compact and pocket friendly**
I started by creating a **base shell** and then slowly adjusted the internal space according to the PCB model.  
After that I added **mounting supports** so the PCB can be fixed inside the case.

One important thing I checked was the **clearance between components and case walls**, because if the tolerance is too tight it becomes difficult to assemble.

### Case Assembly
Here is the final case assembly with the PCB model inside:

<img width="935" height="665" alt="image" src="https://github.com/user-attachments/assets/8b840fd2-e5a8-4b32-9b81-67730ab519b2" />
<img width="528" height="511" alt="image" src="https://github.com/user-attachments/assets/cdd82c41-13c7-4de4-8e59-99143523da6a" />
<img width="654" height="726" alt="image" src="https://github.com/user-attachments/assets/47f5cca4-a744-40b6-bb06-009363a3a14a" />

### What I learned
- How to **export a 3D PCB model**
- How to **import PCB models into Fusion 360**
- Basic **enclosure design workflow**
- Importance of **tolerance and spacing in mechanical design**

 -----------------------------------------------------------------

# Date/log - Wednesday, 11 March, 2026 / 5.6 hr 
## Schematic + PCB Routing
After selecting all the components for the project, I started working on the **schematic design**.  
This step is important because it defines how every component will communicate with each other.

### Schematic
First I placed all the components and started connecting them according to the design logic of the filament sensor system. <br/>
Things I connected in the schematic:
- ESP32 MCU
- Filament presence sensor
- Encoder
- Power connections
- Required resistors and supporting components

Here is the schematic:
<img width="1190" height="845" alt="SCH_Filament runoff sensor_1-P1_2026-03-12" src="https://github.com/user-attachments/assets/0669222d-4d35-4d96-a5dd-b6252f8adb4d" />


### PCB Layout
After finishing the schematic, I moved to the **PCB routing stage**. <br/>
This part took a good amount of time because I wanted the board to be **compact and clean**.  <br/>
I tried to place the components carefully so the routing becomes easier and also the final board size stays small. <br/>

While routing I tried to keep:

- short trace length
- clean routing
- good component placement
- compact board design

Here is the PCB layout: <br/>
<img width="621" height="590" alt="image" src="https://github.com/user-attachments/assets/f327bb87-032b-4afd-b7bd-dba2a64fd00b" />
<img width="882" height="722" alt="image" src="https://github.com/user-attachments/assets/4eaf8852-ea10-4715-8b6d-66a52b9c04a0" />


### Problems
During the design process I faced a few problems:
- Some components **did not have symbol in the library**
- Some parts **did not have footprints**
- A few components **did not have 3D models**
This slowed down the design process a bit.

### Resolution
To solve these issues:
- I **created custom symbols** for missing components
- For missing **3D models**, I searched online and found suitable models from **GrabCAD**
- Then I **aligned and adjusted the 3D models with the footprint** so they fit correctly in the PCB preview


### What I learned
- How to **design custom symbols for components**
- How to **import external 3D models**
- How to **align and adjust 3D models with PCB footprints**
- Importance of **component placement before routing**


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
