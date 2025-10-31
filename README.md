# Arithmetic\_Logic\_Unit

<<<<<<< Updated upstream
=======


>>>>>>> Stashed changes
This repository contains the hierarchical design and implementation of a custom 4-bit Arithmetic Logic Unit (ALU) using Logisim. The ALU integrates essential circuits to perform arithmetic, logic, shift, and comparison operations.



<<<<<<< Updated upstream
The following circuits were designed as sub-components for the main ALU:

1- Full Adder(FA-1Bit)
Function: Performs the addition of two input bits and one carry-in bit, producing a Sum bit and a Carry-Out bit
=======




The following circuits were designed as sub-components for the main ALU:







&nbsp;1- Full Adder(FA-1Bit)



Function: Performs the addition of two input bits and one carry-in bit, producing a Sum bit and a Carry-Out bit



>>>>>>> Stashed changes
Logic: If all inputs are 0, the output is 0. If exactly one input is 1, the Sum output is 1 and Carry-out is 0. If two inputs are 1, the sum is 0 and Carry-Out is 1. If all inputs are 1, the Sum and Carry-Out are both 1



<<<<<<< Updated upstream
2- Arithmetic Unit (AU)
Function: Used to perform 4-bit addition and subtraction of two 4-bit numbers (A and B)
Control: It consists of four Full Adders, The operation is selected using the Carry-in input
If Cin = 0: Performs Addition (A + B)
If Cin = 1: Performs Subtraction (A - B) using two's complement



3- Logic Unit
Function: Performs 4-bit logic operations (AND, OR, XOR, NOT) on two 4-bit inputs (A and B)
Control: It consists of 4 Multiplexers (MUX) controlled by 2 Select lines: (S0, S1) to choose one of 4 logic gates (AND, OR, XOR, NOT)
S1=0, S0=0: Selects the AND operation
S1=0, S0=1: Selects the OR operation
S1=1, S0=0: Selects the XOR operation
=======




&nbsp;2- Arithmetic Unit (AU)



Function: Used to perform 4-bit addition and subtraction of two 4-bit numbers (A and B)



&nbsp;Control: It consists of four Full Adders, The operation is selected using the Carry-in input



If Cin = 0: Performs Addition (A + B)



&nbsp;  If Cin = 1: Performs Subtraction (A - B) using two's complement







&nbsp;3- Logic Unit



Function: Performs 4-bit logic operations (AND, OR, XOR, NOT) on two 4-bit inputs (A and B)



&nbsp;Control: It consists of 4 Multiplexers (MUX) controlled by 2 Select lines: (S0, S1) to choose one of 4 logic gates (AND, OR, XOR, NOT)



S1=0, S0=0: Selects the AND operation



S1=0, S0=1: Selects the OR operation



&nbsp;S1=1, S0=0: Selects the XOR operation



>>>>>>> Stashed changes
S1=1, S0=1: Selects the NOT operation (applied to B)



<<<<<<< Updated upstream
4- Comparator
Function: Compares two 4-bit numbers (A and B) to determine their relative magnitude
=======




&nbsp;4- Comparator



Function: Compares two 4-bit numbers (A and B) to determine their relative magnitude



>>>>>>> Stashed changes
Outputs: Produces three outputs: Greater (A>B),Equal (A = B),or Less(A<B)



<<<<<<< Updated upstream
5- Right Shift (R-Shift)
Function: Performs a logical right shift on the 4-bit number by one position
=======




&nbsp;5- Right Shift (R-Shift)



Function: Performs a logical right shift on the 4-bit number by one position



>>>>>>> Stashed changes
Operation: Divides the number by 2, A '0' is introduced into the leftmost (most significant) bit position



<<<<<<< Updated upstream
6- Left Shift (L-Shift)
=======




&nbsp;6- Left Shift (L-Shift)



>>>>>>> Stashed changes
Function: Performs a logical left shift on the 4-bit number by one position Operation: Multiplies the number by 2, A '0' is introduced into the rightmost (least significant) bit position



<<<<<<< Updated upstream
7- Arithmetic Logic Unit (ALU)
The main ALU circuit combines all the above sub-circuits (AU, Logic Unit, Shift, Comparator) and uses three control lines (Select) to choose the operation:
Select Code (S2 S1 S0) Operation Selected
Arithmetic Unit:(Addition/Subtraction): 000
Logic Unit:(AND/OR/XOR/NOT): 001
Right Shift: 010
Left Shift: 011
Comparator:(Greater): 100
Comparator:(Equal): 101
=======








&nbsp;7- Arithmetic Logic Unit (ALU)



The main ALU circuit combines all the above sub-circuits (AU, Logic Unit, Shift, Comparator) and uses three control lines (Select) to choose the operation:







\&Select Code (S2 S1 S0) Operation Selected



\& Arithmetic Unit:(Addition/Subtraction): 000



Logic Unit:(AND/OR/XOR/NOT): 001



Right Shift: 010



Left Shift: 011



Comparator:(Greater): 100



Comparator:(Equal): 101



>>>>>>> Stashed changes
Comparator:(Less): 110

