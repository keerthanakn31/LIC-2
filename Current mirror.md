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

  Design and analyse the current mirror circuit active load in the amplifier circuit. <br>
  given:VDD=1.8V,P<=1mW,Av=10V/V. <br>

 **Circuit diagram from LT spice**  <br>
 
![Image](https://github.com/user-attachments/assets/4f955232-1e9f-4813-a766-a502c4eba14f)


**Case 1:for length 180nm.** 
**For mirror ratio 1:1** <br>
WKT It=I/Iref+Id Therefore, for 1:1 ratio I/Iref=Id So,Iref=It/2 It=P/Vdd It=1mW/1.8V It=0.555mA. Therefore,Iref=0.277mA.<br>
To obtain the current value according to the given ratio, the provided values of W/L for M1 is 10um/180nm, M2 is 10um/180um, and M3 is um/180um. Vin to be in saturation region so considering Vin is V.<br>





**DC Analysis** <br>

![Image](https://github.com/user-attachments/assets/b2324549-1dec-4634-9a95-c123b9846bd6)
From DC analysis:<br>
Vout= 0.967276V  =Vx. <br>
Iref=Id=277uA. <br>



**Transient Analysis**

![Image](https://github.com/user-attachments/assets/cf976844-929d-4622-93d8-f069021ab2d5)


DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**



![Image](https://github.com/user-attachments/assets/8dd2014e-2392-4823-829b-d38eae585405)

Gain=29.317dB.<br>
29.317-3=26.317 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |180 nm      |   180 nm  | 180 nm    |   
|Width       |10 um       |   10 um   |  30.84967u|
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 

**For mirror ratio 1:2**<br>
**DC Analysis** <br>

![Image](https://github.com/user-attachments/assets/395c8cbd-aea3-4e27-b48c-553994e00451)

From DC analysis:<br>
Vout= 1.07288 <br>
Vx = 1.03495V
Iref=0.183mA<br>
Id = 361.4uA<br>


**Transient Analysis**


![Image](https://github.com/user-attachments/assets/dced0030-7c84-4e90-bdc0-aead110850b8)



DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**

![Image](https://github.com/user-attachments/assets/1869defc-b0d4-4ee5-a301-c545c709dd6c)






Gain=29.065dB.<br>
29.065-3=26.065 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |180 nm      |   180 nm  | 180 nm    |   
|Width       |10 um       |   20 um   |  40.426um |
|Current     |Iref=0.183mA|Id= 361.4uA|Id= 361.4uA| 

**Case 2:for length 500nm.** <br>

**For mirror ratio 1:1** <br>
**DC Analysis** <br>

![Image](https://github.com/user-attachments/assets/249eb4ae-3d7f-4a6f-adc6-58ade08a32a4)
From DC analysis:<br>
Vout= 0.6447V ,361.1V=Vx. <br>
Iref=Id=277uA. <br>



**Transient Analysis**
![Image](https://github.com/user-attachments/assets/2caa88b7-298b-4062-8841-095e9389e18d)





DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**

![Image](https://github.com/user-attachments/assets/44fcbb8d-78f7-42cf-8117-161203ff688a)



Gain=38.28dB.<br>
38.28-3=35.28 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |500nnm      |   500 nm  | 500 nm    |   
|Width       |10 um       |   10 um   | 67.0631u  |        
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 

**For mirror ratio 1:2**<br>

**DC Analysis** <br>
![Image](https://github.com/user-attachments/assets/6c67a4c6-faec-43f6-85bf-872e15a3569c)

From DC analysis:<br>
Vout= 1.65618V <br>    
Vx = 0.7936V <br>
Iref=0.183mA <br>
Id = 0.18302mA



**Transient Analysis**

![Image](https://github.com/user-attachments/assets/c5655dfa-4ac1-440c-9e16-410c47db7c7f)

DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**

![Image](https://github.com/user-attachments/assets/51916f84-f9c5-4594-babf-3206790c56e6)


Gain=7.743dB.<br>
7.743-3=4.743dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |500 nm      |   500 nm  | 500 nm    |   
|Width       |10 um       |   20 um   |39.701901u |
|Current     |Iref=0.183mA|  0.18302mA|0.18302  mA| 



**Case 3:for length 1um.** <br>

**For mirror ratio 1:1** <br>
**DC Analysis** <br>
![Image](https://github.com/user-attachments/assets/de68a57a-a9bc-4530-94d7-70b420e9f215)

From DC analysis:<br>
Vout= 0.2319V <br> 
Vx= 0.293177V <br>
Iref=Id=277uA. <br>



**Transient Analysis**

![Image](https://github.com/user-attachments/assets/cf69f7a6-cf69-4aab-9651-16dcb9a052c7)




DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**


![Image](https://github.com/user-attachments/assets/a7a5220f-8c52-44f3-81e0-c259c90e4f62)


Gain=35.471db<br>
35.471-3=32.471 dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |1um         |   1 um    | 1 um      |   
|Width       |10 um       |   10 um   | 97.048um  |        
|Current     |Iref=0.227mA|Id=0.227 mA|Id=0.227 mA| 

**For mirror ratio 1:2**<br>

**DC Analysis** <br>

![Image](https://github.com/user-attachments/assets/e1373f88-34b3-45c2-9545-ce81edcee0dc)

From DC analysis:<br>
Vout= 0.4357V <br>    
Vx = 0.5159V <br>
Iref=0.183mA <br>
Id = 183uA<br>



**Transient Analysis**

![Image](https://github.com/user-attachments/assets/458a5c87-1cbe-4f2f-a777-f309942a7148)


DC offset=0.5697V and amplitude=10 mV with frequency 1 kHz.<br>

**AC Analysis**

![Image](https://github.com/user-attachments/assets/ea4ee935-10c4-49a5-94c5-dd1bfff449ea)

Gain=39.268db<br>
39.268-3=36.268dB.<br>

|Parameters  |  MOSFET 1  | MOSFET 2  | MOSFET 3  |
|------------|------------|-----------|-----------|
| Length     |1um         |   1um     | 1um       |   
|Width       |10 um       |   20 um   |  65.256um |
|Current     |Iref=0.183mA|Id=0.183 mA|Id=0.183 mA| 

# PART B 

Design the differential amplifier using the same design specification as experiment 3(differential amplifier). Perform DC, Transient, AC analysis for this.<br>

**CIRCUIT**







**DC ANALYSIS**



![Image](https://github.com/user-attachments/assets/1e8b6e9a-deac-46cb-99b7-33974b840edc)





**TRANSIENT ANALYSIS**

![Image](https://github.com/user-attachments/assets/83a0a287-bd9d-403a-86a2-95df8175fad5)



**AC ANALYSIS***


![Image](https://github.com/user-attachments/assets/cadae9d3-eb2a-4219-a989-05eb138ca559)





















 
  

  
  




