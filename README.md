# Cloud-X
A flight controller that is ready made to use for ejection on an educational rocketry model. 

# Overview
This project explores the development of a model rocket and an accompanying STM32 based avionics data logging system. 

The electronics project focuses on collecting and recording sensor measurements, allowing data to be studied and visualized during engineering expreiments. 

# Objectives
- Design a custom PCB using KiCAD
- Develop embedded firmware for an STM32 microcontroller
- Integrate motion and atmospheric pressure sensors
- Implement microSD data storage
- Analyze sensor measurements and visualize recorded data.
- Document the engineering and development process.

# Electronics
The avionics electronics design uses the following main components

|Component|Purpose|
|---|---|
|STM32F7SSRET6|Main microcontroller | 
| ICM-45686 | Motion sensin |
| BMP580 | Atmospheric pressure measurement | 
| HRS DM3D SF | microSD card interface | 
| USB type C | Programming and data transfer | 
| AP2112K-3.3 | Voltage regulation | 
| USBLC6-2SC6 | USB ESD protection | 

# PCB designing 
The custom PCB is designed using KiCAD 
The electronics documentation covers: 
- Schematic design
- PCB layout
- Component selection
- power-management review
- sensor integration
- firmware development
- design rule verification

# Firmware
Firmware development focuses on: 
- STM32 intialization
- Sensor communication
- Sensor data acquisition
- microSD data recording
- USB communication
- Diagnostic information

# Development tools 
- KiCAD: PCB and schematic design
- STM32CubeIDE: Embedded development

# Safety 
This repository documents an educational aerospace engineering project. Any physical rocketry activities must follow applicable laws, recognized model rocketry safety standards and qualified adult supervision. 

The electronics documentation is **NOT** an instruction manual for constructing or operation propulsion or pyrotechnic systems. 

# BOM

# Project pictures 

**Schematics**

<img width="1350" height="831" alt="image" src="https://github.com/user-attachments/assets/cce0d5b8-31d9-43df-8252-6c88c7a6923e" />

**PCB**

<img width="741" height="732" alt="Screenshot 2026-11-12 021925" src="https://github.com/user-attachments/assets/61cab373-5f29-4301-b85b-588c4785163a" />

**PCB 3D RENDERED**

<img width="663" height="667" alt="Screenshot 2026-11-12 021939" src="https://github.com/user-attachments/assets/4a6a556c-688f-4918-9de5-0de1931d1668" />


**Avionics Bay**

<img width="481" height="571" alt="image" src="https://github.com/user-attachments/assets/0079ad6d-ba7c-4d86-99c4-7617014c6693" />


**OpenRocket Software Rocket Design**

<img width="1767" height="407" alt="image" src="https://github.com/user-attachments/assets/c95ab5f6-0d8a-4ceb-9998-32dceb5be69f" />
