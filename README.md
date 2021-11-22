# WATER TANK CONTROLLER

### Team members

* Filip Kocum, 22xxxx (responsible for xxx)
* Martin Knob, 22xxxx (responsible for xxx)
* Gregor Karetka, 22xxxx (responsible for xxx)
* Samuel Košík, 221056, (crying, not helping)

Link to this file in your GitHub repository:

[https://github.com/amwellius/DE2_Project_2021-22](https://github.com/amwellius/DE2_Project_2021-22)

### Table of contents

* [Project objectives](#objectives)
* [Hardware description](#hardware)
* [Libraries description](#libs)
* [Main application](#main)
* [Video](#video)
* [References](#references)

<a name="objectives"></a>

## Project objectives

Write your text here.

<a name="hardware"></a>

## Hardware description

### Arduino Uno + breadboard 
[Datasheet](https://github.com/amwellius/DE2_Project_2021-22/blob/main/Datasheets%20%2B%20DOCs/ATMega_328P_datasheet.pdf)

&nbsp;
![ASI NEJAKA VLASTNA FOTKA](Images/obrazok.png)
&nbsp;

### Nokia 5110 LCD display 
[Datasheet](https://github.com/amwellius/DE2_Project_2021-22/blob/main/Datasheets%20%2B%20DOCs/Nokia5110_datasheet.pdf)

&nbsp;
![asi tiez vlastny obrazok](Images/obrazok.png)
&nbsp;

### RGB LED, Relay Modules (1, 2, or 4 relays) ...........PARTICULAR..........
[Datasheet](link)

&nbsp;
![figure](Images/obrazok.png)
&nbsp;

### UltraSonic sensor HC-SR04
[Datasheet](https://github.com/amwellius/DE2_Project_2021-22/blob/main/Datasheets%20%2B%20DOCs/HCSR04.pdf)

&nbsp;
![figure](Images/HCSR04.png)
&nbsp;

**TIEZ ASI RADSEJ VLASTNY OBRAZOK**

Main sensor (one of **two???**) for measuring the water level of the tank. After entering its dimensions (or volume), the sensor is calibrated. Providing it with short 10us pulse will result in receiving 8 cycles of 40MHz signal. This will be given by *ECHO pin*, so received value will the time the wave travelled to the watel level and back to the sensor. Final distance can be obtained by this equation: 

&nbsp;
![equation](Images/HCSR04_equation.gif)
&nbsp;

Where **t** is the received value on **ECHO pin** and *0.034* cames from ste speed of soun *(340 m/s = 0.034 m/us)*. Sound wave travels from sensor to water, but from water to the sensor as well. That is why the result has to be devidec by two. 




<a name="libs"></a>

## Libraries description

Write your text here.

<a name="main"></a>

## Main application

**OBRAZOK AKO TO CELE VYZERA/T BUDE**

The main purpose of this application is to automatize operation of regulating water level in specified tank. After knowing volume of tank, ultrasonic sensor connected to **Arduino UNO** board will measure the water level. LCD Nokia 5110 display shows *water level in cm, percenttage and max usable volume of the water-tank. Application uses one more sensor **??????** to control the max volume. In normal conditions, sensor all time gives negative data of water level. It is situated few centimeters above the max bound of water (we do not want to fill the tank completely to prevent owerflow). If the water reaches this sensor, ultrasonic has occurred hassle and LCD shows problem ("Dirty water", "Hardware issue", ...).

Our product has **(2)** relays for external usage. These can be used to replenish the tank, irrigation pump control, DC fans, windows opening, and others. 
<a name="video"></a>

## Video

Write your text here

<a name="references"></a>

## References

1. Write your text here.
