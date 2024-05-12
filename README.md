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



Figure -01 HALF ADDER
![half adder](https://github.com/ADARSH778/HALF_ADDER_SUBTRACTOR/assets/149347361/eae43133-3f41-4174-a9bb-4f3ef3a8c5ef)

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B



Figure -02 HALF Subtractor
![half subtractor](https://github.com/ADARSH778/HALF_ADDER_SUBTRACTOR/assets/149347361/2f37a0dd-1a1a-40f5-b931-3c07c1f561b8)

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Developed by: R Adarsh Chowdary
RegisterNumber:212223040166


half adder:
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
assign sum = a^b;
assign carry = a & b;
endmodule
```
half subtractor:
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; 
assign D = a ^ b;
assign Bo = ~a & b;
endmodule
```


Developed by: R Adarsh Chowdary
RegisterNumber:212223040166

**RTL Schematic**
Half adder:

![image](https://github.com/PranaveshSaikumar/HALF_ADDER_SUBTRACTOR/assets/151001393/95c2b59f-13df-4501-91d9-9dce22e9f7e4)

Half subtractor:

![image](https://github.com/PranaveshSaikumar/HALF_ADDER_SUBTRACTOR/assets/151001393/3855072b-5445-4094-b4ec-73bb651392ab)

**Output/TIMING Waveform**
Half adder:

![image](https://github.com/PranaveshSaikumar/HALF_ADDER_SUBTRACTOR/assets/151001393/ffffd5c1-3146-4180-b696-3f675a82d49c)

Half subtractor:

![image](https://github.com/PranaveshSaikumar/HALF_ADDER_SUBTRACTOR/assets/151001393/d482d1bf-0bdc-4854-b899-a716b106ac47)


**Result:**
Thus,the  half adder and half subtractor circuit and its truth table is verified in Quartus using Verilog programming.
