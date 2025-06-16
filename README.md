# Simulator of RISC-V instructions in sed

This `sed` script accepts a `.hex` file with one hexadecimal word (32 bits) per line and starts executing it from the beginning.

To support ecall 5 (input from stdin), run it with an extra `-` argument (for example `./simulator.sed ./mem.hex -`) and feed it with an extra newline after the memory content (an empty line at the end of the `.hex` file or an enter after running the command).

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
* mul
* div
* divu
* remu
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
* ecall (a7 – call number, a0 – argument, supported call numbers: 10 – exit, 34 – print in hexadecimal, 35 – print in binary, 36 – print in decimal, all unsigned, 1 – print in decimal, signed, 5 – read in decimal, signed or unsigned, 4 – print string)
* fence (does nothing)

Strings are zero‐terminated in UTF-32. To avoid having the complete Unicode table in the source, only non‐control characters from these blocks are supported:
* Basic Latin
* Latin-1 Supplement
* Latin Extended-A
* General Punctuation
* Arrows
* Mathematical Operators
