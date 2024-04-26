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

$ sudo apt-get install autoconf automake autotools-dev curl python3 python3-pip libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev ninja-build git cmake libglib2.0-dev libslirp-dev
$ git clone https://github.com/riscv/riscv-gnu-toolchain

./configure --prefix=/opt/riscv make linux
![gnu2](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/c14b6ee5-518e-4a20-8740-fb9a19262075)
![riscv-gnu-toolkit](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/39ceff7a-b014-40bf-8900-6577f3cfc3fa)

3.Installation of Yosys

$ git clone https://github.com/YosysHQ/yosys.git

$ sudo apt install make

$ cd yosys

$ sudo apt-get install build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc

$ make

$ sudo make install

Yosys
![yosys](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/ba317979-8c27-4c37-9a07-38627512c916)

4.Installation of iverilog

sudo apt-get install iverilog 
![iverilog](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/82746fbc-16d6-4d66-a0d6-771630cb0018)

5.Installation of gtkwave

sudo apt update

sudo apt install gtkwave
![gtkwave](https://github.com/harsha240yeager/VSDSquadron_miniInternship/assets/105859299/c00d0487-dfec-4f31-be8b-0cf29c2f9e57)


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
**1.I-Format :** instructions with immediates, loads
  - addi, lw, jalr, slli
**1.S-Format :**  store instructionss
  -sw, sb
**1.B-Format :** branch instructions
  -beq, bge
**1.U-Format :** instructions with upper immediates
  -lui, auipc     —upper immediate is 20-bits
**1.J-Format :** jump instructions
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
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**6.slt r11,r2,r4 :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**7.addi r12,r4,r5 :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**8.sw r3,r1,2 :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**9.lw r13,r1,2 :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**10.beg r0,r0,15 :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**11.bne r0,r1,20 :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**12.sll r15,r1,r2(2) :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.

**13.srl r16,r14,r2(2) :-**
   Instruction type: R Type
   In R type instructions opcode=0110011,func7=0000000 . For add func3=000.The sum is stored in destination register r6 and r1,r2 are source registers .
   Decoding in binary format we get : r1=00001,r2=00010,r6=00110.
   

