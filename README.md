# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
Half Adder
![Screenshot 2024-12-07 214919](https://github.com/user-attachments/assets/63dc2943-67dd-45ce-b90c-e4d181bb5ac5)

Half Subtractor
![Screenshot 2024-12-07 214929](https://github.com/user-attachments/assets/4d70af20-b67e-4e5d-b951-875967dd971f)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
Half Adder
module hadd(a,b,sum,cout);
input a,b;
output sum,cout;
xor g1(sum,a,b);
and g2(cout,a,b);
endmodule 

Half Subtractor
module hsub(a,b,sub,bout);
input a,b;
output sub,bout;
wire w1;
xor g1(sub,a,b);
not g2(w1,a);
and g3(bout,w1,b);
endmodule 

Developed by:Ravivarman vv
RegisterNumber:24006127

**RTL Schematic**
Half Adder
![Screenshot 2024-12-07 214944](https://github.com/user-attachments/assets/8d71d39e-e20a-43e8-836b-fb8b9fea2dd7)
Half Subtractor
![Screenshot 2024-12-07 214950](https://github.com/user-attachments/assets/cae3bc78-93dd-4151-bd12-5adacf226045)

**Output/TIMING Waveform**
Half Adder
![Screenshot 2024-12-07 215004](https://github.com/user-attachments/assets/1c2b05a8-3e84-4b59-b8dd-1d6fd4aa62c8)
Half Subtractor
![Screenshot 2024-12-07 215013](https://github.com/user-attachments/assets/ef143958-ebcb-47ae-8ac6-9690a97ecf76)

**Result:**
Thus the half adder and half subtractor circuits were successfully designed, and their truth tables were verified in Quartus using Verilog programming.
