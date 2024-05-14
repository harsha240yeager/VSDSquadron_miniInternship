#  VSDSquadron Reseacrh Internship 2024

The program is designed around the RISC-V architecture, utilizing open-source tools to provide comprehensive education on VLSI chip design and the RISC-V instruction set architecture. Participants will gain hands-on experience and theoretical knowledge under the expert guidance of Mr. Kunal Ghosh..

## Contact info

**Name:** Narra Harshavardhan Reddy                                                                        
  **College:** JNTUH College of Engineering Hyderabad  
**Email ID:** harshavardhan240.work@gmail.com  
**GitHub Profile:** [harsha-github](https://github.com/harsha240yeager)           
 **Linkedin Profile:** [harsha-linkedin](https://www.linkedin.com/in/harsha240)

----------------------------------------------------------------------------------------------------------------

<details>
<summary><b>**Task 1:** The objective is to install all essential tools required for the internship, including Ubuntu on VMBox, the GNU Toolchain, GTKWave, Yosys, and the iVerilog simulator.</summary>   
<br>

# TASK 1

1.Download Oracle Virtual machine and allocated 4GB RAM,100GB HDD

2.Installation of Ubuntu 22.04 using Virtual Machine

3.Installation of RISC-V GNU Toolchain

4.Installation of Yosys

5.Installation of iverilog

6.Installation of gtkwave

1.Installation of Ubuntu 22.04 using Virtual Machine
![ubuntu](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/1a138e13-08ee-4cf8-a065-c602d614e0ad)

2.Installation of RISC-V GNU Toolchain

```
$ sudo apt-get install autoconf automake autotools-dev curl python3 python3-pip libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev ninja-build git cmake libglib2.0-dev libslirp-dev
$ git clone https://github.com/riscv/riscv-gnu-toolchain
$ ./configure --prefix=/opt/riscv make linux
```

![gnu2](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/c14b6ee5-518e-4a20-8740-fb9a19262075)
![riscv-gnu-toolkit](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/39ceff7a-b014-40bf-8900-6577f3cfc3fa)

3.Installation of Yosys
```
$ git clone https://github.com/YosysHQ/yosys.git

$ sudo apt install make

$ cd yosys

$ sudo apt-get install build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc

$ make

$ sudo make install

$ Yosys
```
![yosys](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/ba317979-8c27-4c37-9a07-38627512c916)

4.Installation of iverilog
```
$ sudo apt-get install iverilog 
```

![iverilog](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/82746fbc-16d6-4d66-a0d6-771630cb0018)

5.Installation of gtkwave
```
$ sudo apt update

$ sudo apt install gtkwave
```

![gtkwave](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/c00d0487-dfec-4f31-be8b-0cf29c2f9e57)

</details>

--------------------------------------------------------------------

<details>
<summary><b>Task 2:</b> The objective is to discern the instruction type of each provided instruction and to present its precise 32-bit instruction code in the designated format for the respective instruction type.</summary>

## TASK 2 

Identify instruction type and exact 32-bit instruction code in the instruction type format.
Below are instruction that are to be tested and simulated:-

![TEST_CASES](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/e540fb6b-f426-4d80-9857-c9820e160110)


### Riscv Introduction 

![riscv](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/b46ae3c4-bd84-4e16-af3f-e502d10f49f3)

In the world of computers, there's a new kid on the block called RISC-V. It's not like the other closed systems you might have heard of, like x86 or ARM. RISC-V is special because it's open to everyone. That means anyone can look at it, change it, or use it without having to pay money or follow strict rules.Risc-V follows a simple and modular approach called RISC, which stands for Reduced Instruction Set Computing. This just means it focuses on doing things in a straightforward way, without unnecessary complications. RISC-V has basic instructions for doing common tasks, like adding numbers together. But it also has extra options you can add if you need them, like handling decimals or doing advanced math.One cool thing about RISC-V is that it can be used in lots of different situations. Whether you're making a tiny computer for a smartwatch or a super-fast machine for scientific research, RISC-V can adapt to fit your needs.Another great thing about RISC-V is that it's open. That means companies and people can work together to make it better without worrying about getting locked into one company's way of doing things. This collaboration has led to lots of tools and gadgets being created that work with RISC-V.

#### RISCV Instruction set :

**RISC-V Instruction Format**  
1.Opcode (op): This field specifies the operation to be performed by the instruction. It determines the type of instruction, such as arithmetic, load/store, branch, or control transfer.
Destination Register (rd): This field identifies the register where the result of the operation will be stored. For instructions that don't produce a result (like branches or jumps), this field may be unused.

2.Source Register 1 (rs1): This field specifies the first source operand for the instruction. It typically contains data to e operated on, fetched from a register.

3.Source Register 2 (rs2): This field holds the second source operand for instructions that require two inputs. Like rs1, the data here comes from a register.

4.Immediate (imm): For instructions that involve immediate values (constants), this field holds the immediate value directly encoded within the instruction itself. The immediate value could represent a constant to be added, a memory offset, or a shift amount, among other possibilities.

5.Function Code (funct): In some instruction formats, particularly for extended instruction sets, this field may specify additional functionality or variant of the operation specified by the opcode.

6.Memory Address (addr): For load and store instructions, this field holds the memory address to be accessed. It's often calculated by adding an offset to a base address stored in a register.
The specific size and arrangement of these fields can vary depending on the instruction type and the RISC-V variant (e.g., RV32I, RV64I). Additionally, RISC-V supports a variety of instruction formats, including R-type (register-register), I-type (immediate), S-type (store), B-type (branch), U-type (upper immediate) and J-type(jump) each tailored for different types of operations and addressing modes.  

<img width="707" alt="1 " src="https://github.com/KeerthiPatil/VSDSQUADRON_MINI_INTERNSHIP/assets/167600409/66243587-505c-4fde-ada5-5c1d99089f9c">  

**1.R-Format :** instructions using 3 register inputs

  -add,xor,mul    -arithmetic/logical operations


**2.I-Format :** instructions with immediates, loads

  - addi, lw, jalr, slli


**3.S-Format :**  store instructionss

  -sw, sb


**4.B-Format :** branch instructions

  -beq, bge


**5.U-Format :** instructions with upper immediates

  -lui, auipc     —upper immediate is 20-bits


**6.J-Format :** jump instructions

  -jal


![Instruction_formats](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/307dab17-2a41-4cce-a866-78a2cd60461d)

**All RISC32 R-format Instructions**
![r_format_inst](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/90832efa-a6b7-4c7c-b7f0-38102a53b4fe)


**All RISC32 I-format Instructions**
![I_format_inst](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/4c9eb893-424a-47df-87cc-d28f57934772)


**All RISC32 S-format Instructions**
![S_format_inst](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/70b0d9be-2f7a-4222-aa1c-84667875ecf4)


**All RISC32 B-format Instructions**
![B_format_inst](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/61ccd2dc-20b1-4323-9aa5-6ebe820c6f72)



##### Solved Instructions

**1.add r6,r2,r1 :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .

   Decoding in binary format we get : r1=00001,r2=00010,r6=00110. 
   
   ![p1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/55f25feb-d181-42d5-b9a7-ff3ec73be434)

    
**2.sub r7,r1,r2 :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For sub func3=000.The sum is stored in destination register r7 and r2,r1 are source registers .
   
   Decoding in binary format we get : r1=00001,r2=00010,r7=00111.
   
   ![p2](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/8e0dbd0d-c832-4532-b547-14c2f1ffe68c)

**3.and r8,r1,r3 :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For and func3=000.The sum is stored in destination register r8 and r1,r3 are source registers .
   
   Decoding in binary format we get : r1=00001,r3=00011,r8=01000.
   
   ![p3](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/0a7770b9-0f84-4bc7-8142-bc5f7787dae3)

**4.or r9,r2,r5 :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For or func3=110.The sum is stored in destination register r9 and r2,r5 are source registers .
   
   Decoding in binary format we get : r5=00101,r2=00010,r9=01001.
   
   ![p4](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/cb436340-0ef8-4296-a9a7-be765cf1263b)


**5.xor r10,r1,r4 :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For xor func3=100.The sum is stored in destination register r9 and r1,r4 are source registers .
   
   Decoding in binary format we get : r1=00001,r4=00100,r9=01001.

   ![p5](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/9ee91326-dcbc-4c09-94b6-f3a2485a985e)

**6.slt r11,r2,r4 :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For slt func3=010.The sum is stored in destination register r11 and r4,r2 are source registers .
   
   Decoding in binary format we get : r4=00100,r2=00010,r11=01011.

   ![p6](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/2b3c9c77-bdd0-460c-a2cd-83465268cae2)

**7.addi r12,r5.5 :-**
   Instruction type: I Type
   
   In I type instructions opcode=0010011 . For addi func3=000.
   
   Decoding in binary format we get :r5=00101,r12=01100,5=12'b000000000101

   ![p7](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/c042a473-a86f-455e-a42c-0e9f82c320e0)

**8.sw r3,r1,2 :-**
   Instruction type: S Type
   
   In S type instructions opcode=0100011 . For sw func3=010.
   
   Decoding in binary format we get : r3=00011,r1=00001,2=7'b0000000|5'b00010.

   ![p8](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/a668ec03-03f5-4110-884b-027d8c825205)

**9.lw r13,r1,2 :-**
   Instruction type: I Type
   
   In I type instructions opcode=0000011 . For lw func3=010.
   
   Decoding in binary format we get : r13=01101,r2=00001,2=12'b000000000010.

   ![p9](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/ee56096d-3bec-4d6f-9e9e-12374ad3927d)
   

**10.beg r0,r0,15 :-**
   Instruction type: B Type
   
   In B type instructions involves conditional jumps based on certain conditions beign met.
   
   
  ![p10](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/2bef1ca7-52dc-4bbf-bfd2-f3b3c6796722)

**11.bne r0,r1,20 :-**
   Instruction type: B Type
   
   In B type instructions involves conditional jumps based on certain conditions beign met.

   ![p11](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/e8e74cce-743e-4cf1-82de-08a76dae89dc)

**12.sll r15,r1,r2(2) :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For sll func3=001.The sum is stored in destination register r15 and r1,r2(2) are source registers .
   
   Decoding in binary format we get : r1=00001,r2(2)=01000,r15=01111.

   ![r12](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/eb285310-7ec9-4ad2-929f-bcc09e10cce6)

**13.srl r16,r14,r2(2) :-**
   Instruction type: R Type
   
   In R type instructions opcode=0110011,func7=0000000 . For srl func3=1011.The sum is stored in destination register r16 and r14,r2(2) are source registers .
   
   Decoding in binary format we get : r14=01110,r2(2)=01000,r16=10000.

   ![p13](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/10b69184-494e-445a-a645-b920317f4636)

</details>

---------------------------------------------------

<details>
<summary><b>Task 3:</b> The task involves referencing both C-based and RISC-V-based laboratory videos and subsequently executing the process of compiling C code using both the GCC compiler and the RISC-V compiler.</summary>
  
 # Task 3

  Refer to C based Lab video and RISC-V based lab videos. Complete exact steps on your machine. Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo.
```
$ leafpad sum1ton.c &

```

  ![s1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/63762f9d-6eba-47e4-ad2a-76db794c7e19)

```
 $ gcc sum1ton.c
  
 $ ./a.out

  ```

  ![s2](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/2ff7ab64-28bf-4965-918c-e12ba6ec3d4c)
```
 $ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
  ![s3](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/7e0c5a14-f0ad-4ce3-a825-5bd04da58d2f)
  
  ![s4](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/e307770c-6327-431c-acf2-be81eebd1beb)
```
 $ riscv64-unknown-elf-objdump -d sum1ton.o
  
 $ riscv64-unknown-elf-objdump -d sum1ton.o | less

```
![s5](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/16899512-5120-477a-9e38-638ce2c1acf9)

</details>

-------------------------------------------------

<details>
<summary><b>Task 4:</b> The task entails conducting SPIKE simulation and debugging the C code by employing the Interactive Debugging Mode using Spike.</summary>


# TASK 4

SPIKE Simulation and observation with -O1 and -Ofast. Upload snapshot of compiled C Code, RISC-V Objdmp with above options on your GitHub repo

**Spike installation**
```
$ git clone https://github.com/riscv/riscv-isa-sim.git      
$ cd riscv-isa-sim    
$ mkdir build  
$ cd build  
$ ../configure --prefix=/opt/riscv
$ sudo apt-get install device-tree-compiler
$ make  
$ sudo apt update  
$ sudo apt install g++-8  
$ make CXX=g++-8  
$ sudo make install  
$ echo 'export PATH=$PATH:/opt/riscv/bin' >> ~/.bashrc  
$ source ~/.bashrc
```

**pk installation**
```
$ git clone https://github.com/riscv/riscv-pk.git    
$ cd riscv-pk    
$ mkdir build    
$ cd build      
$ ../configure --prefix=/home/vsduser/riscv --host=riscv64-unknown-elf --with-arch=rv64gc    
$ make    
$ sudo make install
```

**Commands which provide output of sum of numbers from 1 to n using gcc compiler**
```
$ riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
$ gcc sum1ton.c
$ ./a.out
```

**Debugging the C code using spike**

```
$ spike pk sum1ton.o
$ spike -d pk sum1ton.o
until pc 0 100b0 (program counter(PC) to run till the starting address of the "main" which is 100b0)
```
![spike](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/c0d8f4ad-6581-4352-b905-f8317a6ca277)

</details>

----------------------------------------

<details>
<summary><b>Task 5:</b> 
Utilizing the RISC-V Core's Verilog netlist and testbench, conduct an experiment involving Functional Simulation and observe the resulting waveforms</summary>  
<br>

# TASK 5

Use this RISC-V Core Verilog netlist and testbench for functional simulation experiment. Upload waveform snapshots for the commands on your GitHub.

**Initial steps to follow**
```
$ git clone https://github.com/harsha240yeager/VSDSquadron_miniInternship.git
$ cd VSDSquadron-miniInternship
$ iverilog -o VSDSquadron-miniInternship iv_gt.v iv_gt_tb.v
$ vvp VSDSquadron-miniInternship
$ gtkwave iv_gt.vcd
```

![gt1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/3caff867-32f1-4133-9c3c-879ba544830b)

![gt2](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/5101c87d-665d-482e-9f85-22bd44348170)

![gtk1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/865dcf39-6ef8-4d30-9181-2856bcef5b0e)

## Instrunctions present in the Design file defined with specific Hexadecimal number

![i1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/7b37f799-0843-4b94-ae27-c0518254cce2)

### Specified Instruction set Outputs

IR - 32 bit Instruction , RD - Destination Register , A & B - Source Registers , ALUOUT - Output

**Instruction 1 -: ADD R6, R2, R1**

![ii1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/8f4e9bd9-143d-4119-b03a-5228897330dd)


**Instruction 2 -: SUB R7, R1, R2**

![ii2](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/29384d45-e6fa-4f8b-93c5-3278dd71715e)



**Instruction 3 -: AND R8, R1, R3**

![ii3](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/d4e58ed2-79d9-4918-be66-ed266eda4362)



**Instruction 4 -: OR R9, R2, R5**

![ii4](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/2f32754c-4f3a-4e1c-a78d-c702cac4209c)


**Instruction 5 -: XOR R10, R1, R4**

![ii5](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/69ebcb8f-da98-47d0-bedd-e2cf7e1db8f0)


**Instruction 6 -: SLT R1, R2, R4**

![ii6](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/d28813a5-9e44-4b01-915e-3175404f8685)

**Instruction 7 -: ADDI R12, R4, 5**

![ii7](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/d82b9f65-70f3-4c8b-8328-1e67c17d96dd)


**Instruction 8 -: BEQ R0, R0, 15**

![ii8](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/ca6c5fa8-886a-42d7-aefd-9335e451d05d)


**Instruction 9 -: LW R13,R1,2**

![ii9](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/172c880f-7964-47cc-b80d-b0b61fcbdfcf)


**Instruction 10 -: SW R3,R1,2**

![ii10](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/831ab3f9-3772-4baf-af73-847a48d0a12d)


</details>  

--------------------------------------------------------------- 

<details>
<summary><b>Task 6:</b> The culminating task of this internship entails implementing a digital circuit utilizing VSDSquadron Mini and verifying the functionality by assessing the building and uploading process of a C program file onto the RISC-V processor</summary> 


## Implementing Full Subtractor using VSDSquadron Mini  
  
### **Overview**  
This project involves the implementation of a Full Subtractor combinational circuit using VSDSquadron Mini, a RISCV based SoC development kit. Full Subtractor is an essential component in digital electronics, commonly employed in designing n-bit Subtracter circuits. A full subtractor circuit is a digital circuit that subtracts two binary digits and a borrow-in digit to produce a difference and borrow-out digit. It serves as a crucial element in digital circuits performing subtraction operations. This project showcases the practical application of digital logic and RISC-V architecture in executing arithmetic operations. It demonstrates the process of reading and writing binary data through GPIO pins, implementing the operation of full subtractor through digital logic gates simulated using PlatformIO IDE, and displaying the outputs using LEDs. 

![sub1](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/cdd4837d-b41b-4636-89f7-647d3045633a)

  
### **Components Required**  
* VSDSquadron Mini  
* Push Buttons for Input of binary data  
* 2 LEDs for displaying the Output  
* Breadboard  
* Jumper Wires  
* VS Code for Software Development  
* PlatformIO multi framework professional IDE

### **Logical Diagram and Expressions**

![sub_l](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/9cec7e1d-50b8-4051-8112-ae5d428f4c98)

---

D   = (A XOR B) XOR Bin
    
    = A’B’Bin + A’BBin’ + AB’Bin’ + ABBin
   
    = Bin(A’B’ + AB)  + Bin’(AB’ + A’B)
    
    = Bin( A XNOR B) + Bin’(A XOR B)
    
    = Bin (A XOR B)’  +  Bin’(A XOR B)
    
    = Bin XOR (A XOR B)
    
    = (A XOR B) XOR Bin

 Bout= A’Bin + A’B + BBin
 
     = A’B’Bin + A’BBin’ + A’BBin + ABBin      
    
     = A’B’Bin +A’BBin’ + A’BBin + A’BBin + A’BBin + ABBin
     
     = A’Bin(B + B’) + A’B(Bin + Bin’) + BBin(A + A’)
     
     = A’Bin + A’B + BBin
---     
  
### **Hardware Connections**  
* **Input:** Three input of single bit are connected to the GPIO pins of VSDSquadron Mini via push buttons mounted on the breadboard.  
* **Outputs:** Two LEDs are connected to display the result of Full Subtractor.   
  
### **Truth Table to Verify the Full Adder**  

![sub_truth](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/5ec2821d-c295-4eee-badb-1e8b0a0df4f6)

    
### Program  
```
// Full Subtractor Implementation

// Included the required header files
#include <stdio.h>
#include <debug.h>
#include <ch32v00x.h>

// Defining the Logic Gate Functions
int and(int bit1, int bit2)
{
    int out = bit1 & bit2;
    return out;
}
int or(int bit1, int bit2)
{
    int out = bit1 | bit2;
    return out;
}
int xor(int bit1, int bit2)
{
    int out = bit1 ^ bit2;
    return out;
}
int not(int bit)
{
    int out = ~bit & 1; // Ensuring only the least significant bit is considered
    return out;
}

// Configuring GPIO Pins
void GPIO_Config(void)
{
    GPIO_InitTypeDef GPIO_InitStructure = {0}; // structure variable used for GPIO configuration
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE); // to enable the clock for port D
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC, ENABLE); // to enable the clock for port C
    
    // Input Pins Configuration
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_1 | GPIO_Pin_2 | GPIO_Pin_3;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU; // Defined as Input Type with pull-up
    GPIO_Init(GPIOD, &GPIO_InitStructure);

    // Output Pins Configuration
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_4 | GPIO_Pin_5;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP; // Defined Output Type
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz; // Defined Speed
    GPIO_Init(GPIOC, &GPIO_InitStructure);
}

