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
2. Vov=> Vgs-Vt
3. Id=1/2Kn Vov^2
