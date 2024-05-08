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

**Full adder**

![image](https://github.com/narenm03/FULL_ADDER_SUBTRACTOR/assets/152469427/1d99b16d-9347-4f0d-9a06-b4f9535f7091)

**Full subtractor**

![image](https://github.com/narenm03/FULL_ADDER_SUBTRACTOR/assets/152469427/9edd1c21-ea2b-4613-9bc6-d6acf2997796)

**Procedure**

**Full adder**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

**Full subtractor**

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
*/
## Developed by: NARENDHARAN.M 
## RegisterNumber:212223230134

```
module FULL_addsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum = a^b^cin;
assign carry = (a&b) | (b&cin) | (a&cin);
wire a0;
not (a0,a);
//Write syntax for full subtractor Borrow and Difference in data flow modelling
assign DIFF = a^b^cin;
assign BO = (a0&b) | (b&cin) | (a0&cin);
endmodule
```
### RTL Schematic
![image](https://github.com/narenm03/FULL_ADDER_SUBTRACTOR/assets/152469427/3e02aa78-a870-4584-a84d-723fa4d46be6)

### Output Timing Waveform
![image](https://github.com/narenm03/FULL_ADDER_SUBTRACTOR/assets/152469427/51127c0f-98f0-4503-b66b-fd07ba7ebfd5)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



