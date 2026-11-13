# Cloud-X
An educational model rocketry project exploring aerospace engineering, embedded programming and systems, electronics design and flight-data analysis

# Overview
This project explores the development of a model rocket and an accompanying STM32 based avionics data logging system. 

The electronics project focuses on collecting and recording sensor measurements, allowing data to be studied and visualized during engineering expreiments. 

# Objectives
- Explore aerospace engineering and model rocketry.
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

# Payload Ejection Plan
A motor engine would be used to propel the rocket upwards, upon hitting the apogee, the PCB would send out a tiny electrical signal to the e-matches, allowing the nose cone to release, the nose cone and the rest of the rocket body is connected through a shock cord, where the parachute would be opened closer to the nose cone instead, giving a large space for the flight controller to be released. This flight controller will  then measure altitude, atmospheric pressure, acceleration, and more, all of which is written onto an microSD card within the rocket flight controller itself. 

# Development tools 
- KiCAD: PCB and schematic design
- STM32CubeIDE: Embedded development
- OpenRocket software: Rocket designing 

# Safety 
This repository documents an educational aerospace engineering project. Any physical rocketry activities must follow applicable laws, recognized model rocketry safety standards and qualified adult supervision. 

The electronics documentation is **NOT** an instruction manual for constructing or operation propulsion or pyrotechnic systems. 

