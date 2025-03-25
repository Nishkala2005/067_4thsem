# Experiment 3
## Current Mirrors
### Introduction
A current mirror is a circuit that copies (mirrors) a reference current to another branch while maintaining a constant current despite variations in voltage. It is widely used in biasing circuits, analog IC design, and active loads in amplifiers.

#### Part 1
### Design and analyze current mirror circuit as load active in amplifier circuit

Circuit Parameters: gain<= -10V/V   Vdd = 1.8V
I_total = I_ref + I_x
I_total = P/Vdd
### length = 180n
#### Design for Current mirror 1:1 ratio
I_Ref = I_x = 0.277mA
![image](https://github.com/user-attachments/assets/f1fba6aa-51bd-47fc-a39f-9434fc4b1305)
#### Calculation

![WhatsApp Image 2025-03-24 at 20 14 37_232d37b1](https://github.com/user-attachments/assets/317d962e-317f-4bab-be0b-09adb30d8be0)


| Parameters        | MOSFET1 | MOSFET2 | MOSFET3 |
|------------------|---------|---------|---------|
| Model           | NMOSC     | NMOSP     | NMOSP     |
| MOSFET Length   | 180n     | 180n      | 180n      |
| MOSFET Width    | 47.89u     | 500u     | 1m     |
| Threshold Voltage | T0.3662V    | -.3906V     | -.3906V    |

#### DC Analysis
![image](https://github.com/user-attachments/assets/3b5269d2-8e3f-4f82-ae4d-a16432f37fd4)

#### Transient Analysis
![image](https://github.com/user-attachments/assets/5a028625-bc05-4130-8034-859395d7ca85)

#### AC Analysis
![WhatsApp Image 2025-03-24 at 20 27 29_5e94e810](https://github.com/user-attachments/assets/c105cf72-3d9e-4c94-addf-f9ff5da632e7)

Gain ≈ 28 dB (or 25.1 in linear scale).

Bandwidth ≈ 100 MHz.


#### Design for Current mirror 1:2 ratio
![image](https://github.com/user-attachments/assets/9d6b36cd-c402-437a-a796-8adf07ab1377)


| Parameters        | MOSFET1 | MOSFET2 | MOSFET3 |
|------------------|---------|---------|---------|
| Model           | NMOSC     | NMOSP     | NMOSP     |
| MOSFET Length   | 180n     | 180n      | 180n      |
| MOSFET Width    | 144.5u     | 20u     | 10u     |
| Threshold Voltage | 0.3662V    | -.3906V     | -.3906V    |
#### DC Analysis
![image](https://github.com/user-attachments/assets/606dc415-bac7-4f0b-9b04-31934613994d)

#### Transient Analysis
![image](https://github.com/user-attachments/assets/b7510c4d-0c1b-48fd-bd33-24b9096ff216)


#### AC Analysis
![image](https://github.com/user-attachments/assets/af89945d-8ab7-476a-a5d2-dd03cb3685ea)

Gain ≈ 30 dB

Bandwidth ≈ ~200MHz

#### Design for Current mirror 1:4 ratio

![image](https://github.com/user-attachments/assets/242730c8-fdb1-4028-a85b-2a4c648d4edc)

| Parameters        | MOSFET1 | MOSFET2 | MOSFET3 |
|------------------|---------|---------|---------|
| Model           | NMOSC     | NMOSP     | NMOSP     |
| MOSFET Length   | 180n     | 180n      | 180n      |
| MOSFET Width    | 84.965u | 20u     | 10u     |
| Threshold Voltage | 0.3662V    | -.3906V     | -.3906V    |

#### DC Analysis

![image](https://github.com/user-attachments/assets/dc4e1220-2a27-4c20-9f98-0f01c086e5e6)

#### Transient Analysis

![image](https://github.com/user-attachments/assets/3d2cf079-a68a-490d-ae39-3bdbd9e2fc8b)


#### AC Analysis

![image](https://github.com/user-attachments/assets/be5a23ad-fea8-4370-8483-25a9019287d2)
Gain ≈ 30 dB

Bandwidth ≈ ~250MHz


### length = 500nm
#### Design for Current mirror 1:1 ratio

![image](https://github.com/user-attachments/assets/9ff78412-3cf9-410d-b71e-c11a546df70b)
l=500n w=64.5u  
| Parameters        | MOSFET1 | MOSFET2 | MOSFET3 |
|------------------|---------|---------|---------|
| Model           | NMOSC     | NMOSP     | NMOSP     |
| MOSFET Length   | 500n     | 500n      | 500n      |
| MOSFET Width    | 64.5u | 10u     | 10u     |
| Threshold Voltage | 0.3662V    | -.3906V     | -.3906V    |
#### DC Analysis
![image](https://github.com/user-attachments/assets/d774d35e-0873-4b56-bdb2-2d414f2692da)


#### Transient Analysis
![image](https://github.com/user-attachments/assets/377c8344-79c9-4434-93e1-6d6dd09e45f6)



#### AC Analysis

![image](https://github.com/user-attachments/assets/12a67dec-a6c6-4590-b320-146c0d01a398)

Gain ≈ 37.8 dB

Bandwidth ≈ ~143 MHz

Comparison table for all three circuits.

| **Circuit**               | **MOSFET** | **Model** | **Width (W)** | **Length (L)** | **W/L Ratio** | **Threshold Voltage (Vth)** |
|---------------------------|------------|-----------|---------------|----------------|---------------|-----------------------------|
| **Current Mirror 1:1**    | M1         | NMOSC     | 47.89 µm      | 180 nm         | 266.06        | 0.3662 V                    | 
|                           | M2         | NMOSP     | 500 µm        | 180 nm         | 2777.78       | -0.3906 V                   | 
|                           | M3         | NMOSP     | 1 mm          | 180 nm         | 5555.56       | -0.3906 V                   | 
| **Current Mirror 1:2**    | M1         | NMOSC     | 144.5 µm      | 180 nm         | 802.78        | 0.3662 V                    | 
|                           | M2         | NMOSP     | 20 µm         | 180 nm         | 2777.78       | -0.3906 V                   | 
|                           | M3         | NMOSP     |   10 µm       | 180 nm         | 5555.56       | -0.3906 V                   | 
| **Current Mirror 1:4**    | M1         | NMOSC     |64.5u          |  180 nm        | Not specified | 0.3662 V                    | 
|                           | M2         | NMOSP     | 10 µm         | 180 nm         | 2777.78       | -0.3906 V                   | 
|                           | M3         | NMOSP     | 10 µm         | 180 nm         | 5555.56       | -0.3906 V                   | 


### Part 2

#### Design the differential amplifier using the same design specification as differential amplifier experiment. Perform DC analysis,transient analysis, AC analysis.

![image](https://github.com/user-attachments/assets/f1b418ce-e373-4933-9558-46e985fd8af4)


#### DC Analysis

![image](https://github.com/user-attachments/assets/67534d76-f70b-40cc-b0fe-ce4f83a6d822)


#### Transient Analysis
![image](https://github.com/user-attachments/assets/ed475e9d-086c-45ed-a8b8-44e20b45a5cb)


#### AC Analysis
![image](https://github.com/user-attachments/assets/d9bfda19-d1f6-4cff-ad25-979e9c034c8f)


