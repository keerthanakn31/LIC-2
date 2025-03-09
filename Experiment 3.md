# EXPERIMENT 3
 **DIFFERENTIAL AMPLIFLIER** 


**AIM** : Design and analyze the MOS Differential ampliflier circuit.

**THEORY**<br/>
 A differential amplifier is an electronic device designed to amplify the difference between two input signals, Whereas a normal amplifier,which amplifies a single input signal. The basic differential amplifier consists of Two Input Terminals,Amplification stage,Output.<br/>

 **IDEAL DIFFERENTIAL AMPLIFIER :** IN an ideal case,a differential amplifier would have infinite common-mode rejection,meaning it would prefectly reject any common-mode signals ans amplify only the difference between V1 and V2.<br/>
 
 **PRACTICAL DIFFERENTIAL AMPLIFIER:** In practice, real differential amplifiers are not prefect and will have a finite CMRR.This means that while they are excellent at rejection common-mode signals,they will still amplify a small portion of any common-mode signal.<br/>


**Key characteristics:**

- High Common-Mode Rejection Ratio (CMRR): The differential amplifier rejects common-mode signals, which are signals that are present on both input lines.

- High Differential Gain: The differential amplifier amplifies the difference between the two input signals.

- Low Noise: The differential amplifier has low noise, making it suitable for use in high-precision applications.


 **Objectives:**
 1. To understand the operation of differential amplifier.
 2. To obtain gain and to observe the moods of operation.

 **Procedure**<br/>

 Step 1 : DC Analysis:<br/>
1.Connect the circuit as per the circuit diagram<br/>
2.Fix the appropriate Q point,set the Rd and Rss value to operate in saturation<br/>
3. set the length as 180n and vary the width untill we get required vout<br/>
4.Increase Vicm to 1V and observe Vocm,Vp<br/>
5.Calculate input swign and output swign<br/>
6.Gain Equation using smallsignal modle<br/>

Step 2 : Transient Analysis:<br/>
1.Apply Vinp-pmax and verify the output, calculate gain if the output is linear<br/>
2.In transient analysis there should be 180 degree phase shift <br/>

Step 3 : AC Analysis:<br/>
1.Find the 3-db BW<br/>

In case 1 resister RSS and do the step by step procedure<br/>
In case 2 Replace the resistor in the circuit by Current source do the same procedure <br/>
In case 3 replace it by N Channel Mosfet do the same procedure <br/>

**Design Question**

Design and analyze the differential amplifier for the following  specifications:
Vdd=2.2V, P<=2.2mw ,Vincm=1.2V ,Vocm=1.25V, Vp=0.4V<br/>
perform DC analysis,transient analysis,frequency response and extract parameters.


