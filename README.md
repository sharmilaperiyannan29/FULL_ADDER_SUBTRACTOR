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

Developed by:sharmila Register number:212225230261
**Program:**
FULL ADDER:
```
module fulladder(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```
FULL SUBRACTOR:
```
module sub(a,b,c,x,y,z,sum,dif,car,bor);
input a,b,c,x,y,z;
output sum,dif,car,bor;
assign sum = a^b^c;
assign car = a&b | a&c | b&c;
assign dif = x^y^z;
assign bor = ~x&z | ~x&y | y&z;
endmodule
```

**RTL Schematic**
FULL ADDER
<img width="1307" height="737" alt="image" src="https://github.com/user-attachments/assets/546dd762-8e81-4ce8-a7f4-354390cfb8f1" />
FULL SUBRACTOR
<img width="1306" height="682" alt="image" src="https://github.com/user-attachments/assets/102a8d68-c18c-4349-9e53-b3b71a5c2385" />

**Output Timing Waveform**
FULL ADDER
<img width="1168" height="580" alt="image" src="https://github.com/user-attachments/assets/6f61e6c4-cd8a-43f5-b463-f5bb1ee30ce6" />
FULL SUBRACTOR
<img width="1167" height="595" alt="image" src="https://github.com/user-attachments/assets/ad0e0d63-2e95-4a33-8750-15200546b8ac" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



