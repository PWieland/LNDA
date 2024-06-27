## LNDA
Low Noise Differential Amplifier with JFET Input

This project is inspired by the Stanford Research SR560 Low Noise Voltage Preamplifier,
featured in "The Art of Electronics" by Horowitz & Hill (somewhat of a must-have for analog engineers and voltnuts).
For explanations refer to said book, an LTSPICE simulation file of the basic topology will also be included here at some point.
The schematics of the SR560 can be found here: https://www.physics.wisc.edu/courses/home/spring2020/407/407_Lab_Instrument_Manuals/SR560-low-noise_amplifier-filter/SR560_w_schematics.pdf


### What LNDA is: A DIY project aimed at building high-end test and measurement equipment on a budget.

### What LNDA is NOT: A product with guaranteed performance figures and a proven track record. 


It features an improved implementation of the base topology with significantly lower noise, lower BOM cost
and reduced footprint, made possible by the extensive use of SMD technology.
After SMD assembly the entire board should be cleaned from any flux residue before mounting 
of the electromechanical components such as relays and trim-potentiometers. 
An effort was made to use only components that can be hand-soldered without hot air.

## Component choices:

To achieve optimum noise performance, careful component selection is required. Once the overall topology and the component values are optimised for noise performance, 
it comes down to choosing active and passive components that contribute a

### JFETs:

Compatible with either Texas Instruments JFE2140 or Linear Systems LSK389/489 as input JFET. 

### OpAmps:

In the direct signal path, the original SR560 uses OP37 and LT1028, which are still very good choices.
Both of them are decompensated (as in not unity-gain stable), low-noise, high-precision amplifiers.
Substituting them without compromising performance or even improving performance figures is non-trivial.
Using unity-gain-stable alternatives like Texas Instruments OPAx211

### Resistors:

All resistors in the direct signal path should be thin/metal-film types with low temperature coefficient and tight tolerances.
For the drain resistors and the upper two source resistors, ≤25ppm/K and 0.1% tolerance is strongly recommended. Elsewhere, 50ppm/K and 1% Tolerance is acceptable.

However, even precision resistors aren't made equal. Without going into detail, maximum miniaturisation is not feasible for ultralow noise applications.
There are plenty of papers on resistor noise, one of them compares the (excess) current noise of various types: https://dcc.ligo.org/public/0002/T0900200/001/current_noise.pdf

Figures 6 and 10 indicate that among others, Vishay Beyschlag MMA0204 show relatively low excess noise. They are also reasonably priced, widely available and easy to solder by hand.
MELF resistors may be seen by some as a weird choice in modern electronics, but Vishay MELFs are without a doubt excellent resistors and fit perfectly on most 1206 footprints.

### Capacitors:

In the signal chain, either NP0/C0G ceramic or film capacitors (PP/PS) are used. 
For power filtering, a combination of X7R/X5R ceramics and electrolytic capactitors is employed.
The usual rules about capacitor derating apply, maximum miniaturisation is again not feasible.

### Current Project Status: Prototype(s) working, but no GERBER files suitable for publishing yet

First (home-etched) Prototype with through hole components, single layer layout and accordingly high sensitivity to EMI:
![IMG_1798](https://github.com/PWieland/LNDA/assets/65927363/cef5c569-c689-4579-bc2c-d414e0949bbc)

First SMD Implementation with some minor layout errors (2-Layer PCB):
![IMG_0138](https://github.com/PWieland/LNDA/assets/65927363/e6300009-8223-4f24-b7a1-8b14ac44ca6f)
This version features full gain switching via relay and CMOS switches, controlled over logic level inputs on the headers.
This version is fully DC-coupled, but AC-coupling capacitors and relays can be added externally.

V2 - work in progress


## Simulation:

The original SR560 design with LSK389B and the simulated input referred noise and gain.
<img width="1040" alt="image" src="https://github.com/PWieland/LNDA/assets/65927363/eeafb152-75bc-4df1-a792-f7c8d3083381">
<img width="1020" alt="image" src="https://github.com/PWieland/LNDA/assets/65927363/9267b9d0-5c45-443a-a909-440bbf0484f2">
Simply reducing the values of the feedback and source resistors by roughly 50% (as suggested in "The Art of Electronics") results in a noticeable improvement, lowering the flatband noise to 2nV/rtHz.
<img width="1319" alt="image" src="https://github.com/PWieland/LNDA/assets/65927363/7fb73b79-1cf5-4179-90a0-7b7a53f56156">
The next step is to adjust the drain resistors and the biasing of the JFET to optimize for noise performance without impacting stability.

## Measurements:


