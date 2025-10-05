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

FULL ADDER


<img width="386" height="309" alt="Screenshot 2025-10-06 010949" src="https://github.com/user-attachments/assets/1b012b75-7415-4998-96f7-67aabf63c940" />


FULL SUBTRACTOR


<img width="376" height="267" alt="Screenshot 2025-10-06 011100" src="https://github.com/user-attachments/assets/5d244127-16bb-48ee-a2c4-42716466689b" />


**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.


**Program:**

Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming.


i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule


ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule


**RTL Schematic**


FULL ADDER


<img width="1920" height="984" alt="Screenshot 2025-10-06 005444" src="https://github.com/user-attachments/assets/09b9bf12-becd-4399-a88b-682665de8fb9" />


FULL SUBTRACTOR


<img width="1920" height="991" alt="Screenshot 2025-10-06 010429" src="https://github.com/user-attachments/assets/faabd8bc-00f6-4bd0-9165-caf7f36bc8ab" />



**Output Timing Waveform**


FULL ADDER


<img width="1920" height="983" alt="Screenshot 2025-10-06 010021" src="https://github.com/user-attachments/assets/1f8479c3-6d77-4105-ae32-18e3ce913468" />


FULL SUBTRACTOR


<img width="1920" height="989" alt="Screenshot 2025-10-06 010659" src="https://github.com/user-attachments/assets/00bed295-5941-4162-a011-03bcb40c8f74" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



