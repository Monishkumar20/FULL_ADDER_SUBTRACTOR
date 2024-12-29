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

1.FULL ADDER

![WhatsApp Image 2024-12-21 at 09 58 48_2ab9c91a](https://github.com/user-attachments/assets/fa54badc-e2d4-4c1b-90e7-cceb9814dbcc)

2.FULL SUBTRACTOR

![WhatsApp Image 2024-12-21 at 09 59 07_32a49606](https://github.com/user-attachments/assets/9ca9ad3d-7c01-47d1-9717-098a1307209c)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram. Program:

**Program:**
```
Full Adder: 

module ex(a,b,cin,sum,carry);
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
```
**RTL Schematic**

![image](https://github.com/user-attachments/assets/77681f81-4678-47ff-8937-09289c1fd417)

![image](https://github.com/user-attachments/assets/1d18775a-16ad-42ba-9510-86a53087458b)


**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/93c7fb26-7070-42f4-98ff-a0d4fd879f04)

![image](https://github.com/user-attachments/assets/2c2f6200-4ea3-40fa-a05a-6bd8221c7df5)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



