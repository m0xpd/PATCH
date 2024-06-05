# PATCH RJ45 Board

This folder contains details of a RJ45 board, which allows the Patch system to use a CAT5 cable to provide a six channel link between two locations 
in large a modular case. This idea was propted by a suggestion made in response to the initial Patch system by "CoogLFish" - to whom I am grateful. 

The RJ45 board is seen below in populated and unpopulated form:
<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20RJ45%20Board.jpg">
</p>


The signals from all six sockets on the Patch socket board are passed down six of the conductors of the RJ45 cable. This idea horrifies the engineer in me, but it must work well enough, as 7 such signals are passed down the same type of cable in [this commercial solution](https://www.doepfer.de/A1809.htm) - if it's good enough for Dieter!

The RJ-45 board plugs onto the back of a [Front Panel](https://github.com/m0xpd/PATCH/tree/main/Hardware/Front%20Panel#readme) / [socket board](https://github.com/m0xpd/PATCH/tree/main/Hardware/Socket%20Board#readme) 
combination in the same way as the rest of the PATCH family to make a full module:

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20RJ45%20Module.jpg">
</p>

Two of these modules, one at either end of a standard 'network cable', make a useful multicore. In use, with a 1.5m CAT6 cable, I didn't notice any 
issues of signal loss, crosstalk or hum (etc). But the idea still horrifies me. 

So, I decided to exploit the "twisted pair" construction of network cables and build a Twin RJ45 board, which you can find [here](https://github.com/m0xpd/PATCH/tree/main/Hardware/Twin%20RJ45%20Board#readme) - to hell with the expense!

Those who want to stick with a single cable will find the KiCad design files for the single RJ-45 board in this folder - there's a KiCad project, a schematic and a PCB file.

Like the rest of the PATCH famiy, the RJ45 board is published under a CC BY-SA 4.0 [License](https://github.com/m0xpd/PATCH/blob/main/LICENSE.txt). 
