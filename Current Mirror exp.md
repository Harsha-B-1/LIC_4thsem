# Experiment 6:
## PART-A
### Design and analyze current mirror circuit as active load in amplifier circuit 
 <br>
 Circuit Diagram<br>

<br> ![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm_cir.jpg?raw=true)<br>
## _**FOR DESIGN**_

we need to design current mirroring for Av>10, VDD=1.8 and P<3mV.

total current in the circuit should be ratio of power and Vdd, and total current is sum of reference current and current through M2

that is I(total)=p/VDD

which is equal to 0.555mA

I(total)= Ireff + Ix

for current mirror ratio 1:1

I(total)=2*Iref

therefore Ireff=0.277mA<br>
To obtain the current value according to the given ratio, the provided values of W/L for M1 is 3um/180nm , M2 is 3um/180nm, and M3 is 3um/180nm.<br>
Vin is selected in such a way that it should be in saturation region so the given Vin is 0.838V.<br>




## _**FOR SIMULATION**_

as per the circuit diagram M1 is NMOS and M2 and M3 is PMOS.

for maintaining the stability i am using Vin as half of VDD. for perfect current mirroring the length of the osfet should be large more than 180nm,

so Vdd=1.8V, Vin=0.85V, L(M1,M2,M3)=180nm, Ireff=0.277mA.

now for this values we need to find the value of width(W) of the channel so that we will get exactly Ireff = Ix.

from trial and error it was found to be 2.85um(w1). for current mirror 1:1.

after simulation we get the below DC operating points<br>

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cmdc_1.png?raw=true)
<br>

for confirming the results we need to clarify that all the transisters are in saturation region(Vds>=Vov) so i foud the respective values,<br>

**(b)L=500nm.**
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm_la1.png?raw=true)<br>


We know the (w/L) ratio is 8.333um.

Therefore for L=500nm the w=8.334um.

|Mosfet     |  Id (mA)              |  
|-----------|-----------------------|
|  M1       |   0.243               |             
|  M2       |   0.243               |             
|  M3       |   0.2778              |  <br>

**(c)L=1um.**
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm_la2.png?raw=true)
We know the (w/L) ratio is 16.667.

Therefore for L=1um the w=16.667um.


|Mosfet     |  Id(mA )              | 
|-----------|-----------------------|
|  M1       |   0.2389              |             
|  M2       |   0.2389              |             
|  M3       |   0.0002778           |         <br>

## Transient Analysis:

#### Steps for transient Analysis:

* Replace DC input with an AC signal.
* Use SINE(dc_offset, Amplitude, Frequency).
* Go to "Simulate" > "Edit Simulation Cmd" > "Transient".
* Set Stop Time: 10ms.
* Run the simulation.
* Our dc_offset = 0.85V and assume amplitude as 50mV and frequency as 1KHz.
<br>

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cmt_1.png?raw=true)<br>
## AC Analysis:
#### Steps to get Ac analysis Waveform:
- In simulation tab select AC Analysis.
- In the AC Analysis tab, select **Type of Sweep as Decade**.
- Enter the number of points per decade (ex:20) and the frequency range ( 0.1Hz to 1THz).<br>

**OutPut Waveform:**<br>
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cmac_1.png?raw=true)
<br>
The Expected gain in db of the circuit is 20db.But the obtained gain from the AC analysis(frequency response) is 22.16db.

|Parameter      |Theory value  | Practical value |
|---------------|--------------|-----------------|
|Av(in dB)      | 20dB         | 21.76dB         |
|Av(in V/V)     | 10           | 9.87            |<br>

**3db Bandwidth:**

The obatined 3db B.W = 4 GHz.<br>
## DC Analysis:(for mirror ratio 1:2)

As we know It=Iref+Ix<br>
Therefore, for 1:2 ratio 2*Iref=Ix<br>
So,Iref=It/3<br>
It=P/Vdd<br>
It=1mW/1.8V<br>
It=0.555mA.<br>
Therefore,Iref=0.185mA.<br>
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_c.png?raw=true)
<br>m

To obtain the current value according to the given ratio, the provided values of W/L for M1 is 6um/180nm , M2 is 6um/180nm, and M3 is 4.9um/180nm.<br>
Vin is selected in such a way that it should be in saturation region so the given Vin is 0.8V.<br>
**Obtained Output:**


![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_dc.png?raw=true)
## Transient Analysis:

#### Steps for transient Analysis:

* Replace DC input with an AC signal.
* Use SINE(dc_offset, Amplitude, Frequency).
* Go to "Simulate" > "Edit Simulation Cmd" > "Transient".
* Set Stop Time: 10ms.
* Run the simulation.
* Our dc_offset = 0.763V and assume amplitude as 50mV and frequency as 1Khz.

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_t.png?raw=true)<br>
#### Steps to get Ac analysis Waveform:
- In simulation tab select AC Analysis.
- In the AC Analysis tab, select **Type of Sweep as Decade**.
- Enter the number of points per decade (ex:20) and the frequency range ( 0.1Hz to 1THz).

