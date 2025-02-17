# Experiment 1 - circuit 2:

**Transient AC and DC analysis of common source ampliflier**


<p> The circuit represents the common source ampliflier. To determine the Dc,Ac and Transient analysis of the CS ampliflier circuit. Here we replace the resistor by PMOS .</p> <br>

**COMPONENTS**
<p>
  This circuit consists of TSMC 180nm Transister ,register and voltage source <br> 
  MOSFET LENGTH : 180nm <br>
  MOSFET WIDTH :   5.3um    <br>
  Threshold voltage : 0.36 <br>
  PMOS and NMOS  <br>
  Supply voltage : 1.8V <br>
  Signal generater : 0.9V   <br>
  DC voltage : 1.9V     <br>
  Amplitude :  50mV   <br>
  Frequency :   1k   <br>  
</p> <br>

**DC Analysis**



<p>
From the analysis we got<br> 
Vout =1.68879V    <br>
Vin =950mV <br>
Id = 5.56046e-05     <br>
 If the power dessipation is 100um  across the register ,then 
 currengt  throught the resister is<br>
 Id = 100um/1.8 =55.5um<br>
 The output loadline is given by <br>
 Vout =Vdd-(Id-Rd)<br>
 Rd=(1.8-1.674)/55.5um<br>
   =2.751k ohms<br>
</p> <br>

<p>
  Now replace the resister value by Rd = 2.751891k ohm
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
   
</p>

**AC ANALYSIS**


<P>
  In AC analysis we determine the frequency response by appluing the small signal analysis to the circuit. we do this analysis to check in which frequency the circuit acts as a linear ampliflier.
  For this type of sweep we select 'decade', starting frequency as 0.1Hz and stop frequenct as 1THz.

</P><br>

<p>
  Gain = Vin/Vout<br>
  AV= 0.5625 <br>
  This matches the theoritical value which is calculated but Av = gmRd.<br>
  where gm+ KnVov<br>
  From graph we can observe that there is 180 degree phase shift which is exhibitied by CS ampliflier.
  
</p><br>


  



























