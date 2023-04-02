# USB3 to PS2/UART adapter

PS2-UART-USB3 is a passive adapter between USB3 and PS2 connector (mouse+keyboard). It also offers an UART header (Rx/Tx/GND). 



**STATUS**: untested 



See correspondence of pins in [schematic](pmod.pdf). 

PS2 connector has all pins connected so a splitter cable can be used to connect a PS2 keyboard and mouse.



JP1 header is for selecting power supply of PS2 connector. Three options are possible:

* 5V: Place a jumper between VBUS and central pin
* 3V3: Place a jumper between 3V3 and central pin. For this is required a MiSTer Analog IO version with a jumper that connects 3V3 to pin 9 of USB3.
*  External power supply can also be connected to the central pin and GND.



**TODO**

* Shield pins of PS2 connector are not connected to GND
