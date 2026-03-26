# ALU
ALU is a main component of the central processing unit, which stand for arithmetic logic unit and logic operations. It is also known as an integer unit (IU), an integrated circuit within a CPU or GPU, the last component to perform calculations in the processor. It can perform all processes related to arithmetic and logic operations such as addition, subtraction, multiplication, and shifting operations, including Boolean comparisons like logic gates.

## UNDERSTANDING AND ANALYSIS

### FOR ADD/SUBTRACT:
In our module AddSub that takes five inputs and two outputs. The inputs are two 5-bit vectors A and B, a 1-bit carry-in Cin, a 2-bit operation selector op. The outputs are a 5-bit sum or difference S and a 16-bit carry-out Cout. The module uses an always block that is triggered by the positive edge of clk. Inside the always block, there is an if statement that checks the value of op. If op is zero, it performs an addition operation on A and B with Cin and assigns the result to Cout and S. If op is one, it performs a subtraction operation on A and B with Cin and assigns the result to Cout and S.

### FOR MULTIPLLIER:
Our module mul2 that performs a 2-bit signed multiplication on two 5-bit inputs a and b, and produces a 16-bit output p. The input op is a 2-bit selector that determines whether the multiplication is performed or not. If op is zero, the output p is zero. If op is non-zero, the output p is the product of a and b.

The module uses four intermediate wires x0, x1, x2,x3 and x4 to store the partial products of each bit of a and b. For example, x0 is the result of the least significant bit of a with all bits of b. The module then uses four more intermediate wires s1, s2, s3, and s4 to perform a binary addition of the partial products with appropriate shifts.

The module uses an always block that is sensitive to the changes of Cout and S. This means that the block will be executed whenever Cout or S changes its value. However, this may not be what you intended, since Cout and S are outputs of the module and not inputs.

### FOR ALU:
Our model ALU2 that takes two 5-bit inputs A and B, a 2-bit operation selector Op, and produces a 16-bit output K and a 7-bit output segments. The module uses two submodules, AddSubtract and mul2, to perform addition, subtraction, and multiplication operations on A and B. The module also uses a case statement to assign the output K based on the value of Op. The output segments is used to display the value of Op on a 7-segment display.

## How does an arithmetic-logic unit work?
Typically, the ALU has direct input and output access to the processor controller, main memory (RAM) and input/output devices. Inputs and outputs flow along an electronic path that is called a bus.
