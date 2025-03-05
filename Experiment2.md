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
### **Calculation of Input and Output Dynamic Range for the MOS Differential Amplifier**  

#### **1. Input Dynamic Range (IDR)**  
The **input dynamic range** is determined by the limits within which the differential pair operates in the **active region** without entering cutoff or triode regions.  

- **Lower Limit (\( V_{ICM(min)} \))**:  
  - To keep **both MOSFETs in saturation**, the **source voltage** should be above **\( VSS \)**.  
  - The source voltage is approximately:  
    \[
    VS = VICM - VGS
    \]
  - Since **\( VG = VICM \)** and **\( VGS = VP \)** 
    \[
    VS = VICM - VP
    \]
  - For saturation, we need:  
    \[
    VS > VSS
    \]
  - Given \( VP = 0.4V \), \( VSS = ISS RSS = 1mA \times 400Ω = 0.4V \),  
    \[
    V_ICMmin > VSS + VP = 0.4V + 0.4V = 0.8V
    \]  

- **Upper Limit (\( VICMmax \))**:  
  - The MOSFETs should not enter the **triode region**, so  
    \[
    VDS > VGS - VP
    \]
  - Since \( VD = VDD - ID RD \),  
    \[
    VICMmax < VD - VP
    \]  
  - Substituting \( VD = 2.2V - (0.5mA \times 1.9kΩ) = 2.2V - 0.95V = 1.25V \),  
    \[
    VICMmax < 1.25V - 0.4V = 0.85V
    \]  

#### **Final Input Dynamic Range (IDR):**  
\[
0.8V < VICM < 1.25V
\]  

---

#### **2. Output Dynamic Range (ODR)**  
The **output dynamic range** depends on how much the drain voltage (\( V_D \)) can swing **without pushing MOSFETs into the triode or cutoff region**.  

- **Upper Limit (\( Voutmax \))**:  
  - The drain voltage should not exceed \( Vdd \),  
    \[
    Voutmax \approx Vdd = 2.2V
    \]

- **Lower Limit (\( Voutmin \))**:  
  - To **stay in saturation**,  
    \[
    VD > VS + VP
    \]
  - Since \( VS \approx 0.8V \),  
    \[
    V_outmin > 0.8V + 0.4V = 1.2V
    \]

#### **Final Output Dynamic Range (ODR):**  
\[
1.2V < Vout < 2.2V
\]

---

### **Summary of Results**
| Parameter | Value |
|-----------|--------|
| **Input Dynamic Range (IDR)** | **\( 0.8V < VICM < 1.25V \)** |
| **Output Dynamic Range (ODR)** | **\( 1.2V < Vout < 2.2V \)** |

---



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

### **Step 1**
### DC Analysis

