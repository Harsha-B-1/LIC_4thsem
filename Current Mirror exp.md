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
|  M3       |   0.0002778           |             

![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cmt_1.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cmac_1.png?raw=true)
<br>
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_c.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_dc.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_t.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/cm2_ac.png?raw=true)
<br>
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_cir.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_dcop.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_ta.png?raw=true)
![](https://github.com/Harsha-B-1/LIC_4thsem/blob/main/da_ac.png?raw=true)
