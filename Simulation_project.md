# Design andesign and analyse Telescopic cascode differential amplifier and Folded cascode OTA 

# ABSTRACT
This work presents the design and analysis of two high-performance analog amplifier topologies: the Cascode Telescopic Differential Amplifier and the Folded Cascode Operational Transconductance Amplifier (OTA). 
The Telescopic Cascode Amplifier offers superior gain and bandwidth due to its stacked transistor architecture, making it well-suited for high-speed and low-noise applications. However, its limited output swing constrains its use in low-voltage environments.
To address this, the Folded Cascode OTA is explored as an alternative, leveraging a current folding technique that enhances output swing and common-mode input range while maintaining high gain. Comparative performance metrics including gain, bandwidth, power consumption, and input/output voltage range are evaluated through simulation in a standard CMOS process. The results highlight the trade-offs between the two architectures, providing insights into optimal topology selection based on application requirements.

# INTRODUCTION 
Operational amplifiers (op-amps) are fundamental building blocks in analog and mixed-signal integrated circuits, widely used in signal processing, data conversion, and communication systems. Among the various op-amp topologies, the Cascode Telescopic Differential Amplifier and the Folded Cascode Operational Transconductance Amplifier (OTA) are popular choices for applications requiring high gain, wide bandwidth, and low power consumption.
The Telescopic Cascode Amplifier is known for its excellent high-frequency performance, attributed to the reduced Miller effect and high output impedance achieved through cascode stacking. This topology is often preferred in high-speed and low-noise applications, such as high-resolution analog-to-digital converters and data acquisition systems. However, one major limitation of the telescopic architecture is its restricted output voltage swing, which becomes more pronounced in modern low-voltage CMOS processes.To overcome this constraint, the Folded Cascode OTA introduces a current folding mechanism, allowing for greater voltage headroom and improved input/output swing without sacrificing gain significantly. This makes it more suitable for low-voltage and low-power applications, such as portable electronics and biomedical devices.
This study investigates and compares both amplifier topologies in terms of their design principles, advantages, limitations, and performance metrics. By understanding the trade-offs between these architectures, designers can make informed decisions when selecting the optimal configuration for specific application requirements.

# DESIGN OVERVIEW
1.	**Cascode Telescopic Differential Amplifier**

The Cascode Telescopic Differential Amplifier is a high-gain, low-noise amplifier structure composed of a differential input pair with cascode transistors stacked above each branch. The core design consists of:
Differential input stage: Typically uses NMOS or PMOS transistors for better transconductance.
Cascode transistors: Connected above the input pair to increase output resistance and reduce the Miller effect.
Current sources: Provide biasing for both the input differential pair and cascode stages.
Load: Usually implemented as active current mirrors for high output impedance.
This topology offers high gain and excellent bandwidth due to its reduced parasitic capacitance and enhanced output resistance. However, the stacking of multiple transistors limits the output swing, making it less suitable for low-voltage designs.
2.	**Folded Cascode Operational Transconductance Amplifier (OTA)**

The Folded Cascode OTA modifies the telescopic structure by "folding" the current from the input pair into a different branch, improving voltage headroom. The design includes:
Differential input pair: Usually NMOS (for higher transconductance) that drives PMOS cascode devices.
Folding mechanism: The current from the input NMOS devices is folded into PMOS devices, which allows the circuit to avoid stacking all transistors vertically.
Cascode transistors: Maintain high output impedance and gain.
Output stage: Typically a current mirror or load that provides a single-ended output.
This design enhances output swing, common-mode input range, and power efficiency, making it ideal for low-voltage, low-power applications, while still offering moderate to high gain and bandwidth

CIRCUIT 


