## Name:Packiya Murugan R

## Register number:212223050034


# Experiment--03-Half-Subtractor-and-Full-subtractor

## Implementation-of-Half-subtractor-and-Full-subtractor-circuit

## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime

## Theory:

Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor:

## Half Subtractor:
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y Carry=X'Y

## Full Subtractor:

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 

![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure:

• Use module projname(input,output) to start the Verilog programmming.

• Assign inputs and outputs using the word input and output respectively.

• Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

• Use each output to represnt onre for differnce and the other for borrow.

• End the verilog program using keyword endmodule


## Program:
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
#### Half-subtractor:
module halfsubtractor(a,b,borrow,diff);

input a,b;

output borrow,diff;

assign borrow=~a&b;

assign diff=a^b;

endmodule

#### Full-subtractor:
module fullsubtractor(a,b,bin,borrow,diff);

input a,b,bin;

output diff,borrow;

assign diff=(a^b)^bin;

assign borrow=((~a)&&bin)||(b&&bin)||((~a)&&b);

endmodule

## Truthtable:

#### Half-subtractor:
![291188261-ba5ad1df-e16d-4eed-91da-f633ded2fe55](https://github.com/packiyamurugan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168087/22ce841c-30e7-422e-8027-8039a5caab1a)

#### Full-subtractor:
![291195119-a5114490-150f-4589-904d-da5d800233c1](https://github.com/packiyamurugan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168087/8281bc3d-53c7-4e4d-8bbc-5e4147e4317a)


##  RTL realization:

#### Half-subtractor:

![291188478-558d54fe-f071-4d43-be45-6474328f36e1](https://github.com/packiyamurugan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168087/573f8072-8d4c-46c6-933e-e9697506358b)


#### Full-subtracter:

![291195323-01c6c83c-f34f-4962-8aa0-22ce8395acbd](https://github.com/packiyamurugan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168087/2876a307-2dd9-4c83-bda4-2b84dca8de39)


## Timing diagram:

#### Half-subtractor:

![291188683-5c3ef1e8-e143-46e2-8bfb-6a87e00a7ee6](https://github.com/packiyamurugan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168087/8f2207cc-b533-4873-a502-693fa9a1128a)

#### Full-subtractor:

![291195552-be988c14-e5c8-4a3e-b5b8-079187ef387d](https://github.com/packiyamurugan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168087/3e741af4-5b72-46ba-bccc-9dd6d2e182d4)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
