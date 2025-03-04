# EXPERIMENT 2
## Aim: Design and analyze te MOS differential amplifier circuit following specificationns. Vdd = 2.2V, P <= 2.2mW, Vincm = 1.2V, Vocm = 1.2V, Vp = 0.4V

### **Differential Amplifier**
A differential amplifier is a type of electronic amplifier that amplifies the difference between two input signals while rejecting any common-mode signals. It is widely used in analog signal processing, sensor interfacing, and communication systems due to its high noise immunity and ability to reject interference.
In a MOSFET-based differential amplifier:
Matching between the two MOSFETs is crucial for proper operation and high-performance characteristics.

Mismatches can introduce offset voltage, gain imbalance, and increased common-mode rejection errors.
Circuit 1:

![Screenshot 2025-03-04 061530](https://github.com/user-attachments/assets/57a5f55e-69c5-430c-b3df-eef611b298ab)

### **Step 1**
### DC analysis:
![WhatsApp Image 2025-03-04 at 06 41 49_5b7d1de0](https://github.com/user-attachments/assets/32d8daf4-662b-4cf4-8099-986ac43a8312)
From the calculation we get,

Iss = 1mA
Id1 = Id2 = .5mA
Rd = 1.9kohm
Rss = 400ohm

Set the operating point in configure analysis by selecting dc operating point.
![Screenshot 2025-03-04 064534](https://github.com/user-attachments/assets/5de93c76-3f65-4264-92ce-4e3de296e5da)

For the appropriate dc operating point aspect ratio is 24.9 .
### **Step 2**
### Transient Analysis

Maximum input and output voltage swing

![WhatsApp Image 2025-03-04 at 07 02 53_49d72ce7](https://github.com/user-attachments/assets/85215423-6beb-484f-97d1-3710020e5b4f)








