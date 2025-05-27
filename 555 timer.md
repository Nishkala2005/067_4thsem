# Monostable Multivibrator Using 555 Timer IC

## Aim
Generate a waveform with pulse width of **0.5 ms** under different trigger conditions using **555 timer IC**.

---

## Theory

A **monostable multivibrator**, also known as a one-shot pulse generator, produces a single pulse of fixed duration in response to an external trigger signal. The 555 timer IC is a versatile chip used in this configuration to generate precise time delays.

In monostable mode:
- The output remains **LOW** until triggered.
- Once triggered, the output goes **HIGH** for a specific time period `T`, then returns to **LOW**.
- This duration `T` is determined by an external resistor and capacitor using the formula:
T = 1.1 × R × C

To achieve a pulse width of **0.5 ms**:

Choose suitable values of **R** and **C**, for example:
- R = 4.5 kΩ
- C = 0.1 µF

Then:
T = 1.1 × 4500 × 0.1×10⁻⁶ = 0.495 ms ≈ 0.5 ms

---

## Components Required

| Component             | Value/Part No.     | Quantity |
|----------------------|--------------------|----------|
| 555 Timer IC         | NE555              | 1        |
| Resistor             | 4.5 kΩ (or 4.7 kΩ)  | 1        |
| Capacitor            | 0.1 µF             | 1        |
| Push Button          | -                  | 1        |
| Power Supply         | 5V or 9V DC        | 1        |
| Breadboard & Wires   | -                  | As needed |
| Oscilloscope / DSO   | -                  | 1        |

---

## Circuit Diagram

