# PMOD to USB3 adapter

PMOD-USB3 is a passive adapter between PMOD and USB3. Only 7 pins are wired as is the maximum of USB3. 

**STATUS**: tested with a GEN SMS SNAC with a gamepad working well with 3V3



See correspondence of pins in [schematic](pmod.pdf). 

PMOD only outputs 3V3. 

JP1 header is for detaching power supply pin from both connectors, as PMOD is 3V3 and VBUS is usually 5V. 

JP1 header header has three pins: 3V3 from PMOD, VBUS from USB3 and GND. 

VBUS is the power supply to whatever is connected to the SNAC adapter. 



Different power supply options:

* Placing a jumper between 3V3 and VBUS will not work on all gamepads. 

* Other option is to connect 5V wire from FPGA to VBUS pin   (note that this will require to use a SNAC level shifter in between for protecting 3V3 GPIO)

* Third option would be to get 5V from external power supply so you will need to connect two wires: VBUS to 5V and GND (SNAC level shifter required also).

  

**PLEASE MAKE SURE NOT TO PLACE A JUMPER EVER BETWEEN VBUS AND GND PINS. I'm not responsible for what could happen.**