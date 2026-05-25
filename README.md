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
1.Open Quartus Prime software and create a new project.
2.Select the target device and create a Verilog HDL file.
3.Write the Verilog code for Full Adder and Full Subtractor circuits.
4.Compile the program and correct any syntax errors.
5.Generate the RTL schematic and verify the logic design.
6.Create the input waveform and simulate the circuit.
Verify the output timing waveform with the truth table.
## Full Adder
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:SANJAY A
RegisterNumber:212225040367
*/
```
module full_adder(sum, carry, a, b, cin);
    output sum;
    output carry;
    input a;
    input b;
    input cin;

    assign sum = a ^ b ^ cin;
    assign carry = (a & b) | (cin & (a ^ b));
endmodule
```
**RTL Schematic**
<img width="747" height="260" alt="Screenshot 2026-05-25 201607" src="https://github.com/user-attachments/assets/0038d938-99a9-46b5-ad74-e4826a113e15" />

**Output Timing Waveform**
<img width="1043" height="595" alt="Screenshot 2026-05-25 201621" src="https://github.com/user-attachments/assets/b8e02131-d65e-481c-a3f3-0d92297fdba7" />


## Full Subtractor
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:SANJAY A
RegisterNumber:212225040367
*/
```
module full_subtractor(diff, borrow, a, b, bin);
    output diff;
    output borrow;
    input a;
    input b;
    input bin;

    assign diff = a ^ b ^ bin;
    assign borrow = (a & b) | ((a ^ b) & bin);
endmodule
```
**RTL Schematic**
<img width="753" height="278" alt="Screenshot 2026-05-25 202247" src="https://github.com/user-attachments/assets/bd8ddf32-44c6-4d18-9695-49672e4a8aea" />


**Output Timing Waveform**
<img width="1058" height="590" alt="Screenshot 2026-05-25 202317" src="https://github.com/user-attachments/assets/1b9c94c1-a615-49f5-9ca7-8384c239dc92" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



