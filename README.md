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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
//full adder
module EXP_4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(C1,a,b);
xor(sum,s1,cin);
or(cout,c2,c1);
endmodule

module EXP_4 (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

Developed by:Muralidar RegisterNumber:24900233
*/
![464dab60-5964-4490-b1d3-98a13db85ef4](https://github.com/user-attachments/assets/601a3e12-f855-48a5-9a2b-977f9f4269be)

![8fa230de-128b-4171-8ce3-720d164461c2](https://github.com/user-attachments/assets/ec3065c6-5cf0-450e-825a-805d331aa8bf)


**RTL Schematic**
![EXP4 RTL](https://github.com/user-attachments/assets/0cbb0bf6-502d-44ec-8090-968a1802ede4)

![EXP4 RTL2](https://github.com/user-attachments/assets/ddb5ab78-3cfd-4dee-82b0-964bdbf8605b)




**Output Timing Waveform**

![EXP4 Waveform](https://github.com/user-attachments/assets/180a9dab-569f-4c30-b931-4c199f9bd130)

![EXP4 Waveform2](https://github.com/user-attachments/assets/33b9056b-6515-441a-ba43-1dbf3f280e56)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



