---
title: "Cloud X"
github: "https://github.com/JH-2108/Cloud-X"
description: "A rocket with a custom made flight controller as the payload inside of the rocket which will be ejected upon reaching the apogee. The rocket flight controller has a GPS system placed inside of it, allowing tracking of the rocket and the electronics of it, hence ensuring that the electrical system does not get lost. "
created_at: "2026-11-08"
total_time: "10h 30m"
---

# November 9, 2026: Generated readme.md and BOM.csv
<!-- fabricate:entry 2470 -->

In order to plan out on what kind of rocket I want, what the rocket functions would be, an estimated cost of the rocket and what components the rocket needed, I created both the readme and bom first. The readme.md would tell other people who are recreating my project what this rocket can do, the features of the rocket flight controller and the type of data it will record. As for the BOM, it shows the users on what the estimated cost is and how much funding that they would need in order to recreate this project. It also took me a very long time in order to complete the entire BOM considering that i had to find multiple sources for the purchase link and rocket motors aren't easily sold in my country (Malaysia). There are still more components to consider for the bom that I haven't included yet, but I would include along the way when building the PCB, the rocket body, and the physical rocket itself. 

I also planned the type of flight data this rocket would collect, such as atmospheric pressure, altitude, acceleration, and more. The data that it collects aren't transmitted to my laptop using bluetooth, instead it writes everything to a microSD card within the PCB itself, that once I collect the rocket, it would show the flight data that it collects. This rocket also has an e-match system to allow ejection when the rocket reaches the apogee, where the pyro connections would release an electric signal to the e-match, releasing the nose cone and allowing the payload to be released, the parachute would be on the shock cord and have a short release delay considering that we need some time for the rocket payload to be released. Most of the parts had to be searched up through LCSC, where I can get their easyeda footprints and symbols converted into KiCAD, which makes it quite difficult for some other parts that are not in LCSC. 

![](https://fabricate.hackclub-assets.com/8b8ffca505bdd744d7ec488f4cbbc3a0ca08d55f0349d50d379abcae42ac37c8/image-png/image.png)

![](https://fabricate.hackclub-assets.com/3c2d48e1ad2ff1c635a61acd7b4571ebf7ccd84f49ccde8507d80ecd72774aac/image-png/image.png)

**Total time spent: 4h**

# November 10, 2026: PCB Schematics
<!-- fabricate:entry 2549 -->

Before I started designing the entire PCB, I had a session with a teacher that taught me how to design the schematic before I can continue to designing the PCB. The schematic for some components required custom made symbols and footprints that matched with it, hence I went to LCSC, get their part number used the easyeda2kicad tool in my command prompt and got some symbols for some parts. Throughout this process, I've also learnt a lot on the schematic connections, and how to properly wire something, teaching me that all I needed to do was get the symbols electrically connected properly, the symbols that are provided by easyeda also mostly told me what to do anyways, making it a little simpler. After finishing the entire schematic, I went to check with my teacher whether all of the connections are electrically accurate (I asked mainly because using ERC won't give me the answer with the unspecified connections on the custom symbols). I also realized that I forgot to add some parts, with some parts being incorrect too, I fixed up everything, assigned the footprints, and went on to PCB designing, which I will do tomorrow. 

![](https://fabricate.hackclub-assets.com/e4a76152b53d32b55c4f33437e42302d642ba643b8a5f2d871b2ddf97c9d0255/image-png/image.png)

![](https://fabricate.hackclub-assets.com/c7956947f632a32f16ec48975aa21b5b3d46cd287c3743acb661e44e32a6c230/image-png/image.png)

**Total time spent: 6h 30m**
