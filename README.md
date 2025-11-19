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

![WhatsApp Image 2025-11-19 at 10 25 07_0a44b0da](https://github.com/user-attachments/assets/939d0fb9-9b4a-4e61-bcb9-92fe047233a3)

![WhatsApp Image 2025-11-19 at 10 25 07_9c1abeca](https://github.com/user-attachments/assets/5c4856b9-0b05-4ba2-8552-c99acf35efd0)


**Procedure**

```
Full Adder:

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Full Subtractor:

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.
```

**Program:**
```
 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
 Developed by:Arjun.R.S
 RegisterNumber:25017547
```
**Full Adder**
```
module Fulladder(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule
```
**RTL Schematic**

<img width="1920" height="1080" alt="Screenshot 2025-11-19 103429" src="https://github.com/user-attachments/assets/10c11ce6-61af-438b-bf37-2796abd029bb" />

**Output Timing Waveform**

<img width="1920" height="1080" alt="Screenshot 2025-11-19 104456" src="https://github.com/user-attachments/assets/3ee6ebe8-27d3-48f0-a2a0-6b9d013b3013" />

**Full subtractor**
```
module Fullsubtractor(diff,borrow,a,b,c);
input a,b,c;
output diff,borrow;
xor(diff,a,b,c);
assign borrow= (~a)&c | (~a)&b | (b&c);
endmodule
```
**RTL Schematic**

<img width="1920" height="1080" alt="Screenshot 2025-11-19 105102" src="https://github.com/user-attachments/assets/27e5ed50-ea22-4f7b-a10a-fdd045853f88" />

**Output Timing Waveform**

<img width="1920" height="1080" alt="Screenshot 2025-11-19 105505" src="https://github.com/user-attachments/assets/e2006c76-c380-493d-a07e-dbf0b39d6d57" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



