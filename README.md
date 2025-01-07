# samsung-riscv
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.

## Basic Details

Name: Praveen M S

College: Vidyavardhaka College of Engineering

Email ID: praveenms588@gmail.com

GitHub Profile: praveenms588

LinkedIN Profile: praveenms588

## Task 1: Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler

## C and RISC-V Based Labs

This repository demonstrates the processes involved in compiling C programs and generating assembly code using both a standard GCC compiler and a RISC-V GCC compiler. It includes comprehensive steps and explanations to guide users through each stage of the compilation and debugging workflow.

## C Language-Based Lab

### Steps to Compile a .c File on Your Machine:

1. Open the bash terminal and navigate to the directory where you want to create your file.
2. Use the following command to create and edit a new .c file:
   ```sh
   gedit sum_1ton.c
![sum1ton_code_snippet](https://github.com/user-attachments/assets/04232a53-ca09-4015-85fb-3a441fc0b7dd)
### Steps to Compile a .c File :
 ```sh
 gcc sum_1ton.c
 ./a.out
```
### Compilation and execution complete.

![sum1ton_output](https://github.com/user-attachments/assets/24681ff5-a2ab-45c2-a6f5-bbb96f3e8058)


## RISC-V Based Lab

### Steps to Compile Using RISC-V GCC Compiler:
1. Ensure the RISC-V GCC compiler is installed and accessible on your system.
2. Verify the .c file contents using the cat command:
```sh
cat sum_1ton.c
```
![cat_sum1ton](https://github.com/user-attachments/assets/804de266-d64b-4bfc-82e5-d001f9e754cd)

4. Compile the C program for RISC-V architecture using:
 ```sh
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
```
5. Disassemble the object file to view its assembly code using:
 ```sh
riscv64-unknown-elf-objdump -d sum_1ton.o
```
6. Use /main in the terminal to locate the main function in the assembly output.
![assembly_code_snippet](https://github.com/user-attachments/assets/98ebc243-65f5-441a-8e8e-dc1353a18050)

### Explanation of Commands and Options: 
1. -mabi=lp64: Specifies the Application Binary Interface (ABI) for 64-bit integers, pointers, and long data types, suitable for 64-bit RISC-V architecture.

2. -march=rv64i: Indicates the 64-bit RISC-V base integer instruction set architecture.

3. -O1: Enables basic optimization for better performance without significantly increasing compilation time.

4. riscv64-unknown-elf-objdump: A tool for disassembling RISC-V binaries to examine the code structure and debug it effectively.