![image](https://github.com/user-attachments/assets/4de76156-183a-4964-bf60-df50744f8b17)




![image](https://github.com/user-attachments/assets/d70689ff-1b49-48c0-9fb9-9f27bc80ceb0)





LT Spice Simulation Results:<br>
•	OUTPUT



![image](https://github.com/user-attachments/assets/a49c37aa-18ea-4139-91e6-301f557eca51)




**OUTPUT** 

Characteristic	Description<br>
Power Supply	1.8V<br>
Power Consumption	1.2mW<br>
Gain	55.36 dB<br>
ωUGB (Unity Gain Bandwidth)	352 MHz<br>
Output Phase Value	-61.7°<br>
PM (Phase Margin)	118.3°<br>
THD (Total Harmonic Distortion)	0.332%<br>
Slow Rate	261.25 MHz<br>
Total Output Noise Voltage	101.9337 1.1μV<br>
Output Swing Voltage	1.3 V<br>
CMRR (Common-Mode Rejection Ratio)	> 50 dB<br>


**Frequency Response:**




![image](https://github.com/user-attachments/assets/bca9434c-9962-466a-9610-a38727d2838e)





•	The amplifier shows a midband gain of approximately 55dB from 1 kHz to around 10 MHz.
•	Beyond 10 MHz, the gain begins to roll off due to parasitic capacitances and limited transistor bandwidth.
•	This frequency point lies within the transition region between the midband gain and the unity-gain point.
•	The unity-gain bandwidth (ωUGB), where gain reaches 0 dB, is expected further ahead around 352MHz as per the amplifier’s design target.
•	The phase response starts near 180° at low frequencies and decreases steadily with frequency rise.
•	The amplifier maintains a good phase margin to ensure stable operation without oscillation.








**Folded Cascode** 

Circuit Diagram:




![image](https://github.com/user-attachments/assets/0741bd48-317f-4a86-9526-5de279505933)

 

Design Calculations:

Open-Loop Gain (Aₒ):
Target = 120 dB → Aₒ = 10⁶ = gm × ro =72db
- Unity Gain Bandwidth (UGBW):
UGBW = gm / Cc → For gm = 1 mS, Cc = 20 pF → UGBW = 10 MHz
- Slew Rate (SR):
SR = I / Cc → For Cc = 20 pF, SR = 1 V/µs → I = 20 µA
- Power Consumption:
P = VDD × I = 3.4 V × 2.4 mA = 7.92 mW ≈ 8 mW



LT Spice Simulation Results:
•	Input:




![image](https://github.com/user-attachments/assets/39cfd9e4-d79d-433a-ad28-8ac1cedff821)





•	Operation Point Analysis:


![image](https://github.com/user-attachments/assets/a44238da-2b8d-4ea0-a7e6-166025d7ea36)




Frequency Response:
•	The frequency response (Bode plot) of the folded cascode OTA exhibits characteristics similar to that of a single-pole system within the operational bandwidth.
•	The dominant pole is determined by the output resistance and load capacitance at the output node, which typically falls within the low-to-mid MHz range, defining the unity-gain bandwidth of the OTA.
•	The second pole, arising from internal high-impedance nodes (often at the cascode node), occurs at a much higher frequency — generally in the range of several hundred MHz to GHz, making it insignificant for normal OTA operation.
•	If a Miller compensation capacitor (Cc) is introduced in certain folded cascode designs (e.g., for enhanced stability in multistage amplifiers), it introduces a zero at approximately
•	Z1=gmCcZ_1 = \frac{g_{m}}{C_c}Z1=Ccgm 
which typically lies around 1–2 GHz, and hence is also not influential in the OTA's typical frequency range of interest.
Therefore, the Bode plot of the folded cascode OTA remains effectively that of a single-pole system up to a few hundred MHz, beyond which gain drops off and higher-order effects become negligible for practical applications

 
![image](https://github.com/user-attachments/assets/b0798326-b793-4e76-85ac-2da9e2b237c4)



# CONCLUSION

In this work, the design, analysis, and comparison of two widely used analog amplifier topologies—the Telescopic Cascode Differential Amplifier and the Folded Cascode Operational Transconductance Amplifier (OTA)—were presented. Both architectures demonstrate distinct advantages and are chosen based on specific application requirements.
The Telescopic Cascode Amplifier offers superior gain and low power consumption due to its simple, vertically stacked structure. However, its performance is constrained by limited output voltage swing and reduced input common-mode range, making it less ideal for low-voltage applications.
In contrast, the Folded Cascode OTA overcomes these limitations by “folding” the current path, allowing for greater headroom, better output swing, and wider common-mode input range. Although it introduces slightly more complexity and consumes more power, it is better suited for low-voltage and portable analog systems.
Ultimately, the choice between the two topologies depends on the design priorities—gain and simplicity favor the telescopic approach, while output swing and flexibility make the folded cascode a more versatile solution in modern CMOS design.
# REFERENCE
1. Behzad Razavi, “ Design of Analog CMOS Integrated Circuit”, Tata McGraw Hill 2001.
2. Sudhir.M.Mallya, Joseph.H.Nevin, “Design Procedures for a fully differential Folded Cascode CMOS operational Amplifier”, IEEE Journal of Solid-State Circuits, Vol.24, No.6, December 1989,pp 1737-1740. I. S. Jacobs and C. P. Bean, “Fine particles, thin films and exchange anisotropy,” in Magnetism, vol. III, G. T. Rado and H. Suhl, Eds. New York: Academic, 1963, pp. 271–350.
3. Katsufumi Nakamura and L. Richard Carley, “A Current – based positive-feedback technique for efficient cascode bootstrapping”, in 1991 Symposium on VLSI Circuits Digest Technical Papers, May 1991, pp 107-108.
4. K.Nakamura and L.R. Carley, “An enhanced fully differential folded cascode op-amp”, IEEE Journal of Solid-State Circuits, Vol.27,No.4 APR.1992.
4. Vimala, P., Rao, R. D., Gokhale, C. G., & Aneesh, V. S. (2024). Design of Two Stage Miller Compensated CMOS Opamp with Nulling Resistor in 90nm Technology




