# THE MOS DIFFERENTIAL PAIR AMPLIFIER <br>
1. A differential amplifier amplifies the differential-mode voltage while rejecting common-mode signals,characterized by a high common-mode rejection ratio (CMRR) and differential gain.
2. It is built using matched BJTs or MOSFETs, often incorporating a current mirror for biasing and an active load for improved gain and linearity.
## Applications
Used in operational amplifiers, instrumentation amplifiers, and analog front-end circuits, it enhances noise immunity and precision in signal processing systems.
### Q) Design a differential amplifier for the following specifications 
| Parameter |  value | 
|-----------|--------|
|VDD        | 2.5V   |
|Vp         | 0.5V   | 
|VinCM      | 1.3V   |
|VOcm       |1.4V    |


Perform DC analysis , Transient analysis , frequency response and extract the parameters.

### *circuit diagram and design
![Alt image](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/circuit%20design.jpg?raw=true)

### *Working of MOSFET-Based Differential Amplifier
A FET-based differential amplifier operates by amplifying the voltage difference between two input signals while rejecting common-mode signals. It is commonly implemented using MOSFETs or JFETs, providing high input impedance, low power consumption, and excellent noise immunity.

### *key equations 
1. Vgs>Vthn
2. Vds=>Vov   --> (Vgs-Vt)
3. Id=1/2Kn Vov^2
4. gm=Id/Vgs
5. Av=gm*Rd = 2Id *Rd/Vov (for differential amp)

### *Role of Each Component in a FET-Based Differential Amplifier
A FET-based differential amplifier consists of several key components, each playing a critical role in its operation. Below is a breakdown of their functions:

1.Matched MOSFETs (M1 & M2)
Function: Act as the active amplifying devices.
Working:
The gate terminals receive differential input signals.

The drain currents vary based on the difference in gate-source voltages.

The transistor with a higher gate voltage conducts more current, lowering its drain voltage, and vice versa.


2.Common Source Connection
Function: Both MOSFET sources are connected together to a current source.

Working:
Ensures that the current splits between the two transistors dynamically.
Helps maintain differential operation.


3.Common Source Connection
Function: Both MOSFET sources are connected together to a current source.
Working:
Ensures that the current splits between the two transistors dynamically.
Helps maintain differential operation.


4.Drain Resistors(Rd)
Function: Convert drain current variations into voltage output.

Working:
The voltage drop across Rd determines the output voltage.
The differential output voltage is given by:
Vout =(I1-I2)Rd
Larger Rd increases voltage gain.

###Summary of Component Roles

| Component           | Function                                         |
|---------------------|--------------------------------------------------|
|MOSFETs (M1 & M2)    | Act as the main amplifiers.                      | 
|Common Source        | Provides a shared reference for both transistors |
|Current Source(Ibias)| Sets the operating point and stabilizes current. |
|Drain Resistors(Rd)  | Convert current variations into voltage signals. |


### *Advantages of FET-Based Differential Amplifier
 High input impedance (good for sensor applications).
 Low noise and power consumption.
 Good linearity and stability.
 Ideal for operational amplifiers, instrumentation amplifiers, and signal processing.

 
 ### Circuit Diagram
 ![Alt image](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/c1.png?raw=true)
 
 
 ### DC Analysis
 Procedure 
<br> 1.Make the circuit connections as per diagram.<br>
<br>2.set w/L = 180nm/ 7.59995um such that Id becoes 5.9mA.<br>
<br>3. Even though the given parameter is 6mA ,it is bettter keep the value ratherthan exceeding , because in large scale millions and billions of transistors are used there power consumption of each fet will addup and make device less relaiable.<br>

 Oparating point
 ![Alt image](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/c1dc.png?raw=true)
 

| Parameter    | Theoretical value  | Practical value |
|--------------|--------------------|-----------------|
|Voutcm        | 1.40 V             | 1.40037 V       |
|Vp            | 0.5 V              | 0.498 V         |
|Id1,Id2       | 0.6 mA             | 0.598mA         |
|Id(R3)        | 1.2 mA             | 1.1965 mA       |
|Rd            | 1.83 kohm          | 1.838 kohm      |
|Rss           | 416.67 ohm         | 416ohm          |
|Vgs           | 0.8 V              | 0.801V          |
### Finding input and output swing
<br>therefore Q point = (Vds,Id) = (0.9V,0.598mA).<br>
 Vincm(min)= Vth + Vp = 0.37 + 0.5 = 0.87V <br>
 Vincm(max) = Vdd - (Id*Rd) + Vth = 1.77V <br>
 0.87V < Vin <1.77V(input swing)<br>
 Vout(min) = Vov1 + Vov3 = (0.8-0.37)+0.5 = 0.93V <br>
 Vout(max) = Vdd-(Id*Rd) = 1.4007V <br>
 0.93V<Vo<1.4007V
<br>
### Transient Analysis
procedure
* Replace DC input with an AC signal.
* Use SINE(dc_offset, Amplitude, Frequency).
* Go to "Simulate" > "Edit Simulation Cmd" > "Transient".
* Set Stop Time: 10ms.
* Run the simulation.
* Our dc_offset = 1.3V and assume amplitude as 50mV and frequency as 1Khz
  <br> Case 1: Vin <0.5V (50m amp)<br>
  ![Alt image](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/c1_bll.png?raw=true)
  ![Alt image](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/c1_ll.png?raw=true)
  ![image](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/c1_Q.png?raw=true)
