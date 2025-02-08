# Simulator of RISC-V instructions in sed

This `sed` script accepts a `.hex` file with one hexadecimal word (32 bits) per line and starts executing it from the beginning.

Currently supported instructions: 
* addi
* andi
* ori
* xori
* srli
* srai
* slli
* slti
* sltiu
* add
* sub
* and
* or
* xor
* srl
* sra
* sll
* slt
* sltu
* beq
* bne
* blt
* bltu
* bge
* bgeu
* lw
* lh
* lhu
* lb
* lbu
* sw
* sh
* sb
* lui
* auipc
* jal
* jalr
* ebreak (stops the execution and dumps the memory content to the standard output)
* ecall (a7 – call number, a0 – argument, supported call numbers: 10 – exit, 34 – print in hexadecimal, 35 – print in binary, 36 – print in decimal, all unsigned)
* fence (does nothing)
