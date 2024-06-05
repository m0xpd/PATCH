# PATCH Twin RJ45 Board

This folder contains details of a Twin RJ45 board, which allows the Patch system to use two CAT5 (or better) cables to provide a six channel link 
between two locations in large a modular case. This idea was propted by a suggestion made in response to the initial Patch system by "CoogLFish" - 
to whom I am grateful. 

The Twin RJ45 board is seen below in populated and unpopulated form:
<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20Twin%20RJ45%20Board.jpg">
</p>

The signals from all six sockets on the Patch socket board are passed down three pairs of conductors in each cable connected to the RJ45 sockets. 
These conductor pairs are arranged in twisted pairs, which should help to slichtly reduce crosstalk between channels (although - of course - these 
are not balanced pairs as they would be in data or balanced audio interfaces). If you really want to go mad, you could use CAT8 cables with individual
screening around each pair - but if you care that much, you're probably already too busy chasing Unicorns.

The assembled module is seen below:
<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/Patch%20Twin%20RJ45%20Module.jpg">
</p>

and its role as a multicore is understood from this image:

<p width=100%, align="center">
<img width=40%, src="https://github.com/m0xpd/PATCH/blob/main/Hardware/Images/RJ45%20Multicore.jpg">
</p>

A KiCad project, formed from a project file, a schematic and a pcb file, can be found in this folder.

Like the rest of the PATCH famiy, the Twin RJ45 board is published under a CC BY-SA 4.0 [License](https://github.com/m0xpd/PATCH/blob/main/LICENSE.txt). 