# BOM 
|Part                                                                                                                    |Type      |Quantity|Unit price (USD)|Line total (USD)|Link                                                                                                                                                                                                                                                                                                              |Vendor         |Funding|Notes                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------|--------|----------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|-------|---------------------------------------------------------------------------|
|STM32F722RET6                                                                                                           |Part      |1       |11.30           |11.30           |https://www.lcsc.com/product-detail/C118207.html?s_z=n_q_STM32F722RET6                                                                                                                                                                                                                                            |LCSC           |Grant  |Main microcontroller chip                                                  |
|ICM-45686                                                                                                               |Part      |1       |10.31           |10.31           |https://www.lcsc.com/product-detail/C22459454.html?s_z=n_q_ICM-45686                                                                                                                                                                                                                                              |LCSC           |Grant  |Motion sensor data acquisition                                             |
|BMP580                                                                                                                  |Part      |1       |1.21            |1.21            |https://www.lcsc.com/product-detail/C22391138.html?s_z=n_q_BMP580                                                                                                                                                                                                                                                 |LCSC           |Grant  |Atmospheric pressure measurement                                           |
|USB Type-C 16P SMT                                                                                                      |Part      |1       |0.60            |0.60            |https://www.lcsc.com/product-detail/USB-Connectors_hanxia-HX-TYPE-C-16P-SMT-J2-0_C42453849.html                                                                                                                                                                                                                   |LCSC           |Grant  |Programming and data transfer                                              |
|4.7kΩ resistor                                                                                                          |Part      |1       |0.32            |0.32            |https://www.lcsc.com/product-detail/C99782.html                                                                                                                                                                                                                                                                   |LCSC           |Grant  |I2C communication                                                          |
|ST USBLC6-2SC6                                                                                                          |Part      |1       |0.82            |0.82            |https://www.lcsc.com/product-detail/esd-and-surge-protection-tvs-esd_stmicroelectronics-usblc6-2sc6_C7519.html                                                                                                                                                                                                    |LCSC           |Grant  |ESD protection                                                             |
|SMD tactile push button, 4 pins                                                                                         |Part      |1       |0.50            |0.50            |https://www.lcsc.com/product-detail/C49234134.html?s_z=n_q_l_tactile%2520switch%2520SMD                                                                                                                                                                                                                           |LCSC           |Grant  |Reset and BOOT button                                                      |
|HONGLITRONIC PSC-1608U52GC-G4                                                                                           |Part      |1       |0.74            |0.74            |https://www.lcsc.com/product-detail/C22371297.html?s_z=n_q_0603%2520LED%2520green                                                                                                                                                                                                                                 |LCSC           |Grant  |Status LED                                                                 |
|Samsung Electro-Mechanics CL10B104KB8NNNC                                                                               |Part      |1       |0.72            |0.72            |https://www.lcsc.com/product-detail/C1591.html?s_z=n_q_t_100nf%25200603%2520capacitor                                                                                                                                                                                                                             |LCSC           |Grant  |Decoupling capacitors                                                      |
|Samsung Electro-Mechanics CL10A106KP8NNNC                                                                               |Part      |1       |0.41            |0.41            |https://www.lcsc.com/product-detail/C19702.html?s_z=n_q_t_10uF%25200603%2520capacitors                                                                                                                                                                                                                            |LCSC           |Grant  |Bulk capacitor                                                             |
|2.54mm, 1×04 pin header                                                                                                 |Part      |1       |1.03            |1.03            |https://shopee.com.my/Straight-Pin-Header-MALE-Single-Double-Row-2p-3p-4p-10p-40p-2.54mm-Pitch-i.678234279.17653071533?extraParams=%7B%22display_model_id%22%3A58675164377%2C%22model_selection_logic%22%3A2%7D&image_ids=my-11134207-7r990-ly9mj2d9bfqhc3                                                        |Shopee Malaysia|Grant  |debugging                                                                  |
|HRS DM3D-SF                                                                                                             |Part      |1       |1.60            |1.60            |https://www.lcsc.com/product-detail/C719027.html                                                                                                                                                                                                                                                                  |LCSC           |Grant  |MicroSD card holder                                                        |
|DIODES AP2112K-3.3TRG1                                                                                                  |Part      |1       |0.92            |0.92            |https://www.lcsc.com/product-detail/C51118.html?s_z=n_q_%2520C51118&globalKeyword=%2520C51118                                                                                                                                                                                                                     |LCSC           |Grant  |converts raw power input to save voltage level                             |
|DIODES B130-13-F                                                                                                        |Part      |1       |0.46            |0.46            |https://www.lcsc.com/product-detail/C134423.html                                                                                                                                                                                                                                                                  |LCSC           |Grant  |Protects the circuit if battery is placed incorrectly                      |
|UNI-ROYAL 0603WAF5101T5E                                                                                                |Part      |1       |0.16            |0.16            |https://www.lcsc.com/product-detail/C23186.html?s_z=n_q_C23186&globalKeyword=C23186                                                                                                                                                                                                                               |LCSC           |Grant  |tie CC1 and CC2 to GND                                                     |
|AOS AO3400A                                                                                                             |Part      |1       |0.45            |0.45            |https://www.lcsc.com/product-detail/C20917.html?s_z=n_q_C20917&globalKeyword=C20917                                                                                                                                                                                                                               |LCSC           |Grant  |Ignites parachutes when MCU detects apogee                                 |
|UNI-ROYAL 0603WAF1002T5E                                                                                                |Part      |1       |0.22            |0.22            |https://www.lcsc.com/product-detail/C25804.html?s_z=n_q_C25804&globalKeyword=C25804                                                                                                                                                                                                                               |LCSC           |Grant  |Manages boot configuration, ensures clean SD logging, and measures battery.|
|PCB manufacturing                                                                                                       |PCB       |1       |15.00           |15.00           |https://jlcpcb.com                                                                                                                                                                                                                                                                                                |jlcpcb         |Grant  |Rocket flight controller PCB manufacturing                                 |
|Print Legion                                                                                                            |3D printed|1       |30.00           |30.00           |https://printlegion.hackclub.com                                                                                                                                                                                                                                                                                  |print legion   |Grant  |Rocket body                                                                |
|GNB LiHV 2S 7.6V 1100mAh 60C XT30 LiPo Battery Long Range                                                               |Part      |1       |12.00           |12.00           |https://epicfpv.ca/products/gnb-lihv-2s-7-6v-1100mah-60c-xt30-lipo-battery-long-range-1?variant=60800320405790&country=MY&currency=MYR&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&srsltid=AYCX9vIx-3YrB9azhgDblcEGwU8ssDDiMy9BJdyDTWHyMrJqba1CQkDj8P8             |epicFPV        |Grant  |Battery for electronics and e-matches                                      |
|For Amass XT30PW Male For PCB Board Plug Banana Golden XT30 Connector Black 3.6mm 90 Degrees Right Angle XT30PW-M36 5NRT|Part      |1       |4.50            |4.50            |https://shopee.com.my/For-Amass-XT30PW-Male-For-PCB-Board-Plug-Banana-Golden-XT30-Connector-Black-3.6mm-90-Degrees-Right-Angle-XT30PW-M36-5NRT-i.348385455.53262738873?extraParams=%7B%22display_model_id%22%3A416107095660%2C%22model_selection_logic%22%3A3%7D&image_ids=sg-11134201-823p2-mp3yeoidr56oc4       |Shopee Malaysia|Grant  |Battery connector                                                          |
|Pyro screw terminals                                                                                                    |Part      |2       |1.00            |2.00            |https://shopee.com.my/2P-3P-4P-5P-6P-7P-8P-9P-10P-Pitch-2.54mm-3.81mm-5.00mm-5.08mm-Terminal-Block-Connector-PCB-DIY-Wire-Cable-KF128-i.90748406.20850140188?extraParams=%7B%22display_model_id%22%3A213007401440%2C%22model_selection_logic%22%3A3%7D&image_ids=my-11134207-7r98y-lwi43m3xsdwqa6                 |Shopee Malaysia|Grant  |Pyro e-matches ejector                                                     |
|E-matches for pyro system                                                                                               |Part      |1       |30.00           |30.00           |https://shopee.com.my/Electric-Ignitor-1m-2m-3m-E-Match-Talon-Firing-System-Rocket-Feux-D'artific-Fuse-Igniter-Pyrotechnic-i.251684114.26121992227?extraParams=%7B%22display_model_id%22%3A345451400630%2C%22model_selection_logic%22%3A3%7D&image_ids=my-11134207-7rase-m8e4x92ee8ms73                           |Shopee Malaysia|Grant  |E-matches for parachute system                                             |
|Heat resistant recovery wadding                                                                                         |Part      |1       |6.41            |6.41            |https://www.apogeerockets.com/Building-Supplies/Recovery-Equipment/Disposable-Wadding/Estes-Recovery-Wadding                                                                                                                                                                                                      |Estes          |Grant  |Protects the parachute fabric                                              |
|Parachute                                                                                                               |Part      |2       |10.00           |20.00           |https://estesrockets.com/products/rip-stop-parachute                                                                                                                                                                                                                                                              |Estes Rocket   |Grant  |Slow decent for the rocket                                                 |
|C6-0 Engines                                                                                                            |Part      |1       |15.00           |15.00           |https://estesrockets.com/products/c6-0-engines                                                                                                                                                                                                                                                                    |Estes Rocket   |Grant  |Rocket propulsion engine                                                   |
|3mm shock cords                                                                                                         |Part      |1       |0.35            |0.35            |https://shopee.com.my/1-1.5-2-.2.5-3-4-5mm-Length-2M-Black-Round-Elastic-Cord-Beading-Stretch-Thread-String-Rope-for-Necklace-Bracelet-Jewelry-Making-i.190957605.29855430851?extraParams=%7B%22display_model_id%22%3A139003971739%2C%22model_selection_logic%22%3A3%7D&image_ids=cn-11134207-7r98o-lxs0i2cxw8clb5|Shopee Malaysia|Grant  |Shock cords holding nose cone and rocket body                              |
|Total                                                                                                                   |          |        |                |167.03          |                                                                                                                                                                                                                                                                                                                  |               |       |                                                                           |

# Project pictures 

**Schematics**

<img width="1350" height="831" alt="image" src="https://github.com/user-attachments/assets/cce0d5b8-31d9-43df-8252-6c88c7a6923e" />

**PCB**

<img width="741" height="732" alt="Screenshot 2026-11-12 021925" src="https://github.com/user-attachments/assets/61cab373-5f29-4301-b85b-588c4785163a" />

**PCB 3D RENDERED**

<img width="663" height="667" alt="Screenshot 2026-11-12 021939" src="https://github.com/user-attachments/assets/4a6a556c-688f-4918-9de5-0de1931d1668" />


**Avionics Bay**

<img width="481" height="571" alt="image" src="https://github.com/user-attachments/assets/0079ad6d-ba7c-4d86-99c4-7617014c6693" />


