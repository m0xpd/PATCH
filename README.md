# PATCH
PATCH is a simple modular patchbay project for Eurorack.

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20Perspective.jpg">
</p>

PATCH started with an application to develop a simple interface to my [UMC1820 Audio Interface](https://www.behringer.com/product.html?modelCode=0805-AAN) and my [FX2000 Effects Processor](https://www.behringer.com/product.html?modelCode=P0A3P), both of which have rear-mounted audio I/O and require some input attentuators to allow them to work as I wish in my system. A patchbay is the perfect way to impose order on the tangle of wires, to avoid searching on the back of cases (especially if they're stacked or racked) and is also the logical place to implement attenuating pads, where required. 

The image below shows two PATCH patchbay modules (inside the yellow rounded rectangle) implementing the complete interface to the UMC1820 and FX2000

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patchbay%20in%20Action.png">
</p>

Note that the UMC1820 [does not need attenuators to handle modular signals directly](https://modwiggler.com/forum/viewtopic.php?p=2936306#p2936306). Indeed, it is specified to be capable of handling inputs up to +18dBu. However, this requires that the inputs are set to LINE (obviously), that the PADs are applied, and the GAIN controls are set way down near the bottom of their travel. I have been pleased to discover that in addition to service as front end of a DAW (or similar application), the UMC1820 also operates usefuly as a stand-alone mixer, with 8 channels going in and direct output to the system monitors. In this role, some external attenuation on the inputs is helpful, as it allows the GAIN controls to operate as Level 'faders' over a wider range, with more useful resolution. On the other hand, the FX2000 is specified only to handle inputs up to +4dBu and my modular was easily able to overload its inputs; an external attenuator is certainly required in this case. 

The basic PATCH configuration which services this motivating application, seen in the photos above, is realised by three components: a [front panel](https://github.com/m0xpd/PATCH/tree/main/Hardware/Front%20Panel#readme), a [socket board](https://github.com/m0xpd/PATCH/tree/main/Hardware/Socket%20Board#readme), and a [passive board](https://github.com/m0xpd/PATCH/tree/main/Hardware/Passive%20Board#readme). 

The passive board includes pi networks between the 3.5mm jack sockets at input and output of each channel and provides options to normal the 'tip switches' on the jacks to ground if the channel is configured as an input. This tip normalisation is achieved using 1206 surface mount (0 Ohm) resistors (as I figure not many people will bother to use them), whilst the rest of the board uses through-hole components. Partially populating the resistors of the pi network gives the option to set up a potential divider to drop the signal level in either direction, or to set a unity gain 'straight wire' connection. The system shown above has a 24dB pad on the top two channels and two send/return loops implemented on the next four sockets, with 12dB pads on the sends and straight-wire returns.

Populating the pads is up to you - I'm using a 15k / 1k potential divider for the -24dB and 3k3 / 1k1 potential divider for the -12dB. HOWEVER, you should remember that the device you're plugging into has finite (and possibly LOW) input impedance, which will sit in parallel with the botttom resistor of the potential divider, so either don't take the open-circuit calculations too seriously, or account for this loading in your design!

The Passive board, which makes up PATCH's standard patchbay configuration, houses a set of 3.5mm sockets which face to the rear, mirroring those on the front panel. Standard Eurorack patch leads (or other leads made up for custom applications, such as the 3.5 mm to 6.5mm right angle jacks I've made to hook up to the back of my FX2000) connect to these sockets, when the patchbay is used in the modular:

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patching%20in%20the%20Modular.jpg">
</p>

***

The minimum order quantity at [JLC](https://jlcpcb.com/) (typical of all pcb houses) for the front panel and socket board left me with some spare resources after I'd finished my interface to the Behringer "off-board" units, so I also develped a [passive multiple board](https://github.com/m0xpd/PATCH/tree/main/Hardware/Passive%20Multiple%20Board#readme), and a [buffered multiple board](https://github.com/m0xpd/PATCH/tree/main/Hardware/Buffered%20Multiple%20Board#readme) so as not to waste the relatively expensive Aluminium front panels. 

These multiples share the front panel and the socket board with the basic patchbay design, but use a different final board. 

The complete set of PATCH system panels are seen below.

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20Elements.jpg">
</p>

Both the passive multiple and the buffered multiple are organised as two 1 in, 2 out sections, with the input to the second section normalled to the output of the first, such that the multiple can be operated as two 1 -> 2 units or one 1 -> 4 unit.

A PATCH buffered multiple is seen below:

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Buffered%20Mult%20Side.jpg">
</p>

All the system components are described in the [hardware folder](https://github.com/m0xpd/PATCH/tree/main/Hardware#readme), where schematics, PCB layouts and front panel designs are presented as [KiCad](https://www.kicad.org/) projects.

# PATCH Multicore

The PATCH system now (as at 5 June 2024) also has a multicore option, realised by a pair of boards. The multicore functionality was first suggested by "CoogLFish", within the "Issues" section of this repo and whose inspiration is acknowledged.

The boards are offered in two forms. First, the ["low budget"](https://github.com/m0xpd/PATCH/tree/main/Hardware/RJ45%20Board#readme) option uses a single UTP cable to join two modules to make a six channel multicore]. Second, the ["high end" alternative](https://github.com/m0xpd/PATCH/tree/main/Hardware/Twin%20RJ45%20Board#readme) uses two UTP cables to achieve the same goal with the possibility of slightly better crosstalk performance. This "Twin" system will also work with cables with shielded twisted pairs such as CAT8 and offer some performance advantages - but I have not yet formally tested this to determine how big the performance advantage (over either the single cable solution or UTP cables) really is. I use CAT6 cables over 1.5m and have not yet noticed issues.

# Other PATCH System Components

There may be still more additions to the PATCH system in future - I have a couple more ideas, but there are lots of other potential projects competing for attention, so watch this space, but don't hold your breath.

# License

PATCH is published under [CC BY-SA 4.0 license.](https://github.com/m0xpd/PATCH/blob/main/LICENSE.txt)



