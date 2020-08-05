# Two pass assembler using C

## What is an Assembler?
Assembler is a program for converting instructions that are written in low-level assembly code into relocatable machine code and generating information along, for the loader.

## What is a Single Pass Assembler?

It is an assembler that generates the object code directly in memory for immediate execution. It passes through your source code only once and then it’s done. It generates instructions by evaluating the mnemonics in operation field and finds the value of symbol and literals to produce machine code.

## What is a Two-Pass assembler?

When an assembler divides its tasks in two passes, it is called a Two-pass assembler.
-	Pass-1:

1.	Defines symbols and literals and remembers them in symbolic table form and literal table form respectively.
2.	Keep track of location counter.
3.	Process pseudo-operations.
-	Pass-2:

1.	Generate object code by converting symbolic op-code into corresponding numeric op-code.
2.	Generate data for literals and look for values of symbols.

## Why do we need a Two-pass assembler?

One-pass assembler cannot resolve issues of forward references of data symbols. It requires all data symbols to be defined before they are being used. A Two-pass assembler solves this confusion by devoting one pass exclusively to resolve all issues of forward referencing and then generates object code with no chaos in the next pass. 