![Screenshot 2025-03-04 071659](https://github.com/user-attachments/assets/c46f838f-ff04-492f-b606-857aaab3225c)

### **Step 2**
### Transient Analysis
![Screenshot 2025-03-04 061018](https://github.com/user-attachments/assets/f81acb50-fff4-4c01-b8d5-25d8d413b5ee)

### **Step 3**
### AC Analysis

![Screenshot 2025-03-04 071234](https://github.com/user-attachments/assets/f6f467c8-6eb1-43b4-8149-d6dd4b8e8aab)

## Circuit 3

Replace current source with nMOSFET

![Screenshot 2025-03-04 201720](https://github.com/user-attachments/assets/46744323-f060-4c44-8720-327d375878a1)

Vb should be less than Vp as the drain voltage of MOSFET M3 is Vp and the Vb should be greater than the Vth , therefore the value of Vb should be between 0.366 V and 0.4V.

### **Step 1**
### DC Analysis
set the operating point of M3 such that It is in saturation state. Vb=0.4 V

![Screenshot 2025-03-04 201705](https://github.com/user-attachments/assets/2fcdfffc-d097-492a-9c8b-bfa5ea27994a)


### **Step 2**
### Transient Analysis
![Screenshot 2025-03-04 073929](https://github.com/user-attachments/assets/887ccbe6-3ed4-4add-91f1-5aa6dff134e8)
![Screenshot 2025-03-04 073951](https://github.com/user-attachments/assets/656135fd-e025-4a8a-9fa2-25cddbe37df2)

### **Step 3**
### AC Analysis

![Screenshot 2025-03-04 071234](https://github.com/user-attachments/assets/c0eddf78-bcaf-413d-a13c-779455cc73c8)

## Comparing all the circuits

| **Parameter** | **Circuit 1** | **Circuit 2** | **Circuit 3** |
|---------------|---------------|---------------|---------------|
| **V<sub>DD</sub>** | 2.2 V | 2.2 V | 2.2 V |
| **V<sub>ICM</sub>** | 1.2 V | 1.2 V | 1.2 V |
| **V<sub>OCM</sub>** | 1.25 V | 1.25 V | 1.25 V |
| **R<sub>D</sub>** | 1.9 kΩ | 2.0 kΩ | 2.1 kΩ |
| **R<sub>SS</sub>** | 400 Ω | 450 Ω | 500 Ω |
| **I<sub>SS</sub>** | 1 mA | 1.1 mA | 1.2 mA |
| **I<sub>D</sub>** | 0.5 mA | 0.55 mA | 0.6 mA |
| **Differential Gain (A<sub>d</sub>)** | 4.75 | 5.0 | 5.25 |
| **Power Consumption (P)** | 2.2 mW | 2.42 mW | 2.64 mW |



## Circuit 4
![Screenshot 2025-03-04 195725](https://github.com/user-attachments/assets/d99ea730-c465-4262-acfd-bf01df26e54f)

### **Step 1**
### DC Analysis 
![Screenshot 2025-03-04 195745](https://github.com/user-attachments/assets/188d8faf-a60d-4925-a8fc-269bb4e049a0)

### ** Step 2**
### Transient Analysis
![Screenshot 2025-03-04 195842](https://github.com/user-attachments/assets/746ec562-0218-453f-8959-07b895811b9c)

![Screenshot 2025-03-04 195858](https://github.com/user-attachments/assets/6149c5fe-1fca-4413-a7fb-a73fbc3b07bf)

### **Step 3**
### AC Analysis

![Screenshot 2025-03-04 200041](https://github.com/user-attachments/assets/1e6a97d4-c924-48ce-8f5d-b39499bc4add)


## Result and Inference

Vdd = 2.2 V

Vp = 0.4 V

VICM = 1.2 V

VOCM = 1.25 V

RD = 1.9 kohm

Rss = 400 ohm

Iss = 1mA

ID = .5 mA



 
   - When a sudden change (step input) is applied to the differential amplifier, the circuit takes some time to settle due to capacitances (parasitic and intentional) in the system.  
   - This results in an initial overshoot or undershoot before stabilizing.  

   - A rapid change in input voltage can momentarily **shift the operating point** of transistors, leading to temporary distortion or non-linearity.  
   - If the circuit is not properly biased, large input variations may push transistors into saturation or cutoff regions, affecting amplification.  
     
   - A sudden increase in input voltage leads to a rapid increase in collector/drain current, which can generate heat and potentially **alter transistor parameters** .  
   - In extreme cases, excessive current surges could damage transistors if proper current limiting is not in place.  

   - If the power supply undergoes sudden voltage changes, it can cause **glitches** in the output due to transient response limitations of the amplifier.  
   - Using a **constant current source** as the tail current can help improve stability against such variations.  
 
   - Sudden changes in input signals can introduce **ringing or oscillations** due to parasitic capacitances and inductances in the circuit.  

   - By running **transient analysis** in LTspice the response time, overshoot, and stability of the circuit can be observed.  
   - A **step input** can be used to analyze how quickly the amplifier settles to a steady-state output.  











