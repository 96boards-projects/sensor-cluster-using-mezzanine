# Sensor Cluster using Sensors Mezzaine on DragonBoard410c
The sensor cluster project basically aims at working with as many sensors as possible, making use of the [Grove Starter Kit for the 96Boards](https://www.seeedstudio.com/Grove-Starter-Kit-for-96Boards-p-2618.html) and a Sensors Mezzanine board with a DragonBoard410c.


# Table of Contents
- [1) Hardware](#1-hardware)
   - [1.1) Hardware Requirements](#11-hardware-requirements)
   - [1.2) Hardware Setup](#12-hardware-setup)
- [2) Software](#2-software)
   - [2.1) Software Requirements](#21-software-requirements)
- [3) Building and running](#3-building-and-running)
- [4) Conclusion](#4-conclusion)

# 1. Hardware

## 1.1 Hardware Requirements:

1. [DragonBoard 410c](http://www.96boards.org/product/dragonboard410c/)
2. [Power Supply](https://www.amazon.com/Adapter-Regulated-Supply-Copper-String/dp/B015G8DZK2)
3. [Sensors Mezzanine](http://www.96boards.org/product/sensors-mezzanine/)
4. [Micro USB Cable](https://www.amazon.com/AmazonBasics-USB-Male-Micro-Cable/dp/B01EK87A82/ref=sr_1_3?ie=UTF8&qid=1497618343&sr=8-3&keywords=micro%2Busb&th=1) (optional- only if you plan to use the serial console via ssh or screen)
5. [Grove Starter Kit for 96Boards](https://www.seeedstudio.com/Grove-Starter-Kit-for-96Boards-p-2618.html)

## 2.2 Hardware Setup:
Initially, make sure that the DragonBoard 410c is unplugged (powered off). Conect the Sensors Mezzanine to DragonBoard 410c through the 40 pin low-speed expansion connector. Mezzanine board (male pins) will match 1-to-1 with female pins on DragonBoard 410c connector. Make sure all 40 pins are lined up properly before moving to next step. Then connect the sensors using Grove Universal 4 pin Connectors as follows:
 - A0 --> Light Sensor
 - A1 --> Temperature Sebsor
 - A2 --> Sound Sensor
 - D4 --> Touch Sensor Module
 - D5 --> Button
 - D6 --> Rotary Angle Sensor

# 2. Software

## 2.1 Software Requirements:
Now, I executed this entire project on the Arduino toolchain. If you don't have Arduino toolchain setup on your DragonBoard, refer to [this](https://github.com/sdrobertw/guides/blob/master/arduino-setup.md) guide in order to get started.

# 3. Building and Running:

```shell
$ git clone https://github.com/96boards-projects/sensor-cluster-using-mezzanine.git
```
Open the Arduino IDE. Click on Open and from the browser select sensor-cluster-using-mezzanine.ino.
Click on verify to verify the program. Then click on upload. This will ccompile the code and upload it onto the DragonBoard. Once that is done, click on the serial monitor icon on the top right corner.

## Conclusion:

You can see the results on the Serial Monitor where all the sensor values are displayed in the form of a table.
