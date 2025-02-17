# Circuit 1
## Aim: Calculate the dc analysis, transient analysis and ac analysis for the given circuit 

## Design 1
## Components required: MOSFET, resistor, voltage supply.
![alt text](<Screenshot (1).png>)
## Procedure:
1. Connect the components as given in the circuit.
2. Let Vdd be 1.8V and Vgs be 0.9V
3. Connect the ground to required terminal.

## DC Analysis 
Given information: Power = 100microwatts

Id(drain current) = 55.5uA.

To get the expected current set the aspect ratio and Rd in such a way that obtaineed current value matches the expected current value.

Vov = Vgs - Vth

Rd = 22.6kohm

For the expected Id value, the obtained W/L ratio is 180n/.3u.
![alt text](aspectratio.png) 

To perform dc analysis select DC operating point and run the simulation.

The obtained dc operating point is(.54V,55uA)
![alt text](opt.png)


## Transient Analysis
Transient analysis is used in MOSFET amplifiers to check how the circuit responds to sudden changes in voltage or current. It helps in analyzing signal transitions, switch-on and switch-off behavior, propagation delays, and any overshoot or ringing that may occur due to fast signal variations.

![alt text](<Screenshot (1)-1.png>)

Input waveform

![alt text](ipwf.png)


Output waveform
![alt text](image.png)

## Gain of the circuit

Av = Vout/Vin

Vout = 1.85V

Vin = 950mV

Av = 1.95~~2

## AC Analysis


AC analysis is used in MOSFET amplifiers to study how the circuit responds to different frequencies of an input signal. It helps determine important parameters such as gain, bandwidth, phase shift, and frequency response. This analysis is essential for designing amplifiers that work efficiently over a desired frequency range.

For this analysis select the input voltage as sine wave and set DC offset to 0.9V, amplitude to 50mV and frequency to 1kHz. Select the AC amplitude to 1V. Then in configure analysis, select AC analysis and select decade in type of sweep and the select the number of points to 20 and operating from 0.1Hz to 1THz.

![alt text](<Screenshot (1)-2.png>)

![alt text](ac.png)

AC Analysis graph
![alt text](acgraph.png)


## Result

1.DC operating point :

For Rd = 1kohm
