# CURRENT MIRROR
**AIM** : Design and analyse the Current Mirror circuit.<br>

**THEORY** : 
<br> A current mirror is an electronic circuit designed to copy(or mirror) a reference current from one active device to another. It ensures that the output current remains nearly identical to the reference current, regardless of voltage variations or loading conditions.<br>

**Basic principle**
<p> The current mirror relies on the principle that identical transistors(BJTs or MOSFETs)operating at the same conditions will have the same current.<br>
  
**For a BJT Current Mirror**
<p> 1.If two identical BJTs(Q1 and Q2) have the same V_BE,they should conduct the same current.
<p> 2.The first transistor (Q1) is diode-connected(its base and collector are shorted),ensuring it operates in the active region.
<p> 3.The reference current (I_ref)sets the current in Q1.
<p> 4.Since Q2 shares the same V_BE, it conducts a nearly identical current(I_out = I_ref).
  
**For a MOSFET Current Mirror**
<P>1.A MOSFET current mirror works similarly but uses the V_GS voltage.
<p>2.The first MOSFET (M1) is diode connected,setting its V_GS.
<p>3.The second MOSFET (M2) has the same V_GS,so it conducts the same current.

**Procedure**:
<p> 1.Open LTspice and click on File->New schematic.
<p> 2.Build the current mirror circuit.
<p> 3.Set up Simulation Parameters.
<p> 4.Run the simulation.
<p> 5.Expected Results.<br>
  
**Tabular Column:**
 | Iout(expected)(A)     |Iout(appeared)(A)   | (W/L)2(m)        |(W/L)1(m)   | Vx(V)  | Vout(V)|
 |-----------------------|--------------------|------------------|------------|--------|--------|
 |                       |                    |                  |            |        |        |
 |                       |                    |                  |            |        |        |
 |                       |                    |                  |            |        |        |
 |                       |                    |                  |            |        |        |
 |                       |                    |                  |            |        |        |

 





