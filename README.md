# Samsung RISC-V Program  

**RISC-V Talent Development Program**, powered by **Samsung Semiconductor India Research (SSIR)** in collaboration with **VLSI System Design (VSD)**.  

## Basic Details  
- **Name**: Karan R  
- **College**: Vidyavardhaka College of Engineering  
- **Email**: karanrajashekar07@gmail.com  

## Task 1: RISC-V Toolchain Installation 
- Installation of RISC-V toolchain using the VDI link provided.
- The program demonstrates basic operations in C and their equivalent implementation in RISC-V assembly language.  
<details>
<summary> <b>Task 1:</b></summary>
<br>
1.Compilation and execution of a C program (sum1ton.c) that calculates the sum of numbers from 1 to 15.
  
![image](https://github.com/user-attachments/assets/92581395-3c0d-4253-84b3-d23bfcf6ffe5)
  
2.Leafpad editor displaying the source code of the sum1ton.c program, implementing the logic to calculate the sum of integers from 1 to 15.
![image](https://github.com/user-attachments/assets/71f9f5e8-56af-4034-b858-d67c87dab718)

3.Terminal window displaying disassembled output, including the assembly instructions of the compiled C program
![image](https://github.com/user-attachments/assets/0926616e-90bf-466b-8b4e-4a43febf0452)

4.RISC-V  -O1 and -Ofast

![image](https://github.com/user-attachments/assets/b8e75b6f-855f-4402-8d46-62c50067b565)

</details>

---------------------------------------------------------

## Task 2: RISC-V Object dump for both -O1 and -Ofast

- Compilation and Optimization: A C program is compiled using the RISC-V GCC compiler with the -O1 and -Ofast optimization flag to observe its performance and efficiency.

- Simulation with SPIKE: The compiled binary is executed in the SPIKE RISC-V simulator.

- Object Dump Analysis: The RISC-V object dump of the program is generated, showing the disassembled assembly instructions and memory addresses.

<details>
<summary> <b>Task 2:</b></summary>
<br>
1.simple c program of swap of numbers using RISC-V GCC

![C(swap_of_no )](https://github.com/user-attachments/assets/cce56ffb-6319-4548-aa8a-86171708f784)

2.object dump file for -O1 

![swap_O1_1](https://github.com/user-attachments/assets/32042ae2-75b9-4a09-8a0e-5617018200b4)
![swap_O1_2](https://github.com/user-attachments/assets/b4859cc3-a0c4-4e5f-b1b0-8e5413967272)

3.object dump file for -Ofast

![swap_Ofast_1](https://github.com/user-attachments/assets/a84db581-02bc-450d-9c7d-3333829915f6)
![swap_Ofast_2](https://github.com/user-attachments/assets/17cc8da5-ad19-4a42-b8df-5a53b0da8c04)

</details>

----------------------------------------------

## Task 3: 32-bit Instruction Patterns



## Instruction Types
The RISC-V architecture categorizes instructions into six types based on their format:
- **R-type**: Register to Register operations
- **I-type**: Immediate operations
- **S-type**: Store operations
- **B-type**: Branch operations
- **U-type**: Upper immediate operations
- **J-type**: Jump operations


<details>
<summary> <b>Task 3:</b></summary>
<br>
## Identified RISC-V Instructions
From the `riscv-objdump` output of the application code, the following 15 unique RISC-V instructions were identified along with their 32-bit formats:

| Instruction        | 32-bit Code         | Type  |
|--------------------|---------------------|-------|
| `add x3, x4, x5`  | `0000000 00101 00100 000 00011 0110011` | R-type |
| `sub x3, x4, x5`  | `0100000 00101 00100 000 00011 0110011` | R-type |
| `and x3, x4, x5`  | `0000000 00101 00100 111 00011 0110011` | R-type |
| `or x3, x4, x5`   | `0000000 00101 00100 110 00011 0110011` | R-type |
| `xor x3, x4, x5`  | `0000000 00101 00100 100 00011 0110011` | R-type |
| `sll x3, x4, x5`  | `0000000 00101 00100 001 00011 0110011` | R-type |
| `srl x3, x4, x5`  | `0000000 00101 00100 101 00011 0110011` | R-type |
| `addi x3, x4, 10` | `000000000010 00100 000 00011 0010011` | I-type |
| `andi x3, x4, 10` | `000000000010 00100 111 00011 0010011` | I-type |
| `ori x3, x4, 10`  | `000000000010 00100 110 00011 0010011` | I-type |
| `sb x3, 4(x5)`    | `0000000 00011 00101 000 00100 0100011` | S-type |
| `sh x3, 4(x5)`    | `0000000 00011 00101 001 00100 0100011` | S-type |
| `beq x3, x4, label` | `0000000 00011 00100 000 00001 1100011` | B-type |
| `lui x3, 0x2000`  | `00100000 00000 00000 101 00011 0110111` | U-type |
| `jal x3, label`   | `00000000 00000 00000 101 00011 1101111` | J-type |


</details>

-------------------------------------------------------

## Task 4: Functional Simulation of RISC-V Core 
- This project involves simulating the RISC-V core using a Verilog netlist and testbench to validate its functional correctness. 
- Waveform snapshots and simulation results are analyzed and documented, with all outcomes.


<details>
<summary> <b>Task 4:</b></summary>
<br>
Analysing the Output Waveform 

**```Instruction 1: ADD R6, R2, R1```**  
![ADD](https://github.com/user-attachments/assets/4e1a72ff-5bdb-4f80-93d5-8d331e26c6cb)

**```Instruction 2: SUB R7, R1, R2```**  
![SUB](https://github.com/user-attachments/assets/919071ea-fa28-46de-92c0-f7e68bef40e0)

**```Instruction 3: AND R8, R1, R3```**
![AND](https://github.com/user-attachments/assets/f9b9195b-99ef-4f78-a0d9-51058dd98feb)

**```Instruction 4: OR R9, R2, R5```**  
![OR](https://github.com/user-attachments/assets/5cd81d5f-5778-44c5-9a86-ed8c11003850)

**```Instruction 5: XOR R10, R1, R4```**  
![XOR](https://github.com/user-attachments/assets/d72dcf44-ea01-4e90-9eb0-575f32a445da)

**```Instruction 6: SLT R1, R2, R4```** 
![SLT](https://github.com/user-attachments/assets/609ec06e-4481-4673-855c-2ac0b362a0c1)

**```Instruction 7: ADDI R12, R4, 5```**  
![ADDI](https://github.com/user-attachments/assets/ea0aa791-26f6-495a-8085-08b6a2fd2577)

**```Instruction 8: BEQ R0, R0, 15```**  
  ![BEQ](https://github.com/user-attachments/assets/10cd28dc-be9c-457d-b615-6c085765fc65)
 
**```Instruction 9: BNE R0, R1, 20```**
![BNE](https://github.com/user-attachments/assets/0eab30b1-fc2a-46ad-8192-e2b3cb91553b)
 
**```Instruction 10: SLL R15, R1, R2```**  
![SLL](https://github.com/user-attachments/assets/5de75b7e-60f4-4d60-83a1-86e86c46a3a3)

</details>

------------------------------------------
## Task 5: Ultrasonic Blind Spot Detection:
The Ultrasonic Blind Spot Detection project is designed to enhance vehicle safety by detecting obstacles in the driver's blind spot. Using an ultrasonic sensor integrated with a RISC-V board, the system continuously monitors the area adjacent to the vehicle. When an obstacle is detected within a pre-defined range, the system promptly activates visual (LED) and/or audio (buzzer) alerts, thereby improving situational awareness and reducing the risk of collisions.

<details>
<summary> <b>Task 5:</b></summary>
<br>
 Ultrasonic Blind Spot Detection

## Overview
The Ultrasonic Blind Spot Detection project leverages ultrasonic sensor technology integrated with a RISC-V board to detect obstacles in a vehicle’s blind spot. By continuously monitoring the area with ultrasonic waves, the system alerts the driver through visual (LED) or audio (buzzer) signals when an obstacle is detected, thereby enhancing driving safety and reducing the risk of collisions.

## Components Required
- **RISC-V Board:** Acts as the central processing unit for sensor data and alert control.
- **Ultrasonic Sensor:** (e.g., HC-SR04) for measuring distance.
- **Buzzer/LED:** Provides audio or visual alerts upon obstacle detection.
- **Power Supply:** Suitable voltage supply for the RISC-V board and peripherals.
- **Breadboard:** For assembling the circuit.
- **Jumper Wires:** For making the necessary connections.

## Circuit Connection for Ultrasonic Blind Spot Detection
Below is a table outlining the wiring connections between the RISC-V board and the components used in this project:

| Component                 | RISC-V Board Pin | Description                                   |
|---------------------------|------------------|-----------------------------------------------|
| **Ultrasonic Sensor VCC** | VIN              | Connects to the power supply (e.g., 5V)       |
| **Ultrasonic Sensor Trigger** | PD3          | Digital output pin to send the trigger signal |
| **Ultrasonic Sensor Echo**    | PD2          | Digital input pin to receive the echo signal  |
| **Buzzer/LED VCC**        | VIN              | Connects to the power supply (e.g., 5V)       |
| **Buzzer/LED Control**    | PC7             | Digital output pin to activate the buzzer/LED |
| **GND (All Components)**  | GND              | Common ground for all components              |

How It Works
1. **Ultrasonic Sensing:**  
   The ultrasonic sensor emits high-frequency sound waves that reflect off objects. By measuring the time taken for the echo to return, the sensor calculates the distance to an obstacle.

2. **Detection and Alert:**  
   The RISC-V board continuously processes the distance measurements. When an object is detected within a predefined threshold in the blind spot, it activates the buzzer or LED to alert the driver.

3. **Enhanced Safety:**  
   This system provides drivers with immediate feedback about obstacles in their blind spot, thereby improving overall vehicle safety and reducing potential collision risks.
   

**```Pinout Diagram :```**  
![image](https://github.com/user-attachments/assets/0d5da3d6-fffd-4a65-82bc-1a6764b08a2f)


</details>

------------------------------------------






