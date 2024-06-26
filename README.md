## LNDA
Low Noise Differential Amplifier with JFET Input

This project is inspired by the Stanford Research SR560 Low Noise Voltage Preamplifier,
featured in "The Art of Electronics" by Horowitz & Hill (somewhat of a must-have for analog engineers and voltnuts).
For explanations refer to said book, an LTSPICE simulation file of the basic topology will also be included here at some point.
The schematics of the SR560 can be found here: https://www.physics.wisc.edu/courses/home/spring2020/407/407_Lab_Instrument_Manuals/SR560-low-noise_amplifier-filter/SR560_w_schematics.pdf


What LNDA is: A DIY project aimed at building high-end test and measurement equipment on a budget.

What LNDA is NOT: A product with certified performance and proven track record. Although I have assembled
and tested multiple prototypes, the performance is at the very edge of what I can realiably quantify with my equipment.

It features an improved implementation of the base topology with significantly lower noise, lower BOM cost
and reduced footprint, made possible by the extensive use of SMD technology.
After SMD assembly the entire board should be cleaned from any flux residue before mounting 
of the electromechanical components such as relays and trim-potentiometers. 
An effort was made to use only components that can be hand-soldered without hot air.

Compatible with either JFE2140 or LSK389/489 as input JFET. 

### Current Project Status: Prototype(s) working, but no GERBER files suitable for publishing yet

First (home-etched) Prototype with through hole components, single layer layout and accordingly high sensitivity to EMI:
![IMG_1798](https://github.com/PWieland/LNDA/assets/65927363/cef5c569-c689-4579-bc2c-d414e0949bbc)

V1 of the SMD Implementation with some minor layout errors (2-Layer PCB):
![IMG_0138](https://github.com/PWieland/LNDA/assets/65927363/e6300009-8223-4f24-b7a1-8b14ac44ca6f)

V2 - work in progress


Measurements:


