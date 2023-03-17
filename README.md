CAUTION: THOSE ADAPTERS HAVE NOT BEEN TESTED YET.

This repository is home of simple adapters between pmod/usb3 and other connectors.

* pmod-usb3 is a passive adapter between PMOD and USB3. Only 7 pins are wired as is the maximum of USB3. See correspondence of pins in schematic. JP1 header is for detaching power supply pin from both connectors, as PMOD is 3V3 and VBUS is usually 5V. User can place a jumper or connect a wire from an external power supply.
* ps2-uart-usb is a passive adapter between USB3 and PS2 connector (mouse+keyboard). It also offers an UART header (Rx/Tx). JP1 header can choose power supply to PS2 connector from VBUS (5V) or from pin 9 (3V3 if Analog IO has a jumper to wire 3V3 to this pin). External power supply can also be connected to the central pin.