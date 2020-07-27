# Implementation of Two-pass Assembler

For the Implementation part of our design, we made a C program (test1.c) that takes a Machine-operation codes file (input_opcode.txt) and an assembly level instructions file (input_instructions.txt) as input and after execution, the binary codes for each instruction and the information about labels are written in files (output_machine_code.txt) and (symbol_table.txt) respectively. Source code for the program is attached in the c file (test1.c). Steps in which the execution of the program takes place are shown below:
-	The opcodes along with their binary codes are stored into a hash-table which is formed during the execution of the program. 
-	During Pass 1, a symbol table which contains all labels is generated and can be read in (symbol_table.txt). 
-	During Pass 2, the program is again read and symbol table formed in Pass 1 is used to get the corresponding address associated with each label. Then, each instruction is converted to 32-bit machine code. 

<br /><br />**We have included the following operand formats in our instructions:** <br /><br />
-	r r i = THREE OPERAND REGISTER-REGISTER-IMMEDIATE INSTRUCTION
-	r r r = THREE OPERAND REGISTER-REGISTER-REGISTER INSTRUCTION
-	r i = TWO OPERAND REGISTER IMMEDIATE INSTRUCTION
-	r r = TWO OPERAND REGISTER REGISTER OPERAND INSTRUCTION
-	r = ONE OPERAND REGISTER OPERAND INSTRUCTION
-	a = ONE OPERAND ADDRESS OPERAND INSTRUCTION
-	z = ZERO OPERAND INSTRUCTION

<br /><br /> **We have also associated 5-bit address with each register:** <br /><br />
-	R0-----> 00000	
-	R1-----> 00001
-	R2-----> 00010
-	R3-----> 00011
-	R4-----> 00100
-	R5-----> 00101
-	R6-----> 00110
-	R7-----> 00111
-	R8-----> 01000
-	R9-----> 01001
-	R10-----> 01010
-	R11-----> 01011
-	R12-----> 01100
-	R13-----> 01101
-	R14-----> 01110
-	R15-----> 01111

<br /> <br /> **Special registers for storing the size of the array:** <br /><br />
-	A0-----> 10000
-	A1-----> 10001
-	A2-----> 10010
-	A3-----> 10011

<br /> <br /> **Special registers for handling IN/OUT instructions:** <br /><br />
-	port0 -----> 10100
-	port1 -----> 10101

