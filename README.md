# Experiment 1 - circuit 2:

**Transient AC and DC analysis of common source ampliflier**

![Image](https://github.com/user-attachments/assets/924a28ea-fda1-440a-9d24-e2438bbbed8d)

<p> The circuit represents the common source ampliflier. To determine the Dc,Ac and Transient analysis of the CS ampliflier circuit. Here we replace the resistor by PMOS .</p> <br>

**COMPONENTS**
<p>
  This circuit consists of TSMC 180nm Transister ,register and voltage source <br> 
  MOSFET LENGTH : 180nm <br>
  MOSFET WIDTH :   5.3um    <br>
  Threshold voltage : 0.36 <br>
  PMOS and NMOS  <br>
  Supply voltage : 1.8V <br>
  Signal generater : 0.7V   <br>
  DC voltage : 1.9V     <br>
  Amplitude :  50mV   <br>
  Frequency :   1k   <br> 
  Gate volt : 0.7<br>

</p> <br>

**DC Analysis**

![Image](https://github.com/user-attachments/assets/25559551-c57b-4206-a4ab-89199bad6401)
![Image](https://github.com/user-attachments/assets/682654ab-12d1-408a-8f3f-f5e5af9f0caf)

<p>
From the analysis we got<br> 
Vout =1.8V    <br>
Vin =950mV <br>
Id = 5.54093e-11     <br>
 If the power dessipation is 100um  across the register ,then 
 currengt  throught the resister is<br>
 Id = 100um/1.8 =55.5um<br>

</p> <br>

<p>
  Now replace the resister  by PMOS 
  Since the Calculated current doesnot match the simulated value, maintain the MOSFET length 180nm and vary the width untill the required current.  
</p>

<table>
  <tr>
    <td>Length</td>
    <td>Width</td>
    <td>Id</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>5um</td>
    <td>5.2752e-11</td>
  </tr>
  <tr>
  <td>180nm</td>
  <td>5.1um</td>
  <td> 5.36375e-11	</td>
  </tr><br>
  <tr>
    <td>180nm</td>
    <td>5.2um</td>
    <td> 5.45232e-11	</td>
  </tr>
    
  <tr>
    <td>180nm</td>
    <td>5.3um</td>
    <td> 5.54093e-11</td>
  </tr>
</table><br>

<p>
   The Dc operating point confirms that NMOS operates in saturation region.<br>
   DC operating point (1.8V , 55.5um)
   
</p>

**AC ANALYSIS**

![Image](https://github.com/user-attachments/assets/5d526ac7-a461-4120-a15c-c3f1fc9ac6ae)

<P>
  In AC analysis we determine the frequency response by appluing the small signal analysis to the circuit. we do this analysis to check in which frequency the circuit acts as a linear ampliflier.
  For this type of sweep we select 'decade', starting frequency as 0.1Hz and stop frequenct as 1THz.

</P><br>

**TRANSIENT ANALYSIS**



![Image](https://github.com/user-attachments/assets/d0f1a060-cf14-4521-8669-9f23ef014128)





<p>
  In Transient  Analysis we determine the gain of the circuit. For input we give sinusoidal voltage signal where the DC offset is 0.9v peak voltage Vpeak is 50mv, Frequency is 1kHz and AC amplitude is 1V. set the stop time to 3ms.
</p><br>

<p>
  Gain = Vout/Vin<br>
  Av =1.89 <br>
  This matches the theoritical value which is calculated but Av = gmRd.<br>
  where gm+ KnVov<br>
  From graph we can observe that there is 180 degree phase shift which is exhibitied by CS ampliflier.
  
</p><br>

**INFERENCE**
<p>
 Diode connected MOSFET will always be in the Saturation region.Replace register by PMOS, From DC analysis we get the dc operation point and confirms whether the mosfet is in saturation region.Transient amalysis  shows how the mosfet behave for the time varying Ac signal (sinewave), It shows that ampliflied output with phase shift of 180 degree.The voltage gain Av can be determined by looking at the ratio of the output to input signal magnitude.
The AC analysis helps to determine the small signal behaviour like gain.
These analyses are essential for designing and evaluating the performance of a common-source amplifier.
  
</p><br>

**RESULT**
<p>
  Vout= 1.8v  <br>
  Id=  5.54093e-11<br>
  Vin= 950mV   <br>
  Gain= 1.89   <br>
  
</p>

### COMPARISION TABLE:

|    Parameters      |        Circuit 1      |               Circuit 2              |
|--------------------|-----------------------|--------------------------------------|
|   Connection       | Resistor and NMOSFET  | NMOSFET and Diode connection PMOSFET |
|    length          |     180nm             |                180nm                 |
|     width          |     0.207um           |               5.2um                  |
|     Supply voltage |      1.8V             |                 1.8V                 |
|    Gate Voltage    |        0.9V           |                0.7V                  |
|     Vout           |      1.68879V         |               1.8V                   |
|     Power          |     100uW             |               100uW                  |
|      Current       |      55.5uA           |              55.5uA                  |
|     Q point        | (1.6887V,55.5um  )    |     (1.8V , 55.5um)                  |
|     Phase shift    |       180 degree      |             180 degree               |
|     Gain           |    1.77               |             1.89                     |







  



























