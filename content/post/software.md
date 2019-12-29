+++
title = "software for bewegungsappar.at"
description = ""
date = "2019-12-29"
image = 'img/software.png'
menu = "main"
+++

# Motor Control
Heavily modified version of the hoverboard-firmware-hack software. See https://github.com/bipropellant/bipropellant-hoverboard-firmware.
Added features include sensor Feedback and an advanced serial protocol as well as sinus commutation and some safety features.

Currently used branch is here: https://github.com/p-h-a-i-l/bipropellant-hoverboard-firmware/tree/protocolCOBSR with lots of stability improvements for the serial protocol.

# Wireless communication
Relaying of the Serial protocol via WiFi with UDP between some ESP32 microcontrollers.
Currently used code here: https://github.com/bewegungsappar-at/hoverboard-control/tree/protocolCOBSR

# Paddel Algorithm
A 6-Axis IMU is used to sense the movement of the driver. The Acceleration sensor is used to get an absolute value of the paddle angle, when tilted to one side, the gyro values are used to calculate the paddle tip speed.
The paddle tip speed is then compared with the actual wheel speed and based on the difference, the speed is adjusted