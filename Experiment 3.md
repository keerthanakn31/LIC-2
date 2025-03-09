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

 Gm = 2Id/Vov =  2*1m/0.8-0.366 = 2.3V/V<br>
Av = Gm * Rd = 2.3 * 1.9K = 4.37V/V<br> 

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


![Image](https://github.com/user-attachments/assets/9eff02cf-1c01-4e4f-8883-0347395f727c)


We observed maginitude in the Ac analysis graph as 12.12db ,nothing but <br/>
Gain =12.12 db<br/>

![Image](https://github.com/user-attachments/assets/567984eb-1506-431f-8647-1bd6b2621abb)



Finding gain through calculation:<br>
Av = (Vocm1 - Vocm2)/(Vin1-Vin2)<br>
   = 399.459/99.121<br>
   = 4.0301V/V<br>
In 3db = 20log(4.0301)<br>
       =  12.106db <br>

To find bandwidth :<br>
12.11db - 3db = 9.11db<br>
frequency for gain 9.11 = 21.7GHz<br>
Bw = f<sub>h</sub> - f<sub>l</sub> <br>
   = 21.7GHz -0Hz = 21.7GHz <br>

# CASE 3 : Differential amplifier with NMOSFET 

In this case we just replace the current source with NMOSFET at source terminal

**CIRCUIT**

![Image](https://github.com/user-attachments/assets/1880b1d8-0f0c-4c78-9b24-0fdf3b0128bc)

**Step 1 : DC analysis**

For dc analysis we fix the length as 180n for 3 transistors M1,M2,M3 and then varying the width value untill we get the required Vocm as 1.25V <br/>
Length=180n for M1,M2,M3<br>
Width = 8.5u for M1 and M2 transistors <br>
Width = 9.4616u for M3 transistor<br>

![Image](https://github.com/user-attachments/assets/79c03c57-b4e4-47ef-9756-bba713bf3d11)

From above analysis we can observe:<br/>
Vocm1 = Vocm2 + 1.25V<br/>
Id = 1mA<br/>

From Error log 

![Image](https://github.com/user-attachments/assets/ac543489-4eda-4f4b-b20d-a9818b397ef8)

Vgs of all the mosfet id greter than Vth ,
Vds>Vgs-vth ,
hence it is in saturation <br>

Gain = (2*Id3)/(Vov3)<br>
= (2*0.5m)/(0.8-0.495)
=2.51mV/V<br>

 **Step 2 : Transient Analysis**


![Image](https://github.com/user-attachments/assets/782bd146-b1c0-4442-86c4-b9baa0cec8cf)


  To perform transient analysis we need to find the input and output maximun and minimun swing.<br/>

**INPUT SWING**<br/>
  Vincm(min)</sub> = Vth + Vp <br>
= 0.496 + 0.4 <br>
= 0.896 V <br><br>
Vincm(max)</sub> = Vdd - ( Id * Rd ) + Vth <br>
= 2.2 - ( 0.5m * 1.9K ) + 0.496 <br>
= 1.746 V <br><br>
**OUTPUT SWING**<br/>
Vocm(min)</sub> = Vov1 + Vp   <br>
= (Vgs1 - Vth) +(Vgs3 - Vth)  <br>
= (0.753 - 0.496) + (0.895 - 0.496) <br>
= 0.656 V <br><br>
Vocm(max)</sub> = Vdd - ( Id * Rd ) <br>
= 2.2 - ( 0.5m * 1.9K) <br>
= 1.25V <br><br>


**Step 3 : AC Analysis**


![Image](https://github.com/user-attachments/assets/a04393f1-e579-47cd-af37-dcccdaa40c9c)


We observed maginitude in the Ac analysis graph as 13.75db ,nothing but <br/>
Gain = 13.75db<br/>


![Image](https://github.com/user-attachments/assets/2985d292-cfdc-4a7a-89ad-8c7ae813d796)


Finding gain through calculation:<br>
Av = (Vocm1 - Vocm2)/(Vin1-Vin2)<br>
   = 525.86400/109.14217<br>
   = 4.8181V/V<br>
In 3db = 20log(4.8181)<br>
       =  13.65db <br>

To find bandwidth :<br>
13.65db - 3db = 10.65db<br>
frequency for gain 10.65 = 16.71GHz<br>
Bw = f<sub>h</sub> - f<sub>l</sub> <br>
   = 16.71Ghz -0Hz = 16.71GHz <br>



### RESULT

|  PARAMETERS    |  CASE 1 (with Rss)    |  CASE 2 (with Current source) |  CASE 3(with NMOS | 
|----------------|-----------------------|-------------------------------|-------------------|
|   Vincm        |   1.2V                |       1.2V                    |   1.2V            |
|  Vocm          |   1.25V               |      1.25V                    |   1.25v           |
|  Vp            |   0.4V                |    0.4V                       |   0.4V            |
| Id             |0.5mA                  |0.5mA                          |  0.5mA            |
| Rd             |  1.9Kohm              |  1.9Kohm                      |  1.9Kohm          |
|  Avdm          |  4.007V/V             |                               |     4.8181V/V     |
|  Gain in db    |  12.06db              |                               |     13.65db       |
| Bandwidth      |   21.7GHz             |                               |    16.71GHz       |


 **INFERENCE**
 - The gain changes in each circuit because of output resistance.
 - The DC operating point remains same in all 3 cases.
 - by replacing Rss with current source gain will not changes more it remains almost same but by replacing it bt NMOS affets the gain,biasing and input impedence.
 -Comparing 3 cases in case 3 it has high gain.


