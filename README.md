# Simulator of RISC-V instructions in sed

This `sed` script accepts a `.hex` file with one hexadecimal word (32 bits) per line and starts executing it from the beginning.

Currently supported instructions: 
* addi
* add
* sub
* and
* or
* xor
* srl
* sra
* sll
* beq
* bne
* blt
* bltu
* bge
* bgeu
* lw
* sw
* lui
* jal
* jalr
* ebreak (stops the execution and dumps the memory content to the standard output)
