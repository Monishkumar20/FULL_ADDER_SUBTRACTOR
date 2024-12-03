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
![image](https://github.com/user-attachments/assets/810d6c12-a370-4fc4-9e8c-cd1d57bfb176)


**Truthtable**
![image](https://github.com/user-attachments/assets/acb82e81-706c-4f54-a3d1-d3aae49fabcd)


**Procedure**

Write the detailed procedure here

**Program:**
Full Adder: 

~~~module ex(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

Full Subtractor:

module ex2(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule
~~~
**RTL Schematic**
![image](https://github.com/user-attachments/assets/ca371c30-4d11-4f77-a386-0423a5022e86)
![image](https://github.com/user-attachments/assets/7a295b31-e5eb-43fa-85bd-bcc93b77876c)



**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/244c100f-e090-4894-84b4-8a0b73f1f641)
![image](https://github.com/user-attachments/assets/1d539bdd-557c-4be5-b65d-75a6f70083f0)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