**CIRCUIT DESIGN**
![Image](https://github.com/user-attachments/assets/e06727e3-7cfc-41bc-b08e-582b1622c279)

**CALACULATION**

![Image](https://github.com/user-attachments/assets/288115bb-f7d7-41a5-9d67-cc5ed99aef5c)

Iss = 1mA<br/>
Id = 0.5mA<br/>
RD = 1.9Kohm<br/>
Rss = 400ohm<br/>


# CASE 1 : Differential ampliflier circuit with Resistor 


![Image](https://github.com/user-attachments/assets/e06727e3-7cfc-41bc-b08e-582b1622c279)

**Step 1:   DC Analysis**


For dc analysis we fix the length as 180n and then varying the width value untill we get the required Vocm as 1.25V <br/>
Length=180n<br/>
Width = 6.4125u<br/>

![Image](https://github.com/user-attachments/assets/3782e659-a2b5-4f00-a28a-69d930970a31)

From above analysis we can observe:<br/>
Vocm1 = Vocm2 + 1.25V<br/>
Id1 = Id2 = O.5mA and Iss = 1 mA<br/>

From Error log 
![Image](https://github.com/user-attachments/assets/8e932e72-02c1-4c15-baf9-13229dbd3c28)

We got the <br/>
Vgs = 0.8V , Vds = 0.85V , Vth = 0.495V , Id = 0.5mA  , Q-Point ( 0.85V , 0.5mA ) <br/>
 Vds > Vgs - Vth <br/>
 Hence the mosfet operates in saturation region<br/>

 **Step 2 : Transient Analysis**


 ![Image](https://github.com/user-attachments/assets/ddb293fd-17bf-44c9-ae73-d72e826855f7)

  To perform transient analysis we need to find the input and output maximun and minimun swing.<br/>

**INPUT SWING**<br/>
  Vincm(min)</sub> = Vth + Vp <br>
= 0.366 + 0.4 <br>
= 0.766 V <br><br>
Vincm(max)</sub> = Vdd - ( Id * Rd ) + Vth <br>
= 2.2 - ( 0.5m * 1.9K ) + 0.366 <br>
= 1.616 V <br><br>
**OUTPUT SWING**<br/>
Vocm(min)</sub> = Vov1 + Vp   <br>
= Vgs - Vth +Vp  <br>
= 0.8 - 0.36 + 0.4 <br>
= 0.84 V <br><br>
Vocm(max)</sub> = Vdd - ( Id * Rd ) <br>
= 2.2 - ( 0.5m * 1.9K) <br>
= 1.25V <br><br>

**Step 3 : AC Analysis**

![Image](https://github.com/user-attachments/assets/8e6ffb35-4cc6-40a3-8c55-b87b5d44d9d5)


We observed maginitude in the Ac analysis graph as 12.12db ,nothing but <br/>
Gain = 12.12db<br/>





Finding gain through calculation:<br>
Av = (Vocm1 - Vocm2)/(Vin1-Vin2)<br>
   = 397.869/99.285<br>
   = 4.007V/V<br>
In 3db = 20log(4.007)<br>
       =  12.06db <br>

To find bandwidth :<br>
12.12 db - 3db = 9.12db<br>
frequency for gain 9.12 = 21.7GHz<br>
Bw = f<sub>h</sub> - f<sub>l</sub> <br>
   = 21.7Ghz -0Hz + 21.7GHz <br>


   
   
# CASE 2: Differential amplifier circuit with current source 

In this case we just replace the resistor Rss by Current source I
**Circuit**

![Image](https://github.com/user-attachments/assets/e9229b24-3467-492b-b0fd-b6ef1d37c689)


**Step 1 : DC analysis**

For dc analysis we fix the length as 180n and then varying the width value untill we get the required Vocm as 1.25V <br/>
Length=180n<br/>
Width = 8.5u<br/>

 ![Image](https://github.com/user-attachments/assets/7ecee57f-8102-4687-a03e-6e94c4635e3f)
 
From above analysis we can observe:<br/>
Vocm1 = Vocm2 + 1.25V<br/>
Id1 = Id2 = O.5mA and Iss = 1 mA<br/>

From Error log 

![Image](https://github.com/user-attachments/assets/a37905b5-6ca9-48b4-a87c-a62446e90660)


We got the <br/>
Vgs = 0.8V , Vds = 0.85V , Vth = 0.495V , Id = 0.5mA  , Q-Point ( 0.85V , 0.5mA ) <br/>
 Vds > Vgs - Vth <br/>
 Hence the mosfet operates in saturation region<br/>
 In this stimulation we can conclude that there is no much difference in the resistor and current source 

 **Step 2 : Transient Analysis**

![Image](https://github.com/user-attachments/assets/b73785b7-fa3a-41b1-909e-d2fa0ac0883c)


  To perform transient analysis we need to find the input and output maximun and minimun swing.<br/>

**INPUT SWING**<br/>
  Vincm(min)</sub> = Vth + Vp <br>
= 0.366 + 0.4 <br>
= 0.766 V <br><br>
Vincm(max)</sub> = Vdd - ( Id * Rd ) + Vth <br>
= 2.2 - ( 0.5m * 1.9K ) + 0.366 <br>
= 1.616 V <br><br>
**OUTPUT SWING**<br/>
Vocm(min)</sub> = Vov1 + Vp   <br>
= Vgs - Vth +Vp  <br>
= 0.8 - 0.36 + 0.4 <br>
= 0.84 V <br><br>
Vocm(max)</sub> = Vdd - ( Id * Rd ) <br>
= 2.2 - ( 0.5m * 1.9K) <br>
= 1.25V <br><br>

**Step 3 : AC Analysis**





We observed maginitude in the Ac analysis graph as db ,nothing but <br/>
Gain = db<br/>


![Image](https://github.com/user-attachments/assets/4dfb2bad-1cb8-4de9-b9f4-255c3e39fd26)


Finding gain through calculation:<br>
Av = (Vocm1 - Vocm2)/(Vin1-Vin2)<br>
   = 476.699/119.144<br>
   = 4.008V/V<br>
In 3db = 20log(4.008)<br>
       =  12.04db <br>

To find bandwidth :<br>
12.04db - 3db = 9.04db<br>
frequency for gain 9.04 = 21.4GHz<br>
Bw = f<sub>h</sub> - f<sub>l</sub> <br>
   = 21.4Ghz -0Hz + 21.4GHz <br>

# CASE 3 : Differential amplifier with NMOSFET 

In this case we just replace the current source with NMOSFET at source terminal

**CIRCUIT**






    
 

