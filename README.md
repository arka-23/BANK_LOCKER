# BANK_LOCKER
This repository contains a Digital Lock design for a logic circuit(combinational and sequential) based digital bank locker opener with three buttons,1,2 and R.
In order to enter a code, the numerical buttons are to be pressed and the push button ‘R’ is used for reset
purpose. For opening the locks a user should first push the reset button ‘R’ and then enter a code of three
digits. R button is to be used to start over again in case of any mistake in entering the code. To open the
locker your circuit should produce an output of ‘O’ after the correct code has been entered and draw the
schematic circuit diagram of the locker for the code 1-2-1.



# Table of Contents
   * [Abstract](#abstract)
  * [Block diagram for the proposed model of the digital lock](#block-diagram-for-the-proposed-model-of-the-digital-lock)
  * [Equipment Required](#equipment-required)  
- [Working of the circuit](#working-of-the-circuit)
  * [Inputs](#inputs)
  * [The Valid Input Detector](#the-valid-input-detector)
  * [The Encoder Circuit](#the-encoder-circuit)
  * [The Counter Circuit](#the-counter-circuit)  
  * [The Three Bit SIPO Register With Counter Acknowledge](#the-three-bit-sipo-register-with-counter-acknowledge)
  * [The Comparator Circuit](#the-comparator-circuit)
  * [The Seven Segment Display](#the-seven-segment-display)
  
 - [Examples to illustrate the working of the circuit](#examples-to-illustrate-the-working-of-the-circuit)
 - [Multisim Implementation](#multisim-implementation)
 - [Verilog Implementation](#verilog-implementation)
 - [Precautions in circuit design](#precautions-in-circuit-design)
 - [Contributors](#contributors)
 - [Acknowledgement](#acknowledgement)
 - [References](#references)


## Abstract

This repository contains a Digital Lock design for a logic circuit(combinational and sequential) based digital bank locker opener with three buttons,1,2 and R.
In order to enter a code, the numerical buttons are to be pressed and the push button ‘R’ is used for reset
purpose. For opening the locks a user should first push the reset button ‘R’ and then enter a code of three
digits. R button is to be used to start over again in case of any mistake in entering the code. To open the
locker your circuit should produce an output of ‘O’ after the correct code has been entered and draw the
schematic circuit diagram of the locker for the code 1-2-1.

OBJECTIVE: THE LOCK MUST BE SO DESIGNED THAT HARDWARE REQUIREMENT AND COST ARE
MINIMIZED AND SPEED OF OPERATION IS ENHANCED.


## Block diagram for the proposed model of the digital lock:

![image](https://user-images.githubusercontent.com/70422874/177373592-96b0f1eb-12d8-488a-abfe-ac7d7bfdbd3c.png)


## Equipment required
Breadboard

Switches (transistor based or otherwise) for inputs

2:1 Encoder with enable input

3 bit serial in parallel out register (may be designed using 3
D flip-flops as well)

3 bit comparator (may be designed using logic gates as well)

Basic logic gates: AND, OR,
XOR, XNOR gates

D flip-flops (3 for synchronous mod 3 counter) with clear input

Programmable 7 segment display

Connecting wires

Voltage supply

Ground terminal

# Working of the circuit

WE EXPLORE IN DETAIL THE WORKING OF EACH BLOCK OF THE CIRCUIT

## Inputs
![image](https://user-images.githubusercontent.com/70422874/177374833-6a86e9b9-06e1-4fa1-8e52-a6428e54a9c3.png)

## The Valid Input Detector
![image](https://user-images.githubusercontent.com/70422874/177375133-842d866c-59b0-4e67-ac34-2db929fdf5bc.png)


## The Encoder Circuit
![image](https://user-images.githubusercontent.com/70422874/177375337-16af2ac2-06fc-438f-bea0-26252540e6dd.png)


## The Counter Circuit
![image](https://user-images.githubusercontent.com/70422874/177375420-9ad7d043-cce6-42cf-a6eb-68bd28826a62.png)


## The Three Bit SIPO Register With Counter Acknowledge
![image](https://user-images.githubusercontent.com/70422874/177375621-a654115f-cbdc-4a7c-b022-298f496e21a0.png)


## The Comparator Circuit
![image](https://user-images.githubusercontent.com/70422874/177375805-a068e5c4-eece-45b8-98e2-2d215a8bcdd3.png)


## The Seven Segment Display
![image](https://user-images.githubusercontent.com/70422874/177375993-5e50e46a-2f19-46a2-8dd7-55dcfc2aca2e.png)


# Examples to illustrate the working of the circuit

A few sample user inputs are discussed and the signal flow is examined in each case.

![image](https://user-images.githubusercontent.com/70422874/177377360-9f610679-9f3e-46f4-8ab9-4ee0035ed335.png)

![image](https://user-images.githubusercontent.com/70422874/177377394-93b478b2-c203-47c4-9f47-1e8f8a328640.png)

![image](https://user-images.githubusercontent.com/70422874/177377455-1cc4e5e8-86b6-4542-ae64-aeb5b3d92661.png)


# Multisim Implementation

Multisim Circuit

![image](https://user-images.githubusercontent.com/70422874/177455847-5807e9d8-2386-46c3-82b2-c29ee50ed69a.png)

Input : 1-2-1 [Matches Key Code - Output Glows]

![image](https://user-images.githubusercontent.com/70422874/177456054-80a648eb-812d-42e7-9242-109c2f0d6ca5.png)

Input : 1-2-2 [Doesnot match Key Code - No Glow]

![image](https://user-images.githubusercontent.com/70422874/177456170-8e72be82-8418-4b14-bf8c-8f0fd02f4c03.png)

Input : 1-2-R

![image](https://user-images.githubusercontent.com/70422874/177456481-fd8f4e9f-fae6-46f0-9a43-3f92a779facd.png)



# Verilog Implementation

Verilog Code: For input sequence - 1 2 1

![image](https://user-images.githubusercontent.com/70422874/177451271-d764ad68-54f7-436d-ac1b-5cb289115dfd.png)

![image](https://user-images.githubusercontent.com/70422874/177451329-7f34a398-6890-4210-865e-5a7a3321b928.png)

![image](https://user-images.githubusercontent.com/70422874/177451512-5c686304-cc3a-4fb8-8460-8e34db42167e.png)


Testbench:

![image](https://user-images.githubusercontent.com/70422874/177384405-2edc6433-8922-4d33-ad64-d6f7a69254b9.png)

Output:

![image](https://user-images.githubusercontent.com/70422874/177452458-9295ec87-9fe7-4b5e-ae7f-2a82bf636cbc.png)


Verilog Code: For input sequence - 1 2 2

Testbench:

![image](https://user-images.githubusercontent.com/70422874/177452127-c8bcbdf6-08e1-4167-8eac-1dada5e5eef7.png)

Output:

![image](https://user-images.githubusercontent.com/70422874/177452055-e97efd45-bb94-4bd7-97e0-5d712f6fe9d2.png)




# Precautions in circuit design
1. The components used in the circuit must be resistant to physical changes in temperature, humidity, etc.
2. We must ensure the circuit requirements for current and voltage are met, at the same time, the power rating of the components are not exceeded.
3. The devices must be as close to ideal operation, for better results.
4. Connections must be made properly and the wires must be designed to withstand


# Contributors:
1. Akansha Mukherjee - Mukherjeeakansha07@gmail.com
2. Arka Chakraborty - arkachakraborty16@gmail.com

# Acknowledgement
1. 

3. 

# References
[1] Balraj Singh, Mukesh Kumar, and J. S. Ubhi, “Analysis of CMOS based
NAND and NOR Gates at 45mm Technology”, IJEECS, ISSN 2348-
117X, Volume 6, Issue 4, April 2017.
[2] Sudhakar Alluri1, Uma Umaheshwar, B. Rajendra Naik and
N.S.S.Reddy, “Design and Performance Analysis of VLSI Circuits in
180nm Technology”, IJCRT, ISSN: 2320-2882, Volume 6, Issue 2 April
2018



