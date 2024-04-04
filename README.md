***FULL_ADDER_SUBTRACTOR***
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

image

Figure -1 FULL ADDER

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

image

Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![WhatsApp Image 2024-04-04 at 13 39 52_6b640332](https://github.com/Munimadhuriganji/FULL_ADDER_SUBTRACTOR/assets/138849444/3bf9532e-94b2-48fa-859c-9569a2a7eb54)

![WhatsApp Image 2024-04-04 at 13 39 52_fdcdc378](https://github.com/Munimadhuriganji/FULL_ADDER_SUBTRACTOR/assets/138849444/27310810-8c5b-4d24-9ce5-ee20f2a84471)

**Procedure**

**Full Adder:**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

**Full Subtractor:**

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

*Developed by:* GANJI MUNI MADHURI
*RegisterNumber:* 212223230060

Full adder
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule
```

Full subractor
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
*/

**RTL Schematic**
![sa](https://github.com/Munimadhuriganji/FULL_ADDER_SUBTRACTOR/assets/138849444/66d55441-aaed-4897-a3dc-7340a7e563d2)

**Output Timing Waveform**
![Screenshot 2024-04-04 134916](https://github.com/Munimadhuriganji/FULL_ADDER_SUBTRACTOR/assets/138849444/281c4a65-5a32-47f4-8346-3ed4350a6b4b)

![Screenshot 2024-04-04 135139](https://github.com/Munimadhuriganji/FULL_ADDER_SUBTRACTOR/assets/138849444/fce8832a-f4ac-4354-9d24-ba220b8b922b)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