![WhatsApp Image 2025-05-27 at 06 51 44_352bd98c](https://github.com/user-attachments/assets/917b2b1f-ec5c-4bce-b494-2afab1b1b5a9)

---

## Working

- When the trigger pin (pin 2) receives a LOW signal (<1/3 Vcc), the timer starts timing.
- The output (pin 3) goes HIGH for the duration `T = 1.1RC`.
- After the time `T` elapses, the output returns to LOW.
- Re-triggering is only possible after the pulse ends.

---

## Trigger Conditions Tested

| Condition                      | Observation                         |
|-------------------------------|--------------------------------------|
| Manual trigger using push button | Output pulse of 0.5 ms observed     |
| Trigger from square wave generator | Output pulse of 0.5 ms per trigger |
| Trigger during HIGH output    | No effect until output goes LOW      |

---

## Output Waveform

Simulations were performed using a pulse source (`VTrig`) with varying parameters to test the monostable response.

###  Case 1: Properly Spaced Triggers

**Trigger Pulse Source:**
VTrig PULSE(5 0 0.05m 0 0 0.01m 2m)
![WhatsApp Image 2025-05-27 at 06 52 04_2cadc49e](https://github.com/user-attachments/assets/3620b6f3-937b-4caa-892d-f4f608936627)

- Generates a falling edge every **2 ms**.
- Simulation Time: **10 ms**

**Expected Results:**

- Each falling edge successfully triggers the 555 timer.
- The output (`VOUT`) goes HIGH for ~0.5 ms per trigger.
- Multiple distinct output pulses are generated.

**Waveforms:**

1. **Trigger Input (VTrig)**: Periodic 2 ms LOW pulses.
2. **Capacitor Voltage (VC)**: Shows charge/discharge profile.
3. **Output (VOUT)**: Series of 0.5 ms HIGH pulses.

---

### 🔹 Case 2: Rapid Repeated Triggers

**Trigger Pulse Source:**
VTrig PULSE(5 0 0.05m 0 0 0.01m 0.2m)
![WhatsApp Image 2025-05-27 at 06 52 25_dab8248f](https://github.com/user-attachments/assets/dbb08b27-a7cb-4694-a980-f77b61f8c3fd)

- Generates a falling edge every **0.2 ms** (faster than output duration).
- Simulation Time: **2 ms**

**Expected Results:**

- Only the **first falling edge** triggers the timer.
- Output (`VOUT`) remains HIGH for 0.5 ms.
- Subsequent triggers during the HIGH period are **ignored**.
- Only **one output pulse** is generated.

**Waveforms:**
1. **Trigger Input (VTrig)**: Fast repetitive pulses.
2. **Capacitor Voltage (VC)**: Single charge/discharge cycle.
3. **Output (VOUT)**: Single 0.5 ms HIGH pulse.

---

##  Observations

| Condition                    | Output Behavior                        |
|-----------------------------|----------------------------------------|
| Properly spaced triggers    | Multiple 0.5 ms pulses                 |
| Rapid repeated triggers     | Single 0.5 ms pulse, others ignored    |

---

##  Applications

- Pulse stretching
- Debouncing mechanical switches
- Delay generation in digital circuits
- Frequency-to-time conversion

---

##  Conclusion

The monostable multivibrator using the 555 Timer IC was successfully simulated and tested. Under well-spaced triggers, each falling edge initiates a 0.5 ms pulse. In rapid trigger conditions, only the first falling edge is acknowledged, validating the one-shot pulse behavior.

---



# Astable and Monostable Multivibrators Using 555 Timer ICs

##  Aim

To generate a waveform with **pulse width of 0.5 ms** under different trigger conditions using **555 timer ICs**. This includes configuring:
- One 555 timer in **astable mode** as the pulse generator.
- Another 555 timer in **monostable mode** for waveform shaping.

---

##  Circuit Diagram

![WhatsApp Image 2025-05-27 at 06 52 57_6d374cc6](https://github.com/user-attachments/assets/4d7b3bd4-2b20-46f5-8dc8-d84ef6048463)
 
> *Figure: Astable and Monostable Multivibrators Using NE555 Timer IC*

---

##  Theory

###  555 Timer in Astable Mode

- Generates continuous square wave (no external trigger required).
- Output oscillates between HIGH and LOW indefinitely.

Formulas:
- `T_ON = 0.693 × (R1 + R2) × C`
- `T_OFF = 0.693 × R2 × C`
- `T_PERIOD = T_ON + T_OFF`

###  555 Timer in Monostable Mode

- Generates a single output pulse of fixed duration on every trigger.
- Pulse width `T = 1.1 × R × C`

---

##  Calculations

###  Case 1: `T_ON = 0.3 ms`, `T_OFF = 0.2 ms`

- Period = `0.3 + 0.2 = 0.5 ms`
- Frequency = `1 / 0.5 ms = 2 kHz`

Assume:  
- C = 0.01 µF  
From `T_ON = 0.693 × (R1 + R2) × C`, we get:
0.3 ms = 0.693 × (R1 + R2) × 0.01×10⁻⁶
=> R1 + R2 ≈ 43.26 kΩ

From `T_OFF = 0.693 × R2 × C`:

0.2 ms = 0.693 × R2 × 0.01×10⁻⁶
=> R2 ≈ 28.87 kΩ
=> R1 ≈ 14.39 kΩ

>  **Use:** R1 = 14.4 kΩ, R2 = 28.9 kΩ, C = 0.01 µF

---

###  Case 2: `T_ON = 0.7 ms`, `T_OFF = 0.3 ms`

- Period = `0.7 + 0.3 = 1.0 ms`
- Frequency = `1 / 1.0 ms = 1 kHz`

Assume C = 0.01 µF again:

0.7 ms = 0.693 × (R1 + R2) × 0.01×10⁻⁶
=> R1 + R2 ≈ 100.99 kΩ

0.3 ms = 0.693 × R2 × 0.01×10⁻⁶
=> R2 ≈ 43.29 kΩ
=> R1 ≈ 57.70 kΩ

>  **Use:** R1 = 57.6 kΩ, R2 = 43.3 kΩ, C = 0.01 µF
> 
###  Case 3: `T_ON = 0.4 ms`, `T_OFF = 0.1 ms`, `T = 0.5 ms`
![WhatsApp Image 2025-05-27 at 06 53 47_69d26ff7](https://github.com/user-attachments/assets/a09959e9-298a-4230-8987-634d2b1778af)

Assume C = 0.01 µF  
- `R1 + R2 = 57.69 kΩ`  
- `R2 = 14.43 kΩ` → `R1 ≈ 43.26 kΩ`

> Used: R1 = 43.2 kΩ, R2 = 14.4 kΩ, C = 0.01 µF

**Inverted Output:**
Using the transistor inverter (Figure 2), we invert this waveform:
- Inverted `T_ON = 0.1 ms`  
- Inverted `T_OFF = 0.4 ms`

This gives a falling edge trigger with:
- Enough time for monostable reset
- Reliable trigger edge separation

---
---

##  Experimental Setup

| Component           | Value                |
|--------------------|----------------------|
| IC                 | NE555 x2             |
| R1, R2             | As per calculation   |
| Capacitors         | 0.01 µF, 1 µF, 0.1 µF|
| Diode              | 1N4148               |
| Op-Amp             | LM358 (if used)      |
| Supply Voltages    | +5V, ±12V            |

---

##  Output Waveform Observations

###  Case 1 (T = 0.5 ms)
![WhatsApp Image 2025-05-27 at 06 53 11_10e9921b](https://github.com/user-attachments/assets/806c7d61-234c-48ee-ad3f-cf44efe010fd)

- Astable output toggles every 0.5 ms (0.3 ms ON, 0.2 ms OFF).
- Each falling edge triggers the monostable multivibrator.
- Monostable generates a **0.5 ms pulse** per trigger.
- Output waveform is a series of 0.5 ms pulses aligned with each trigger.

###  Case 2 (T = 1.0 ms)
![WhatsApp Image 2025-05-27 at 06 53 26_3e34c3b1](https://github.com/user-attachments/assets/789ec5bb-891e-4e27-9021-5d3fceb7fe97)

- Astable output toggles every 1.0 ms (0.7 ms ON, 0.3 ms OFF).
- Fewer trigger pulses due to slower frequency.
- Monostable output still maintains 0.5 ms pulse per trigger.

###  Case 3 (with inverter)
![WhatsApp Image 2025-05-27 at 06 54 05_bb49e532](https://github.com/user-attachments/assets/91fb1b97-f6d8-4d1c-be46-e29db839ca57)

- Trigger pulse: `0.1 ms HIGH`, `0.4 ms LOW`
- Falling edges spaced by 0.5 ms
- Monostable has sufficient time to return to LOW before next pulse

---

##  Conclusion

The circuit successfully demonstrates:
- Generation of clock pulses using astable multivibrator.
- Controlled pulse width generation using monostable multivibrator.
- Flexible waveform shaping by tuning R and C values.

---



