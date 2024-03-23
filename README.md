# PATCH
PATCH is a simple modular patchbay project for Eurorack.

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20Perspective.jpg">
</p>

PATCH started with an application to develop a simple interface to my [UMC1820 Audio Interface](https://www.behringer.com/product.html?modelCode=0805-AAN) and my [FX2000 Effects Processor](https://www.behringer.com/product.html?modelCode=P0A3P), both of which have rear-mounted audio I/O and require some attentuation to allow them to accept modular audio levels. 

The basic PATCH configuration which services this motivating application, seen in the photo above, is realised by three components: a front panel, a socket board, and a passive board. 

The passive board includes pi networks between the 3.5mm jack sockets at input and output of each channel and provides options to normal the 'tip switches' on the jacks to ground if the channel is configured as an input. Partially populating the resistors of the pi network gives the option to set up a potential divider to drop the signal level in either direction, or to set a unity gain 'straight wire' connection. The system shown above has a 24dB pad on the top two channels and two send/return loops on the next four sockets, with 12dB pads on the sends and straight-wire returns.

The minimum order quantity at [JLC](https://jlcpcb.com/) (typical of all pcb houses) for the front panel and socket board left me with some spare resources after I'd finished my interface to the Behringer "off-board" units, so I also develped a passive multiple board, and a buffered multiple board, so as not to waste the relatively expensive front panels. These share the front panel and the socket board, but use a different final board. The complete set of PATCH system panels are seen below.



The system is described in the hardware folder, where schematics, PCB layouts and front panel designs are presented.

There may be more additions to the PATCH system in future - watch this space.

PATCH is published under [CC BY-SA 4.0 license.](https://github.com/m0xpd/PATCH/blob/main/LICENSE.txt)



