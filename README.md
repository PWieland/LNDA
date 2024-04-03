## LNDA
Low Noise Differential Amplifier with JFET Input

This project is inspired by the Stanford Research SR560 Low Noise Voltage Preamplifier,
featured in "The Art of Electronics" by Horowitz & Hill (somewhat of a must-have for analog engineers).
For explanations refer to said book, an LTSPICE simulation file of the basic topology will also be included here.

What LNDA is: A DIY project aimed at building high-end test and measurement equipment on a budget.

What LNDA is NOT: A product with certified performance and proven track record. Although I have assembled
and tested multiple prototypes, the performance is at the very edge of what I can realiably quantify with my limited equipment.

It features an improved implementation of the base topology with lower noise, lower BOM cost
and reduced footprint, made possible by the extensive use of SMD technology. After SMD
assembly the entire board may be cleaned before mounting of the electromechanical
components such as relays and trim-potentiometers. The goal is to use footprints suitable for handsoldering without hot air.

Compatible with either JFE2140 or LSK389/489 as input JFET.

First (home-etched) Prototype with through hole components, single layer layout and accordingly high sensitivity to EMI:
![IMG_1798](https://github.com/PWieland/LNDA/assets/65927363/cef5c569-c689-4579-bc2c-d414e0949bbc)

V1 of the SMD Implementation with some minor layout errors (2-Layer PCB):
![IMG_0138](https://github.com/PWieland/LNDA/assets/65927363/e6300009-8223-4f24-b7a1-8b14ac44ca6f)


