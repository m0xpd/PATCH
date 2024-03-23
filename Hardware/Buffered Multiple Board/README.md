# Buffered Multiple Board

This folder contains design files for the Buffered Multiple Board which (in conjuntion with the Socket Board and Front Panel) form an active, Buffered Multiple. 
The design files are presented as a [KiCad](https://www.kicad.org/) project.

The Buffered Multiple Board hosts two 9 * 1, 0.1 inch headers (to mount it on to the Socket Board),  a standard 2*5 Eurorack Power Header and filtering capacitors. 
It also hosts a quad op-amp (I used a TL084, but anything similar will work), the stages of which are used as voltage followers, and a few resistors to set the 
input and source impedance. 

The resulting buffered multiple is organised as two 1 in, 2 out sections, with the input to the second section normalled to the output of the first, 
such that the module can be operated as two 1 -> 2 multiples or one 1 -> 4 multiple.
