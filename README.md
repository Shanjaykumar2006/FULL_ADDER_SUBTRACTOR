# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

Devoloped By : SHANJAY KUMAR.S

Register No : 212224230245

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

![image](https://github.com/user-attachments/assets/37cd1ff6-d443-4860-9035-42464686a51c)


**Procedure**

Write the detailed procedure here

**Program:**

FULL ADDER

module exp4(a,b,c,sum, carry);

input a,b,c;

output sum, carry;

wire w1,w2,w3;

assign sum=a^b^c;

assign w1=a&b;

assign w2=b&c;

assign w3=c&a;

assign carry=w1|w2|w3;

endmodule;

FULL SUBTRACTOR

module exp4_1(df,bo,a,b,bin);

input a,b,bin;

output df,bo;

wire w1,w2,w3;

assign w1=a^b;

assign w2=(~a&b);

assign w3=(~w1&bin);

assign df=w1^bin;

assign bo=w2|w3;

endmodule



/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

![image](https://github.com/user-attachments/assets/f4fbe279-5c5a-4631-9668-820a5a62b930)

![image](https://github.com/user-attachments/assets/a4733e74-d710-4032-9a40-fc900f15d0e8)

**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/0f85d77f-6207-49ff-9b20-6c80d975fd24)

![image](https://github.com/user-attachments/assets/bf30bdec-e69f-4beb-b626-59a8aee2ae64)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



