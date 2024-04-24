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
