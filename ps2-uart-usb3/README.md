# USB3 to PS2/UART adapter

PS2-UART-USB3 is a passive adapter between USB3 and PS2 connector (mouse+keyboard). It also offers an UART header (Rx/Tx/GND). 

**STATUS**: working Ok. See testing and improvement notes below.

See correspondence of pins in [schematic](pmod.pdf). 

PS2 connector has all signal pins connected so a splitter cable can be used to connect a PS2 keyboard and mouse.

JP1 header is for selecting power supply of PS2 connector. Three options are possible:

* 5V: Place a jumper between VBUS and central pin
* 3V3: Place a jumper between 3V3 and central pin. For this is required a MiSTer Analog IO version with a jumper that connects 3V3 to pin 9 of USB3.
*  External power supply can also be connected to the central pin and GND.



**NOTES ABOUT USB3 CABLES**

* male male cable is crossover cable, meaning that Rx- is connected to Tx- and Rx+ to Tx+

* female male cable is straight cable, meaning all pins have exact correspondence in each side of cable (Rx- with Rx-, ...)

  

**SETUP IN MISTER DE10-nano FPGA**

* Connect  an [SNAC level shifter adapter](https://manuferhi.com/p/snac-adapter-for-mister) to the user IO port of MiSTer Analog addon

* Connect a male male USB3 cable between the SNAC adapter and the USB3 to PS2 adapter

* Connect a [PS2 splitter cable](https://es.aliexpress.com/item/32827138560.html) if you intend to use keyboard and mouse simultaneously.

  

**TODO**

* Shield pins of PS2 connector are not connected to GND
* 3V3 silkscreen NOTE at pcb back "3V3 from MiSTer analog IO with user IO jumper placed"

**IMPROVEMENTS**

* Make a male USB3 version to avoid having to connect a male to male cable
* Make a male USB3 version with voltage protections so the SNAC adapter would be unnecessary

**TESTING**

* Tested using PMOD-USB3 adapter: UART, keyboard and mouse works well, with 3V3 without SNAC adapter, or with 5V and SNAC level shifter adapter.  This means in MiSTer should work.

  NOTE: Code in FPGA side need to take into account the crossover signals of the male to male cable.

* Tested from USB3 port of Deca cape: Keyboard not working good with the integrated level shifter of Deca cape.
