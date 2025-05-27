# Instrumentation Amplifier 

## Introduction

An **Instrumentation Amplifier (In-Amp)** is a precision amplifier designed to amplify **small differential voltages** in the presence of **large common-mode signals**. It is widely used in **sensor signal conditioning**, **data acquisition systems**, and **bio-medical instrumentation** due to its high input impedance and excellent common-mode rejection ratio (CMRR).

---

##  Basic 3-Op-Amp Configuration

The classic instrumentation amplifier is built using **three operational amplifiers**:
![image](https://github.com/user-attachments/assets/e1f9abd3-f1ed-4e20-9f98-6e620ddc6ba3)


###  Key Components:
- **Two input buffer amplifiers**: Provide high input impedance.
- **One difference amplifier**: Performs subtraction and amplification.

---

## Gain Equation

The voltage gain **(Av)** of a typical 3-op-amp instrumentation amplifier is given by:
        
        Vout = (1 + (2 * R1) / RG ) * (V2 - V1)


Where:

- `V1`, `V2` = Input voltages  
- `R1` = Resistor connected in series with the input buffer op-amps  
- `RG` = Gain-setting resistor

 **Note**: A smaller `RG` results in a **higher gain**, and vice versa.


## Features

-  High Common-Mode Rejection Ratio (CMRR)
-  High input impedance
-  Differential signal amplification
-  Gain set by a single resistor (easy to configure)

---

##  Applications

- Biomedical signal processing (ECG, EEG)
- Strain gauge and load cell signal conditioning
- Temperature sensors (RTD, Thermocouples)
- Industrial and instrumentation systems

---



>  A good instrumentation amplifier ensures accurate low-level signal measurement in noisy environments.


##  Aim

Design an **Instrumentation Amplifier** using a **three op-amp configuration** with the following constraints:

- Resistors:  
  `R1 = R2 = R3 = R4 = R5 = R6 = 100 kΩ`
- Desired **Differential Mode Gain (ADM)**: `20 V/V`
- Calculate:
  - **Common Mode Gain (ACM)**
  - **Common Mode Rejection Ratio (CMRR)** for ADM = 20 and ADM = 50

---

##  Theory

An instrumentation amplifier is typically built with **three operational amplifiers**:
- Two **input buffer op-amps** (Op-Amp 1 and 2)
- One **differential amplifier** (Op-Amp 3)

###  Gain Equation

For a symmetrical 3-op-amp INA:


To achieve **ADM = 20**, solve for `RG`:


Given:
- 1. ADM = 20 V/V
- R1 = 100 kΩ

###  Solving for RG:

ADM = 1 + (2 * R1) / RG

ADM = 1 + (2 * R1) / RG

=> 20 = 1 + (2 * 100k) / RG => 19 = (200k) / RG => RG = 200k / 19 => RG ≈ 10.526 kΩ

## Circuit Diagram
![Screenshot 2025-04-15 093125](https://github.com/user-attachments/assets/cc4fb7c3-169d-426b-b088-70a34735a6ce)


## Analysis of Adm

![Screenshot 2025-04-15 092242](https://github.com/user-attachments/assets/e03e2202-2d9d-4d7e-8c16-d1f4cb6b79cb)

## Analysis of Acm

![Screenshot 2025-04-15 093101](https://github.com/user-attachments/assets/554a2738-3edf-4d4a-928c-289d112f1e0a)

---

###  Common Mode Gain (ACM) Calculation — For ADM = 20

**Observation from waveform:**
- Output Voltage `Vout ≈ ±5 nV` (peak)
- Common Mode Input Voltage `Vin_CM = 0.5 V` (peak)

**Formula:**

ACM = Vout / Vin_CM = (5 × 10⁻⁹) / 0.5 = 1 × 10⁻⁸ V/V



---

### 📊 CMRR Calculation for ADM = 20

CMRR = 20 × log₁₀(ADM / ACM) = 20 × log₁₀(20 / 1×10⁻⁸) = 20 × log₁₀(2 × 10⁹) ≈ 20 × 9.3 = 186 dB


 **CMRR = 186 dB**


---

###  Final Results

| Parameter | Value         |
|----------:|---------------|
| **ADM**   | 20 V/V        |
| **ACM**   | 1 × 10⁻⁸ V/V  |
| **CMRR**  | **186 dB**    |



---

- 2. ADM = 50 V/V
- R1 = 100 kΩ

##  Calculation of Gain Resistor (RG) for ADM = 50

The differential mode gain (ADM) for a 3-op-amp instrumentation amplifier is given by:

ADM = 1 + (2 * R1) / RG


###  Solving for RG:

ADM = 1 + (2 * R1) / RG => 50 = 1 + (2 * 100k) / RG => 49 = 200k / RG => RG = 200k / 49 => RG ≈ 4.0816 kΩ

## Circuit Diagram

![Screenshot 2025-04-15 093406](https://github.com/user-attachments/assets/1c35a084-2467-421d-b6de-a99ddac3f12e)


## Analysis of Adm

![Screenshot 2025-04-15 093934](https://github.com/user-attachments/assets/289ff972-afe9-4831-aed3-54fba6cecfa9)


## Analysis of Acm

![Screenshot 2025-04-15 093608](https://github.com/user-attachments/assets/9e3665d7-2508-4198-9507-c6f20bd56bad)

##  Simulation: Common Mode Gain (ACM) and CMRR Calculation

###  Circuit Setup

- Both inputs are common-mode signals:  
  `Vin1 = Vin2 = 0.5 sin(2π·1k·t)`
- Differential input = 0 → any output is due to **common-mode gain**.
- Simulation Output:  
  `Vout ≈ ±5 nV (peak)`

---

###  ACM (Common Mode Gain)

Formula:

ACM = Vout / Vcm


Given:
- Vout = 5 nV = `5 × 10⁻⁹` V
- Vcm = 0.5 V

Calculation:

ACM = (5 × 10⁻⁹) / 0.5 = 1 × 10⁻⁸ V/V


---

###  CMRR (Common Mode Rejection Ratio)

Formula:

CMRR = 20 × log₁₀(ADM / ACM)

For ADM = 50:

CMRR = 20 × log₁₀(50 / 1e-8) = 20 × log₁₀(5 × 10⁹) ≈ 20 × 9.7 ≈ 194 dB


---

###  Final Results

| Parameter | Value         |
|----------:|---------------|
| **ADM**   | 50 V/V        |
| **ACM**   | 1 × 10⁻⁸ V/V  |
| **CMRR**  | **194 dB**    |

>  Very high CMRR indicates excellent common-mode rejection, as expected for a well-balanced 3-op-amp instrumentation amplifier.


