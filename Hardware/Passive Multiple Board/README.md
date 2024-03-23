# Passive Multiple Board

This folder contains design files for the Passive Multiple Board which (in conjuntion with the Socket Board and Front Panel) form a Passive Multiple. 
The design files are presented as a [KiCad](https://www.kicad.org/) project.

The Passive Multiple Board is trivial, hosting only two 9*1 0.1 inch headers (to mount it on to the Socket Board) and containing tracks between the 
poles of these headers to make the electrical connections which define the circuit (see the Schematic).

The resulting passive multiple is organised as two 1 in, 2 out sections, with the input to the second section normalled to the output of the first, 
such that the module can be operated as two 1 -> 2 multiples or one 1 -> 4 multiple.
