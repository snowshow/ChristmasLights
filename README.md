This is a C program compilable with the mspgcc toolchain
for a TI MSP430 microcontroller (like MSP430 launchpad).
It drives a WS2801 based string of RGB LEDs (or 2
strings, or more...) to create lights for a christmass
tree.

Copyright 2012 - Bracken Dawson - Licensed under GPLv3.

===========
CONFIGURING
===========
Edit configuration.h, it is commented. Settings
include number of LEDs, selection of patterns and
defaults. If you can't compile in the space on your
MSP430, you might try taking out some patterns.

If you like, you can define your own patterns, see
patterns/fade.h for a documented example.

===========================
MSP430 MINIMUM REQUIREMENTS
===========================
 * 4KB program memory (8KB recommended).
 * 128B RAM (256B recommended).
 * DCO.
 * TimerA0.
 * USI.

I use the MSP430G2452 that comes with more recently
shipped launchpad development boards.

(If you use my code as a base for a simple program
with one pattern it will fit on a 2KB chip.)

==========
INSTALLING
==========
You require the mspgcc toolchain (I used version 
mspgcc-20120406), and a tool to program the chip such
as mspdebug or msp430-gdbproxy.

Compile with "make". Or if you are using mspdebug; "make prog"
will also program the MCU.
