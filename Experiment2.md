# EXPERIMENT 2
## Aim: Design and analyze te MOS differential amplifier circuit following specificationns. Vdd = 2.2V, P <= 2.2mW, Vincm = 1.2V, Vocm = 1.2V, Vp = 0.4V

### **Differential Amplifier**
A differential amplifier is a type of electronic amplifier that amplifies the difference between two input signals while rejecting any common-mode signals. It is widely used in analog signal processing, sensor interfacing, and communication systems due to its high noise immunity and ability to reject interference.
In a MOSFET-based differential amplifier:
Matching between the two MOSFETs is crucial for proper operation and high-performance characteristics.

Mismatches can introduce offset voltage, gain imbalance, and increased common-mode rejection errors.
## Circuit 1:

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

For transient analysis waveform select transient analysis in configure analysis
Select sine wave,dc offset voltage as 1.2V , amplitude as 50mV, frequency as 1KHz and V2phi(deg as 180.

![Screenshot 2025-03-04 061018](https://github.com/user-attachments/assets/7bf6cdc1-541a-40cc-bddd-ed3b5eec1636)

When the input voltage is more then the minimum swing or outside the allowable swing the output wave form deforms, i.e it is in triode or cutoff region.

### **Step 3**
### AC Analysis

• Type of sweep: Decade
• Number of points per decade: 10
• Start frequency: 0.1 Hz
• Stop frequency: 1 THz
AC Amplitude as 1 and AC Phase as 0 in V1 <br>
AC Amplitude as 1 and AC Phase as 180 in V2 <br>

![Screenshot 2025-03-04 071234](https://github.com/user-attachments/assets/871fb422-0cb6-467e-ad7b-7462930e4f47)

## Circuit 2

Replace the resistor with a current source of 1mA.
![Screenshot 2025-03-04 071746](https://github.com/user-attachments/assets/432baa90-8829-4c0a-832d-5ee0b15aa707)

### ** Step 1**
### DC Analysis

![Screenshot 2025-03-04 071659](https://github.com/user-attachments/assets/c46f838f-ff04-492f-b606-857aaab3225c)

### ** Step 2**
### Transient Analysis
![Screenshot 2025-03-04 061018](https://github.com/user-attachments/assets/f81acb50-fff4-4c01-b8d5-25d8d413b5ee)

### **Step 3**
### AC Analysis

![Screenshot 2025-03-04 071234](https://github.com/user-attachments/assets/f6f467c8-6eb1-43b4-8149-d6dd4b8e8aab)










