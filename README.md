# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y
## PROGRAM
```
module full(output D,B,input x,y,z);
assign D = x^y;
assign B = (~x&y);
endmodule
```
## RTL
![RTL HALF](https://user-images.githubusercontent.com/94506182/192109865-592bad0e-af4e-40cb-8419-81ef86998cd7.jpeg)

## TIMING DIAGRAM
![HALF](https://user-images.githubusercontent.com/94506182/192109744-3ecd8923-59cb-41c5-8b96-dc1acd9a9639.jpeg)

## TRUTH TABLE
![half sub](https://user-images.githubusercontent.com/94506182/192109979-67a05886-01e5-42ce-98cf-d1d023c3ca35.jpeg)


##
## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/
~~~
module full(output D,B,input x,y,z);
assign D = x^y^z;
assign B = (~x&(y^z)|(yz));
endmodule
~~~

## Truthtable

![half sub](https://user-images.githubusercontent.com/94506182/192109998-a0feb81f-aef9-44f6-b84c-b26d4ab290f5.jpeg)


##  RTL realization
![FULL RTL](https://user-images.githubusercontent.com/94506182/192110100-983eddd9-6be6-4687-b2a0-d651e6158402.jpeg)


## Timing diagram 
![WAVE](https://user-images.githubusercontent.com/94506182/192110201-bf38d0c8-31a2-4856-9cd1-5e0449765ae0.jpeg)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