**OutPut Waveform:**

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_ac.png?raw=true)
<br>
The Expected gain in db of the circuit is 21.34db.But the obtained gain from the AC analysis(frequency response) is 24.6db.

|Parameter      |Theory value  | Practical value |
|---------------|--------------|-----------------|
|Av(in dB)      | 21.34dB      | 23.6dB          |
|Av(in V/V)     | 10           | 10.37           |

**3db Bandwidth:**

The obatined 3db B.W=1.58GHz.<br>
----------------------------------------------------------------------
# PART-B
## Aim
Design the differential amplifier using the same design specification as Experiment-3.
Perform DC analysis,trasient and AC analysis.

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_cir.png?raw=true)
### DC Analysis:
Here’s a well-structured explanation of the **DC Analysis** for your circuit while ensuring that all MOSFETs operate in the **saturation region** and match the experimental results.
## **DC Analysis of the Given Circuit**

### **1. Overview of the Circuit**
The circuit consists of six MOSFETs (M1 to M6) with different **(W/L) ratios**, and we need to ensure that all transistors remain in the **saturation region** during the analysis. The given (W/L) ratios for each transistor are:

- **M1**: 7μm / 180nm  
- **M2**: 7μm / 180nm  
- **M3**: 6.1μm / 180nm  
- **M4**: 3.5μm / 180nm  
- **M5**: 7μm / 180nm  
- **M6**: 7μm / 180nm  

Since the circuit must maintain the same **current and voltage values** as in Experiment 3, the **DC operating point (biasing conditions)** is determined accordingly.

---


### **2. DC Analysis - Ensuring Same Current & Voltage Values**
DC analysis involves finding the **DC operating points (voltages and currents)** of each MOSFET. Based on Experiment 3, we ensure the following:

- **Current Matching:** The drain current (\( I_D \)) of matched transistors (M1, M2, M3) must be the same.
- **Voltage Consistency:** The node voltages should match experimental results.

Since **M1, M2, and M3** have the **same W/L ratio**, they will have identical drain currents, ensuring symmetry.

For **M4, M5, and M6**, their **(W/L) ratios differ**, but they must still be biased properly to maintain the same experimental **current and voltage values**.

---

### **3. Steps to Verify the DC Analysis**
1. **Compute \( V_{GS} \) for each transistor**  
   - Ensure each MOSFET is in **saturation** by checking \( V_{GS} \) and \( V_{th} \).
   
2. **Find the DC operating point (voltages and currents)**  
   - Solve Kirchhoff’s Current Law (KCL) and Kirchhoff’s Voltage Law (KVL) equations.
   
3. **Check consistency with Experiment 3 results**  
   - Verify that **simulated values** match **measured values** in the lab.


**Output:**

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_dcop.png?raw=true)
### Transient Analysis:

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_ta.png?raw=true)<br>
#### Steps to get Ac analysis Waveform:
- In simulation tab select AC Analysis.
- In the AC Analysis tab, select **Type of Sweep as Decade**.
- Enter the number of points per decade (ex:20) and the frequency range ( 0.1Hz to 1THz).

**Output Waveform:**

The Expected gain in db of the circuit is 22.72db.But the obtained gain from the AC analysis(frequency response) is 30.1db.<br>
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_ac.png?raw=true)<br>
|Parameter      |Theory value  | Practical value |
|---------------|--------------|-----------------|
|Av(in dB)      | 21.34dB      | 30.1dB          |
|Av(in V/V)     | 8.6          | 13.68           |<br>
**3db Bandwidth:**

The obatined 3db B.W=1.412MHz.<br>
## Inference
The observed higher-than-expected gain in the circuit likely stems from parasitic effects or device mismatches, highlighting practical non-idealities. Additionally, the high bandwidth (100mHz to 504MHz) reaffirms its suitability for high-frequency applications, with gain deviations possibly linked to underestimated drain resistance or variations in transconductance.<br>

Current mirrors are essential in analog IC design, providing precise bias currents while minimizing process variation effects. Despite minor discrepancies due to second-order MOSFET characteristics and process-dependent factors like channel length modulation, the design remains robust. This underscores the importance of current mirrors in ensuring stable, efficient operation in high-performance circuits.<br>

Current mirrors are vital for biasing circuits, particularly in differential amplifiers, as they ensure consistent operation with minimal fluctuations. Using NMOS current mirrors as bias voltage sources enhances the gain, stability, and energy efficiency of differential amplifiers, establishing them as indispensable elements in contemporary analog IC design.<br>
