# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
# Full Adder:
![Screenshot 2024-04-04 010034](https://github.com/jayaseelan2006/FULL_ADDER_SUBTRACTOR/assets/151389443/0166498b-15b5-44e2-a28e-5fd8c2ffbde4)
# Full Subtractor:
![Screenshot 2024-04-04 010048](https://github.com/jayaseelan2006/FULL_ADDER_SUBTRACTOR/assets/151389443/b555b0ff-9cdc-406b-8e54-6468d551f61b)


**Procedure**

Write the detailed procedure here

**Program:**
module full_addersub(a,b,c,sum,carry,D,Bo);

input a,b,c;

output sum,carry,D,Bo;

assign sum = a^b^c;

assign carry = (a&b)|(b&c)|(a&c);

assign D = a^b^c;

assign Bo = (~a&b)|(b&c)|(~a&c);

endmodule



**RTL Schematic**
![Screenshot 2024-04-04 010523](https://github.com/jayaseelan2006/FULL_ADDER_SUBTRACTOR/assets/151389443/4642d355-c57c-43fe-b3d4-8e4998768523)


**Output Timing Waveform**
![Screenshot 2024-04-04 010555](https://github.com/jayaseelan2006/FULL_ADDER_SUBTRACTOR/assets/151389443/26f4d637-d6f2-4f7a-8d58-81754a676fbf)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



