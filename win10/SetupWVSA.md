---
layout: default
title: SetupWindowsVirualShieldsArduino
permalink: /win10/SetupWVSA.htm
---

#Get Started

This section explains how to set up your Windows Virtual Shields for Arduino!

{% include steps.html device="WVSA" %}

#Setup for Windows Virtual Shields for Arduino (Arduino and PC)

##Hardware

###What you need
 1. Arduino Uno or compatible device.
 2. Bluetooth module: [SparkFun BlueSMiRF Silver](https://www.sparkfun.com/products/12577) and 4 wires to connect.

###Set up your Arduino
 1. Prepare the Bluetooth module if necessary (the Bluetooth module may need to have headers soldered onto it).
 2. Except for one difference below, connect the Bluetooth module to the Arduino per your wiring diagram ([BlueSMiRF wiring diagram](https://learn.sparkfun.com/tutorials/using-the-bluesmirf/hardware-hookup)).

		DIFFERENCE: Use pins 0 and 1 instead of 2 and 3:
		The Bluetooth TX should connect to pin 0 (Arduino RX).
		The Bluetooth RX should connect to pin 1 (Arduino TX).

##Software

###What you need
 1. Arduino IDE 1.6 or better.
 2. ArduinoJson library.
 3. This [repository](https://github.com/ms-iot/virtual-shields-arduino).

###Set up your Arduino IDE
 1. Download and install the [Arduino IDE](http://www.arduino.cc/en/Main/Software).
 2. Try downloading an empty sketch (setup and loop only) to make sure that your board and port settings are correct (found under the Tools menu).

###Set up ArduinoJson library
 1. From the [ArduinoJson repository](https://github.com/bblanchon/ArduinoJson), clone the repository or download the zip.
 2. Place the whole repository into your libraries folder (i.e. Documents\Arduino\libraries\ArduinoJson\).

###Set up this repository.
 1. Clone this [repository](https://github.com/ms-iot/virtual-shields-arduino) or download the zip.
 2.	Copy the Arduino/libraries/VirtualShield folder from your repository to your Arduino library (i.e. Documents\Arduino\libraries\VirtualShield\).

###Test your setup
 1. From the Arduino IDE, go to the menu item File->Examples->Virtual Shields->Hello Blinky. This should load the Hello Blinky example.
 2. Before uploading, temporarily remove the Bluetooth TX and RX wires from the Arduino. (There is only one serial port shared between the USB and Bluetooth. The Bluetooth interferes with the upload).
 3. Upload the sketch.
 4. Replace the Bluetooth TX and RX wires into the Arduino pins. (Bluetooth TX to Arduino RX and Bluetooth RX to Arduino TX).
 5. In order to see anything on the phone, you will need to go to the next step (Set up your Phone and PC).