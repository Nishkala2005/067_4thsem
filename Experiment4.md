# Instrumentation Amplifier - Theory

## Introduction

An **Instrumentation Amplifier (In-Amp)** is a precision amplifier designed to amplify **small differential voltages** in the presence of **large common-mode signals**. It is widely used in **sensor signal conditioning**, **data acquisition systems**, and **bio-medical instrumentation** due to its high input impedance and excellent common-mode rejection ratio (CMRR).

---

##  Basic 3-Op-Amp Configuration

The classic instrumentation amplifier is built using **three operational amplifiers**:


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
- ADM = 20 V/V
- R1 = 100 kΩ

###  Solving for RG:

ADM = 1 + (2 * R1) / RG

ADM = 1 + (2 * R1) / RG

=> 20 = 1 + (2 * 100k) / RG => 19 = (200k) / RG => RG = 200k / 19 => RG ≈ 10.526 kΩ

## Circuit Diagram


## Analysis of Adm

## Analysis of Acm
