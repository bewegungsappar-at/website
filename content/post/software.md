+++
title = "software for bewegungsappar.at"
description = ""
date = "2014-04-02"
image = 'img/software.png'
menu = "main"
+++

# Motor control software
Github Repo: https://github.com/p-h-a-i-l/hoverboard-firmware-hack (based on [hoverboard-firmware-hack](https://github.com/NiklasFauth/hoverboard-firmware-hack))

Modified code with lots of improvements with a focus on serial communication and parallel use of ADCs as input. "transpotter" like control can be configured just via parameters.

Changes to [hoverboard-firmware-hack](https://github.com/NiklasFauth/hoverboard-firmware-hack)

* Build Environment is platform.io. Old Makefile based system should work too, but not tested.
* UART Control can be configured to Connect to USART2 or USART3
* Added CRC Checksum to UART Control. This way, the protocol just loses sync but the board does not try to kill you anymore (at least less often)
* UART Control and Debug can be active on the same cable
* Extended ADC Input Control config options. Default is platooning / "transpotter"
* ADC Input Control can coexist with all other control Methods as long as the other Method uses the other cable
* Watchdog Implemented which monitors if main is still running. Stops motors and shuts down if not.
* Serial Protocol implemented (very shrunk down version from [btsimonhs pidcontrol](https://github.com/btsimonh/hoverboard-firmware-hack))
  * PWM can be set and read
  * Human readable ASCII Protocol can coexist with machine parseable Messages
  * Buzzer commands
  * Hall Interrupts for Speed Feedback

# Wireles Interface Module and Paddelec Remote Control
ESP32 with Acceleration Sensor and Gyro, OLED Display. Serial communication to Motor control board, ESPnow link between ESPs.

see https://git.hacknology.de/phail/bewegungsappar.at_control