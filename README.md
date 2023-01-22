# Makers @ OU General Purpose Motor Board

![Makers Motor Board](https://github.com/Makers-Oakland-University/readme-images/blob/main/motor_board_render.png?raw=true)

The Makers @ OU motor board is meant to serve as a general-purpose robot base for all kinds of projects. 
The board utilizes the ESP32 Devkit 1, along with an L293D H-Bridge driver. 
The LM7805 voltage regulator enables the board to be powered from any supply between 4.5V and 30V. 
The input voltage can be used directly to drive the motor, or the 5V power rail can be used through selection through the header. 

This repo contains the KiCad EDA files for the board, gerber production files, the board schematic in PDF format, and a .step file to aid CAD design. 

# ESP32 Pin Connections

The following pins on the ESP32 are connected to the motor driver:

- IO26 -> Driver 1A
- IO27 -> Driver 2A
- IO23 -> Driver 3A
- IO25 -> Driver 4A
- IO32 -> Driver 1,2EN
- IO33 -> Driver 3,4EN

# BOM 
This section provides a list of components used by this board, and some amazon links that can be used to acquire them. 

- [ESP32 DevKit V1](https://www.amazon.com/ESP32-WROOM-32-Development-ESP-32S-Bluetooth-Arduino/dp/B084KWNMM4/ref=sr_1_1_sspa?crid=8881ZROOTJFK&keywords=ESP32+devkit&qid=1674351980&sprefix=esp32+devkit+%2Caps%2C108&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExU0RPNzlPNUpQTTFUJmVuY3J5cHRlZElkPUEwMzA4OTc1M080TFlWOFMxVkRGUiZlbmNyeXB0ZWRBZElkPUEwOTA5NTc0MTdUSDJMWDFHTEU4RyZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=)
- [L293D Motor Driver](https://www.amazon.com/BOJACK-16-pin-Stepper-Drivers-Controllers/dp/B09NBQVYLL/ref=sr_1_1_sspa?crid=2IHZB0VAWDBTZ&keywords=L293D&qid=1674351391&sprefix=l293d%2Caps%2C357&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExWFlUOFpBSUhMSkY4JmVuY3J5cHRlZElkPUEwNzEwMTg5MUdVTDAzMVlWUzZSTyZlbmNyeXB0ZWRBZElkPUEwNjY0MzQxUFQwMkg5TFZHT0hWJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==)
- [LM7805 Voltage Regulator](https://www.amazon.com/BOJACK-Regulator-Integrated-Circuits-Regulators/dp/B07VRS9HW4/ref=sr_1_2_sspa?crid=114WNR497M2D3&keywords=LM7805&qid=1674351959&sprefix=lm7805%2Caps%2C107&sr=8-2-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEzSTFNWldGTEYyM1ZHJmVuY3J5cHRlZElkPUEwNjMwMzEyM002TFE5SFA0UUI3MyZlbmNyeXB0ZWRBZElkPUEwMTMyMDg5MktBWFBDWjVRTEJRWiZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=)
- [2 Position 5mm Pitch Terminal Blocks](https://www.amazon.com/DIYhz-green-Terminal-Connector-Arduino/dp/B0774YRVVX/ref=sr_1_16?crid=2E3RW9V76RSA4&keywords=5mm+2+position+terminals&qid=1674352018&sprefix=5mm+2+positio+terminals%2Caps%2C109&sr=8-16)
- [Standard Header Jumpers (only need 1 per board)](https://www.amazon.com/uxcell-100pcs-Standard-Circuit-Connection/dp/B08Y7Y9LKV/ref=sr_1_4?crid=TVEIYRUGLAMC&keywords=header+jumpers&qid=1674352070&sprefix=header+jumper%2Caps%2C107&sr=8-4)

Any electrolytic capacitor can be used provided it's voltage rating is above the input voltage present at PWR IN

# Acknoledgements 
This repo uses Victor Lamoine's [ESP32 Devkit V1 Symbol and Footprint](https://gitlab.com/VictorLamoine/kicad).