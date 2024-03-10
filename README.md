# PATCH
PATCH is a simple modular patchbay project for Eurorack.

PATCH started with an application to develop a simple attentuating interface to my [UMC1820 Audio Interface](https://www.behringer.com/product.html?modelCode=0805-AAN) and my [FX2000 Effects Processor](https://www.behringer.com/product.html?modelCode=P0A3P). 

The basic patchbay which services this motivating application is realised by a front panel, a socket board, and a passive board. 

The passive board includes pi networks between the 3.5mm jack sockets at input and output of each channel and provides options to normal the 'tip switches' on the jacks to ground if the channel is configured as an input. Partially populating the resistors of the pi network gives the option to set up a potential divider to drop the signal level in either direction, or to set a unity gain 'straight wire' connection.

The minimum order quantity at [JLC](https://jlcpcb.com/) for the front panel and socket board left me with some spare resources, so I also develped a passive multiple board, and a buffered multiple board.

The system is described in the hardware folder, where schematics, PCB layouts and front panel designs are presented.

PATCH is published under [CC BY-SA 4.0 license.](https://github.com/m0xpd/PATCH/blob/main/LICENSE.txt)



