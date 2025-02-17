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
For Rd = 1kohm and W/L = 180n/500u , operating point is (5mV,1mA)
![image](https://github.com/user-attachments/assets/37fa039f-3f62-4aac-9754-f529fc63e5af)


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

For Rd = 1kohm, W/L=180n/500u : (5mV,1mA)
For Rd = 22.6kohm, W/L=180n/.3u : (.54V,55uA)

2. Gain of the circuit : 2


## Inference

1.The width of the MOSFET directly effects the Drain current.
2.By changing the dimensions of the MOSFET M1 when varying the width of PMOS there is not a lot of change in the drain current(ie. Id doesn't get effected much).
M2 when varying the width of NMOS there is drastic change in the drain current.
3.If width is increased it leads to a higher gain 4.180 degree phase shift between the input and output waveform.

## Design 2

![image](https://github.com/user-attachments/assets/e696fec2-cdf7-425e-b5bb-e76bee8c38d4)

## Procedure:
1. Connect the components as shown in the circuit diagram.
2. Let the Vdd be 1.8V and Vg be .8V.
3. Connect the ground to the terminals wherever required.


## DC Analysis

Let Vin be 1V
Id = 55.5uA
To get the expected current set the aspect ratio and pmos impedance in such a way that obtaineed current value matches the expected current value.

Vov = Vgs - Vth

For the expected current the aspect ratio of M1 is 180n/.38u

![image](https://github.com/user-attachments/assets/cac76666-c97e-4c7c-a941-848a05bb3feb)

DC operating point is(1.79V,55uA).

![image](https://github.com/user-attachments/assets/6b2ad0a8-6a90-4fd6-a21e-9c1cee31bbea)

## Transient Analysis
Transient analysis is used in MOSFET amplifiers to check how the circuit responds to sudden changes in voltage or current. It helps in analyzing signal transitions, switch-on and switch-off behavior, propagation delays, and any overshoot or ringing that may occur due to fast signal variations.

Input waveform
![image](https://github.com/user-attachments/assets/581601ec-173b-4ff0-ae8b-9a3f3827b046)


Output waveform
![image](https://github.com/user-attachments/assets/f1415824-e9d4-4ed8-ad1e-cbe2b522e413)


## Gain of the circuit

Av = Vout/Vin
Vout = 1.79V
Vin = .85V
Av = 2.1


## AC Analysis

AC analysis is used in MOSFET amplifiers to study how the circuit responds to different frequencies of an input signal. It helps determine important parameters such as gain, bandwidth, phase shift, and frequency response. This analysis is essential for designing amplifiers that work efficiently over a desired frequency range.

For this analysis select the input voltage as sine wave and set DC offset to 0.9V, amplitude to 50mV and frequency to 1kHz. Select the AC amplitude to 1V. Then in configure analysis, select AC analysis and select decade in type of sweep and the select the number of points to 20 and operating from 0.1Hz to 1THz.

![image](https://github.com/user-attachments/assets/8276f16f-1fd5-428b-8809-cfb291a77d62)

Analysis graph
![image](https://github.com/user-attachments/assets/bffcef10-c22c-4dd2-9eb9-ccabf650b90b)



## Result
1. DC operating point (1.7V,55uA)
2. Gain of the circuit : 2


## Inference

1.The width of the MOSFET directly effects the Drain current.
2.By changing the dimensions of the MOSFET M1 when varying the width of PMOS there is not a lot of change in the drain current(ie. Id doesn't get effected much).
M2 when varying the width of NMOS there is drastic change in the drain current.
3.If width is increased it leads to a higher gain 4.180 degree phase shift between the input and output waveform.
4.The CMOS amplifier has gain =5.5 dB.(ie, the ouput signal is almost 6 times larger then the input signal.









 
