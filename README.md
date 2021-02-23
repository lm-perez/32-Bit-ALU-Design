# 32-Bit-ALU-Design
The objective is to implement and test a 32-bit Arithmetic Logic Unit (ALU) which is capable of performing six operations.

**Design and Implementation**

This project contains five components. 
1. 1-Bit Full Adder
2. 4-Bit Full Adder (built using four 1-bit adders)
3. 16-Bit Adder (built using four 4-bit adders)
4. 32-Bit Adder/Subtractor (built using two 16-bit adders)
5. ALU (32-bit adder/subtractor used to implement)

**I. 1-Bit Full Adder & 4-Bit Adder & 16-Bit Adder & 32-Bit Adder**

The adder component has three inputs: X, Y and Cin; and two outputs: S, and Cout. The component adds the three inputs and shows the sum on S (sum). If there is overflow, then Cout (carry out) is high. For there to be overflow, the sum has to be over the range of the n-bit adder. The range is calculated using 2n-1, where n is the number of bits. The only difference between the 1-bit adder, 4-bit adder, 16-bit adder and 32-bit adder is the number of bits.

**II. ALU**

The ALU core takes in three inputs: a, b, and op; and has three outputs: result, zero, and cout. The inputs a and b, and the output, result, have 32-bits; however for simplicity, the simulation was done using unsigned decimals. The op represents the operator inputs where it implements the operation that is to be done on a and b. The zero output is a binary output where it is high when the result is zero. The cout (overflow) is a binary output where it is high when the result is over the range of the n-bit adder. However, when adding the two inputs, there is overflow if the sum of positive numbers results in a negative number (in 2’s complement) and when subtracting, there is overflow if the sum of two negative numbers result in a positive number (in 2’s complement). This is shown in the waveform when subtracting 7 and 6. This binary of 7 and 6 are: 0000 0000 0000 0000 0000 0000 0000 0111 and 0000 0000 0000 0000 0000 0000 0000 0110 respectively. When subtracting, the binary equivalents of 7 and 6 are changed into 2’s complement and are added. The result is 0000 0000 0000 0000 0000 0000 0000 0001, which is 1 in 2’s complement. Therefore, there is overflow. 
