# Semi-Domino Full Adder  
Semi-Domino Full adder for 15-4 Compressor using 28nm Technology by using Synopsys Custom Compiler


# Table of Content 
- ABSTRACT 
- INTRODUCTION
- TOOLS USED
- XNOR CIRCUIT DESIGN
- NETLIST
- ACKNOWLEDGEMENT 
- REFERENCE 


## ABSTRACT

 In this paper, I present Semi-Domino full adder for 15-4 compressor used in Digital signal processing application. Semi-Domino logic which is very-faster than 
existing logic and also consumes less power than conventional logics. Objective of this work to inspect the power, power delay and delay product of full adder in 
semi-domino full adder. the performance of the adder circuits and compressors is based on TMSC 28nm CMOS process models at the supply of 1v, 500Mhz frequency evaluated by 
the comparing of simulation results obtained from different software. 

# INTRODUCTION

- In this Semi-Domino Full adder ckt shown in below Fig(A), is consists of two pre-charge transistor (M1, M8), evaluation network for carry and sum (PDB carry, PDN sum), 
two keeper transistors (M2, M9), six footer Transistors (M3, M4, M5, M10, M11, M12) and two semi-domino inverters. Through the pre-charge phase when the CLK is low, the 
pre-charge Pmos transistor become ON and the dynamic node is connected to the VDD and obtains Pre-charge from VDD. When clock goes high, the evaluation phase starts and the 
output gets evaluated with the pull-down network and conditionally gets discharged if any one of the inputs stays at logic 1.
At the evaluation stage when all the inputs are at logic 0, the dynamic node became logic 1. But more fan-in Nmos pull-down leaks the charge stored in the capacitance at the 
dynamic node due to the sub-threshold leakage. This charge is compensated by the Pmos keeper, which we want to recapitulate the voltage of the dynamic node. At a time e 
when, noise voltage impulse come at gate input, the keeper may not be able to restore the voltage level of the dynamic node. To stop that the footers M3, M4 and M5 and the M10, 
M11 and M12 are connected to the carry and sum part. M3 and M10 operate as stack transistors. At the evaluation phase when PDN of sum and carry are at logic 1, at that time M3 and M10 stops the free discharge of dynamic node voltage to evaluate logic 0 at the dynamic node of carry and sum simultaneously. To compensate that M5 and M12 make a charge discharge path for the carry path and the sum path simultaneously.
The Output node pulse N-Dyn always propagated by turning ‘ON’ the Nmos transistor for the buffer by the pre-charge pulse in dynamic node. We have connected the 
source of the buffer’s Nmos transistor M7 and M14 to the drain of the Nmos clock transistor M7 and M14 to the drain of the Nmos clock transistor (N_FOOT) instead of GND, which 
operates in semi-domino logic.


# TOOL USED

- Synopsys Custom Compiler: The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

- Synopsys Primewave: PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

- Synopsys 28nm PDK: The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Semi_Domino_full_adder Circuit Design

Semi-domino Full Adder is shown in fig. 

![image](https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/ckt.png)

- SCHEMATIC

![image](https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/schematic.png)

                                                                                                                                                                                                                                                                                                                                                                            
- SYMBOL

![image](https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/full_adder_symbol.png)                                                                                                                                                                                                                                                                                                                                                                               

- TESTBENCH SYMBOL

![image](https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/TB.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
- PRIMEWAVE WINDOW

![image](https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/testsuite.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                        
- TESTBENCH WAVEFORM

![image](https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/waveview.png)                                            

# NETLIST
The netlist of the above circuit has also been uploaded to the github repo with the file name -https://github.com/Govindarathod/Semi_Domino_full_adder/blob/main/Report_images/netlist_semi_domino.txt  

# AUTHOR
Govinda M Rathod, MTech VLSI and Embedded Systems , Defence Institute of Advanced Technology, Pune, Maharashtra

# ACKNOWLEDGEMENT 

- Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
- Synopsys, India
- VLSI System Design(VSD) Corporation Private Limited India
- Indian Institute of Technology, Hyderabad 
- Cloud Based Analog IC Design Hackathon
- Sameer Durgoji, NIT Karnataka
- Chinmay panda, IIT Hyderabad

# REFERENCES

- Meher, P.; Mahapatra, K.K., "Low power noise tolerant domino 1-bit full adder," Advances in Energy Conversion Technologies (ICAECT), 2014 International Conference on , vol., no., pp.125,129, 23-25 Jan. 2014.
- Marimuthu, R.; PradeepKumar, M.; Bansal, D.; Balamurugan, S.; Mallick, P.S., "Design of high speed and low power 15-4 compressor," Communications and Signal Processing (ICCSP), 2013 International Conference on , vol., no., pp.533,536, 3-5 April 2013.
- R. Zimmermann, W. Fichtner, “Low-power logic styles: CMOS versus pass transistor logic”, IEEE Journal of SolidState Circuits, Vol. 32, pp. 1079–1090, July 1997.
- J. M. Rabaey, A. Chandrakasan, B. Nikolic, “Digital Integrated Circuits- A Design Perspective”, 2nd Prentice Hall, Englewood Cliffs, NJ, 2002.
