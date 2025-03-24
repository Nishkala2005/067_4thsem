# Experiment 3
## Current Mirrors
1. Introduction
A current mirror is a circuit that copies (mirrors) a reference current to another branch while maintaining a constant current despite variations in voltage. It is widely used in biasing circuits, analog IC design, and active loads in amplifiers.
### Design and analyze current mirror circuit as load active in amplifier circuit
#### Part 1
Circuit Parameters: gain<= -10V/V   Vdd = 1.8V
I_total = I_ref + I_x
I_total = P/Vdd
#### Design for Current mirror 1:1 ratio
I_Ref = I_x = 0.277mA
![image](https://github.com/user-attachments/assets/f1fba6aa-51bd-47fc-a39f-9434fc4b1305)

![WhatsApp Image 2025-03-24 at 20 14 37_232d37b1](https://github.com/user-attachments/assets/317d962e-317f-4bab-be0b-09adb30d8be0)

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

#### DC Analysis
![image](https://github.com/user-attachments/assets/606dc415-bac7-4f0b-9b04-31934613994d)

#### Transient Analysis
![image](https://github.com/user-attachments/assets/b7510c4d-0c1b-48fd-bd33-24b9096ff216)


#### AC Analysis
![image](https://github.com/user-attachments/assets/af89945d-8ab7-476a-a5d2-dd03cb3685ea)

Gain ≈ 30 dB

Bandwidth ≈ ~1 GHz

#### Design for Current mirror 1:5 ratio
