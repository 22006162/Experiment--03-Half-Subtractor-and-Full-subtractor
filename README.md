Experiment--03-Half-Subtractor-and-Full-subtractor
Implementation-of-Half-subtractor-and-Full-subtractor-circuit
AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

Half Subtractor Full Subtractor
Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

Procedure



Write the detailed procedure here 


Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule

Developed by: Harzhita S P
RegisterNumber:  22006162

LOGIC GATES:

![Screenshot (4)](https://user-images.githubusercontent.com/123094490/214295596-316ef95f-8d74-4808-abdd-1a176d2ec35e.png)

OUTPUT RIT REALIZATION:

HALF SUBTRACTOR:

![Screenshot (5)](https://user-images.githubusercontent.com/123094490/214295673-1f7b5d76-b3db-4373-87cc-f2a147125697.png)

FULL SUBTRACTOR:

![Screenshot (6)](https://user-images.githubusercontent.com/123094490/214295710-466617d1-28d5-4992-b05a-9673acae5608.png)

TIMING DIAGRAM :
HALF SUBTRACTOR:

![Screenshot (7)](https://user-images.githubusercontent.com/123094490/214295785-521b0e00-4621-4ddf-88f4-7782cd03ba0e.png)

FULL SUBTRACTOR:

![Screenshot (8)](https://user-images.githubusercontent.com/123094490/214295800-4f9c6758-00ed-435d-853d-4e2334c019d2.png)

Truth table:

HALF SUBRACTOR:

![Screenshot (9)](https://user-images.githubusercontent.com/123094490/214298765-ce6aa3c0-a8af-4600-adf1-471d0c91e072.png)



FULL SUBTRACTOR:
![Screenshot (10)](https://user-images.githubusercontent.com/123094490/214296973-20fa28e8-1d0b-4abe-937f-a67741346ac4.png)


Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
