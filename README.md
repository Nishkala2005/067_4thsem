# Circuit 1
## Aim: Calculate the dc analysis, transient analysis and ac analysis for the given circuit 

## Design 1
## Components required: MOSFET, resistor, voltage supply.
![Screenshot (1)](https://github.com/user-attachments/assets/cbf66c21-9165-445a-9681-8e3bf46c73f1)

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
![aspectratio](https://github.com/user-attachments/assets/f811ecb5-5610-4412-bddf-53323b08c1c4)


To perform dc analysis select DC operating point and run the simulation.

The obtained dc operating point is(.54V,55uA)
![opt](https://github.com/user-attachments/assets/6e4cba50-3d9c-412a-ad4b-085f50abe6e2)



## Transient Analysis
Transient analysis is used in MOSFET amplifiers to check how the circuit responds to sudden changes in voltage or current. It helps in analyzing signal transitions, switch-on and switch-off behavior, propagation delays, and any overshoot or ringing that may occur due to fast signal variations.

![Screenshot (1)](https://github.com/user-attachments/assets/c5b6dd5e-4f1f-4e19-a452-9e99bda1f58b)


Input waveform and output waveform
![image](https://github.com/user-attachments/assets/4c26982f-4d35-4e1e-8b7c-893b0d10ff8d)


## Gain of the circuit

Av = Vout/Vin

Vout = 1.85V

Vin = 950mV

Av = 1.95~~2

## AC Analysis


AC analysis is used in MOSFET amplifiers to study how the circuit responds to different frequencies of an input signal. It helps determine important parameters such as gain, bandwidth, phase shift, and frequency response. This analysis is essential for designing amplifiers that work efficiently over a desired frequency range.

For this analysis select the input voltage as sine wave and set DC offset to 0.9V, amplitude to 50mV and frequency to 1kHz. Select the AC amplitude to 1V. Then in configure analysis, select AC analysis and select decade in type of sweep and the select the number of points to 20 and operating from 0.1Hz to 1THz.

![Screenshot (1)](https://github.com/user-attachments/assets/7419b0a9-6ba6-412f-bb2c-78f6e213cf5c)


![ac](https://github.com/user-attachments/assets/fafdf120-2e03-4e7a-9ef3-12475a06ae01)


AC Analysis graph
![acgraph](https://github.com/user-attachments/assets/5083d083-edd4-4edb-bed3-15edb641a59c)



## Result

1.DC operating point :

For Rd = 1kohm
