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
FULL ADDER
module ha_dataflow(a, b, s, ca);
    input a;
    input b;
    output s;
    output ca;
	 assign#2 s=a^b;
	 assign#2 ca=a&b;
endmodule

FULL SUBTRACTOR
module hs_behv(a, b, dif, bor);
    input a;
    input b;
    output dif;
    output bor;
	 reg dif,bor;
	 reg abar;
	 always@(a or b) begin
	 abar=~a;
	 dif=a^b;
	 bor=b&abar;
	 end
endmodule


**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot 2025-12-04 211846" src="https://github.com/user-attachments/assets/79e2a7dd-21d2-491f-a27f-0612d3f17e97" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/186f2084-b55c-4b5b-9337-1da343407a57" />

**Output Timing Waveform**
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/115b6757-8e81-4616-84d5-2998b0f5b9f0" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/83b786dd-9050-4be7-9ead-547a915eb0f9" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



