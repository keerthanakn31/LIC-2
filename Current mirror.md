# CURRENT MIRROR
**AIM** : Design and analyse the Current Mirror circuit.<br>

**THEORY** : 
<br> A current mirror is an electronic circuit designed to copy(or mirror) a reference current from one active device to another. It ensures that the output current remains nearly identical to the reference current, regardless of voltage variations or loading conditions.<br>

**Basic principle**
<p> The current mirror relies on the principle that identical transistors(BJTs or MOSFETs)operating at the same conditions will have the same current.<br>
  
**For a MOSFET Current Mirror**
<P>1.A MOSFET current mirror works similarly but uses the V_GS voltage.
<p>2.The first MOSFET (M1) is diode connected,setting its V_GS.
<p>3.The second MOSFET (M2) has the same V_GS,so it conducts the same current.

**Procedure**:
 1.Open LTspice and click on File->New schematic. <br>
 2.Build the current mirror circuit.<br>
 3.Set up Simulation Parameters.<br>
  4.Run the simulation. <br>
  5.Expected Results.<br>
**Design question**
  Design and analyse the current mirror circuit active load in the amplifier circuit. <br>
  given:VDD=1.8V,P<=1mW,Av=10V/V. <br>

 **Circuit diagram from LT spice**  <br>
 
![Image](https://github.com/user-attachments/assets/4f955232-1e9f-4813-a766-a502c4eba14f)


**Case 1:for length 180nm.** 
**For mirror ratio 1:1** <br>
WKT It=l\Iref+Id Therefore, for 1:1 ratio l\Iref=Id So,Iref=It/2 It=P/Vdd It=1mW/1.8V It=0.555mA. Therefore,Iref=0.277mA.<br>
To obtain the current value according to the given ratio, the provided values of W/L for M1 is 10um/180nm, M2 is 10um/180um, and M3 is um/180um. Vin to be in saturation region so considering Vin is V.<br>





**DC Analysis** <br>

![Image](https://github.com/user-attachments/assets/b2324549-1dec-4634-9a95-c123b9846bd6)
From DC analysis:<br>
Vout=      =Vx. <br>
Iref=Id=277uA. <br>



**Transient Analysis**




DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**



![Image](https://github.com/user-attachments/assets/8dd2014e-2392-4823-829b-d38eae585405)

Gain=29.28dB.<br>
29.28-3=26.28 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |180 nm      |   180 nm  | 180 nm    |   
|Width       |10 um       |   10 um   |           |
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 

**For mirror ratio 1:2**<br>
**DC Analysis** <br>
From DC analysis:<br>
Vout=      =Vx. <br>
Iref=Id=277uA. <br>



**Transient Analysis**






DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**





Gain=29.28dB.<br>
29.28-3=26.28 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |180 nm      |   180 nm  | 180 nm    |   
|Width       |10 um       |   10 um   |           |
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 

**Case 2:for length 500nm.** <br>
**For mirror ratio 1:1** <br>
**DC Analysis** <br>
From DC analysis:<br>
Vout=      =Vx. <br>
Iref=Id=277uA. <br>



**Transient Analysis**






DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**





Gain=29.28dB.<br>
29.28-3=26.28 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |180 nm      |   180 nm  | 180 nm    |   
|Width       |10 um       |   10 um   |           |
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 

**For mirror ratio 1:2**<br>
**DC Analysis** <br>
From DC analysis:<br>
Vout=      =Vx. <br>
Iref=Id=277uA. <br>



**Transient Analysis**






DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**





Gain=29.28dB.<br>
29.28-3=26.28 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |180 nm      |   180 nm  | 180 nm    |   
|Width       |10 um       |   10 um   |           |
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 






















 
  

  
  




