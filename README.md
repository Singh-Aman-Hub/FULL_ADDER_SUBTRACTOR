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
![Full sub](https://github.com/user-attachments/assets/1fbb9823-e118-465b-886c-9bd201515c87)
![full-adder-truth-table](https://github.com/user-attachments/assets/b7127e4c-8b08-4fc1-92e0-c5e3795d5622)



**Program:**

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
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule

**RTL Schematic**
![logic diagram](https://github.com/user-attachments/assets/3f36df67-3409-448f-acb1-971cad970894)
![logic diagram](https://github.com/user-attachments/assets/b665b639-9dd0-41df-9e83-cc99df2edf65)



**Output Timing Waveform**
![waveform](https://github.com/user-attachments/assets/7d0d7274-11f5-479d-bbec-0f3c2122525d)
![waveform](https://github.com/user-attachments/assets/220e8dbd-faf2-462f-ad78-6e633f129f0e)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

![waveform](https://github.com/user-attachments/assets/fc11bdef-b004-4201-9cfc-be231bfc5321)

![waveform](https://github.com/user-attachments/assets/d3df3680-572e-4a11-931c-ba3b520766f4)



