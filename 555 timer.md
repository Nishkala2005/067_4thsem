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