// The MAIN function responsible for the execution of the program
int main()
{
    uint8_t A, B, Bin, Diff, Bout; // Declared the required variables
    uint8_t p, q, r; 
    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_2);
    SystemCoreClockUpdate();
    Delay_Init();
    GPIO_Config();

    while(1)
    {
        A = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_1);
        B = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_2);
        Bin = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_3);
        
        // Full Subtractor Logic
        Diff = xor(xor(A, B), Bin); // Difference = A ⊕ B ⊕ Bin
        p = and(not(A), B); // p = A' B
        q = and(B, Bin); // q = B Bin
        r = and(not(A), Bin); // r = A' Bin
        Bout = or(or(p, q), r); // Borrow out = A' B + B Bin + A' Bin

        // Write the Difference output
        if(Diff == 1)
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_4, RESET); // LED on for Difference = 1
        }
        else
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_4, SET); // LED off for Difference = 0
        }

        // Write the Borrow output
        if(Bout == 1)
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_5, RESET); // LED on for Borrow out = 1
        }
        else
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_5, SET); // LED off for Borrow out = 0
        }
    }
}
                                                                                              
```  

### Application Video  

[Video link](https://drive.google.com/file/d/1pPG_-_EH2geWBX1sQKpaL642XB0bNlLJ/view?usp=sharing)

</details>

--------------------------------------------------------------

<details>
<summary>Acknowledgement</summary>
<br>

>*I extend my heartfelt gratitude to Kunal Ghosh Sir for providing an exceptional internship experience focused on RISC-V Architecture using VSDSquadron Mini. This opportunity has enabled me to delve into the realm of RISC-V with enthusiasm, serving as an invaluable kickstart to my journey. I have cherished every moment of this internship program and am immensely grateful to VLSI System Design for offering such an extraordinary research internship opportunity.*  

</details>




