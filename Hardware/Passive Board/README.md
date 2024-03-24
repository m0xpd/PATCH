# Passive Board

This folder contains design files of the "Passive Board" which, in conjunction with the Front Panel and Socket Board, implements a simple six-channel patchbay. 
The design files are presented as a [KiCad](https://www.kicad.org/) project.

The Passive Board hosts six "[Thonkiconn](https://www.thonk.co.uk/shop/thonkiconn/)" 3.5mm sockets, which mirror those on the front panel and two 9*1 0.1 inch headers, which mount the Passive Board onto 
the Socket Board. 

A set of 12 positions for 1206 surface mount resistors on the bottom side of the board allow 0 Ohm links to be fitted, which normal the Tips of the sockets 
(on the Passive and Socket board) to ground, as required.

On the top side of the board, positions are provided for through hole resistors forming a "pi network" to be placed between each socket on the Socket Board and 
the corresponding socket on the Passive Board. This allows (by leaving one resistor unpopulated) for a potential divider to be fitted to attentuate the signal 
in either direction or (by fitting a 0 Ohm link - i.e. a wire  in the resistor position at the top of th 'pi' and leaving the other resistors unpopulated), making 
the channel a straight-wire connection.
