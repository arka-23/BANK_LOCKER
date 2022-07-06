# BANK_LOCKER
This repository contains the proposed design and simulated results for a simple logic (sequential and combinational) circuit based Digital Lock design with three buttons 1,2 and R.



# Table of Contents
   * [Abstract](#abstract)
  * [Block diagram for the proposed model of the digital lock](#block-diagram-for-the-proposed-model-of-the-digital-lock)
  * [Equipment Required](#equipment-required)  
- [Building blocks of the circuit](#building-blocks-of-the-circuit)
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
 - [Proposed alternate approach](#proposed-alternate-approach)
 - [Contributors](#contributors)
 - [Acknowledgement](#acknowledgement)
 - [References](#references)


## Abstract

In order to enter a code, the numerical buttons are to be pressed and the push button ‘R’ is used to reset the system. 
To unlock, a user must first push the reset button ‘R’ and then enter a three-digit code. 
'R' button is to be used to start over again in case of any mistake in entering the code. 
To indicate success (i.e. match with the locker code and successful unlocking) the circuit should produce an output of ‘O’ after the correct code has been entered.

We present the ideas, schematic diagram and simulation results for the locker code of 1-2-1.

Objective: The lock design should be simple, efficient, fast and cost effective. 


## Block diagram for the proposed model of the digital lock:

![AkanshaMukherjee_001910701094 pptx (10)](https://user-images.githubusercontent.com/66127211/177494027-f5a4f163-99ed-4bb5-906f-33325bff9a71.jpg)

## Equipment required for hardware implementation:
* Breadboard
* Switches (transistor based or otherwise) for inputs
* 2:1 Encoder with enable input
* 3 bit serial in parallel out register (may be designed using 3 D flip-flops as well)
* 3 bit comparator (may be designed using logic gates as well)
* Basic logic gates: AND, OR, XOR, XNOR gates
* D flip-flops (3 for synchronous mod 3 counter) with clear input
* Programmable 7 segment display
* Connecting wires
* Voltage supply
* Ground terminal

# Building blocks of the circuit

Each block of the circuit and its function is discussed below:

## Inputs
![AkanshaMukherjee_001910701094 pptx](https://user-images.githubusercontent.com/66127211/177490045-3ec7cba3-3504-4c8f-9f6f-f8e212ff4478.jpg)

## The Valid Input Detector
![AkanshaMukherjee_001910701094 pptx (1)](https://user-images.githubusercontent.com/66127211/177490187-875c26bf-8ec5-4e4f-b3c6-241393147d64.jpg)

## The Encoder Circuit
![AkanshaMukherjee_001910701094 pptx (2)](https://user-images.githubusercontent.com/66127211/177490457-879ac34b-6bae-4008-82b8-43ba83068514.jpg)


## The Counter Circuit
![AkanshaMukherjee_001910701094 pptx (3)](https://user-images.githubusercontent.com/66127211/177490526-1dc6f386-6b2a-479e-9d12-0d1ad0dc3d52.jpg)


## The Three Bit SIPO Register With Counter Acknowledge
![AkanshaMukherjee_001910701094 pptx (4)](https://user-images.githubusercontent.com/66127211/177490819-1a830042-4f05-4f22-ba83-bcfbce55a476.jpg)


## The Comparator Circuit
![AkanshaMukherjee_001910701094 pptx (5)](https://user-images.githubusercontent.com/66127211/177490942-7a29e84f-bd44-44da-b0c9-d90022ad9e0c.jpg)


## The Seven Segment Display
![AkanshaMukherjee_001910701094 pptx](https://user-images.githubusercontent.com/66127211/177491225-ec98351b-fada-4b72-b63c-ac830be26218.jpg)


# Examples to illustrate the working of the circuit

A few sample user inputs are discussed and the signal flow is examined in each case.
![AkanshaMukherjee_001910701094 pptx (3)](https://user-images.githubusercontent.com/66127211/177491476-665c9df6-c43d-4560-bc23-47136ef3e6da.jpg)

![AkanshaMukherjee_001910701094 pptx (2)](https://user-images.githubusercontent.com/66127211/177491532-1203bf2f-d64b-4fe9-b550-923277c89289.jpg)

![AkanshaMukherjee_001910701094 pptx (1)](https://user-images.githubusercontent.com/66127211/177491571-511d94df-ce94-494d-bea4-2a942c1ea07f.jpg)





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

# Proposed alternate approach:
An alternate sequential circuit based approach has been proposed and discussed below. Simulation results have not been included.

![AkanshaMukherjee_001910701094 pptx (1)](https://user-images.githubusercontent.com/66127211/177493152-930e3d5a-ea01-45a4-93c8-11d42d0fb540.jpg)

![AkanshaMukherjee_001910701094 pptx](https://user-images.githubusercontent.com/66127211/177493172-72b89a4f-5283-494a-8b1b-b00a659e7ea9.jpg)

![AkanshaMukherjee_001910701094 pptx (2)](https://user-images.githubusercontent.com/66127211/177493299-2d4f1dc5-4ad8-40a1-831c-52ec4959664f.jpg)

![AkanshaMukherjee_001910701094 pptx (3)](https://user-images.githubusercontent.com/66127211/177493355-91f5494d-c9b6-4329-be0b-1b6a2fbdd71b.jpg)

![AkanshaMukherjee_001910701094 pptx (4)](https://user-images.githubusercontent.com/66127211/177493469-083a6f32-854b-4622-9cb3-8054ce3122b3.jpg)

![AkanshaMukherjee_001910701094 pptx (5)](https://user-images.githubusercontent.com/66127211/177493508-eb0b39a4-4bf0-479c-be2e-9e573d358855.jpg)

![AkanshaMukherjee_001910701094 pptx (6)](https://user-images.githubusercontent.com/66127211/177493593-818f95d5-db05-4031-9d62-1720b2490842.jpg)

![AkanshaMukherjee_001910701094 pptx (7)](https://user-images.githubusercontent.com/66127211/177493641-70bbaf91-e9b8-4471-a2f6-ffc7f4a95c2f.jpg)

![AkanshaMukherjee_001910701094 pptx (8)](https://user-images.githubusercontent.com/66127211/177493717-a5876c0c-e45b-41d8-9f43-38a5ddfabd99.jpg)

![AkanshaMukherjee_001910701094 pptx (9)](https://user-images.githubusercontent.com/66127211/177493774-33eb85bd-8328-4ee1-9a7f-e2d91da062d4.jpg)




# Contributors:
1. Akansha Mukherjee - mukherjeeakansha07@gmail.com
2. Arka Chakraborty - arkachakraborty16@gmail.com

# Acknowledgement
1. Prof. Subir Kumar Sarkar, department of Electronics and Telecommunication, Jadavpur University, Kolkata

# References
[1] Digital Logic And Computer Design By M. Morris Mano.



