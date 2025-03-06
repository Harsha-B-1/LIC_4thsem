# THE MOS DIFFERENTIAL PAIR AMPLIFIER <br>
1. A differential amplifier amplifies the differential-mode voltage while rejecting common-mode signals,characterized by a high common-mode rejection ratio (CMRR) and differential gain.
2. It is built using matched BJTs or MOSFETs, often incorporating a current mirror for biasing and an active load for improved gain and linearity.
## Applications
Used in operational amplifiers, instrumentation amplifiers, and analog front-end circuits, it enhances noise immunity and precision in signal processing systems.
### Q) Design a differential amplifier for the following specifications 
Vdd =2.5V | Vincm=1.3V | Vp=0.5V| P<=3mW|Vocm=1.4V

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
1. Matched MOSFETs (M1 & M2)
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


4. Drain Resistors(Rd)
Function: Convert drain current variations into voltage output.
Working:
The voltage drop across Rd determines the output voltage.
The differential output voltage is given by:
Vout =(I1-I2)Rd
Larger Rd increases voltage gain.

### *Advantages of FET-Based Differential Amplifier
 High input impedance (good for sensor applications).
 Low noise and power consumption.
 Good linearity and stability.
 Ideal for operational amplifiers, instrumentation amplifiers, and signal processing.
