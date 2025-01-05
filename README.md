# samsung-riscv
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.

# Basic Details

Name: Praveen M S

College: Vidyavardhaka College of Engineering

Email ID: praveenms588@gmail.com

GitHub Profile: praveenms588

LinkedIN Profile: praveenms588

Task 1: Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler

# C Language based LAB
We have to follow the given steps to compile any .c file in our machine:

Open the bash terminal and locate to the directory where you want to create your file. Then run the following command:

gedit sum_1ton.c
This will open the editor and allows you to write into the file that you have created. You have to write the C code of printing the sum of n numbers. Once you are done with your code, press Ctrl + S to save your file, and then press Ctrl + W to close the editor.

To the C code on your terminal, run the following command:

gcc sum_1ton.c
./a.out
C Code compiled on gcc Compiler

RISCV based LAB
We have to do the same compilation of our code but this time using RISCV gcc compiler. Follow the given steps:

Open the terminal and run the given command:

cat sum_1ton.c
cat Command

Using the cat command, the entire C code will be displayed on the terminal. Now run the following command to compile the code in riscv64 gcc compiler:

riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
Open a new terminal and run the given command:

riscv64-unknown-elf-objdump -d sum_1ton.o
Objdump using -O1 format

The Assembly Language code of our C code will be displayed on the terminal. Type /main to locate the main section of our code.
Descriptions of the keyword used in above command
-mabi=lp64: This option specifies the ABI (Application Binary Interface) to use lp64, which is for 64-bit integer, long and pointer size. This ABI is used for 64-bit RISCV architecture.
-march=rv64i: This option specifies the architecture that we use, which is rv64i, indicates the 64-bit RISCV base integer instruction set. This also confirms the targeting of 64-bit architecture.
riscv-objdump: A tool for disassembling RISC-V binaries, providing insights into the code structure and helping in debugging.
-Ofast: The option -Ofast in the command riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c is a compiler optimization flag used with the GNU Compiler Collection (GCC). This flag is used to instruct the compiler to optimize the generated code for maximum speed. The use of -Ofast is typically chosen for applications where execution speed is critical and where deviations from standard behavior are acceptable. However, it's important to test thoroughly, as this level of optimization can introduce subtle bugs, especially in complex calculations or when strict compliance with external standards is required.
-O1: This options is an optimization level that tells the compiler to optimize the generated code but without greatly increasing compilation time. -O1 aims to reduce code size and execution time while keeping the compilation process relatively quick.
Other common options are as follows:
-O0: No optimization, the default level if no -O option is specified.
-O2: More aggressive optimizations that might increase compilation time but typically provide faster and sometimes smaller code.
-O3: Maximizes optimization more aggressively than -O2.
-Os: Optimizes code for size. It enables all -O2 optimizations that do not typically increase code size.
Here, the term more aggressive optimization in the context of compilers like GCC refers to a deeper and more complex set of transformations applied to the code in order to improve its performance and possibly reduce its size. The compiler uses more complex techniques that aims to generate faster executing code or code that occupies less memory. However, these optimizations typically increase the compilation time and can sometimes introduce bugs, making it harder to debug.
