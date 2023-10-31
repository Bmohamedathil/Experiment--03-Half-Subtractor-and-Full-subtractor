# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

STEP 1: Use module project name(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule.


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: MOHAMED ATHIL B

RegisterNumber: 212222230081

### half subtractor:
```
module half(A,B,s,c);
input A,B;
output s,c;
assign s = A^B;
assign c = ~A&B;
endmodule
```
endmodule

### full subtractor:
```
module half(A,B,bin,diff,borrow);
input A,B,bin;
output diff,borrow;
assign diff = A^B^bin;
assign borrow = ~(A&B) | ~(A^B)&bin;
endmodule
```
## Output:

## Truthtable

### half subtractor

![ha](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/0ac1ac6a-1e5b-4b80-9246-a1026e0fb65e)

### full subtractor
![fu](https://github.com/Praveen0500/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120218611/36f561e9-0ea3-4dd8-8857-8b3e85710775)


##  RTL realization

### half subtractor 
![de 4 i)a](https://github.com/Bmohamedathil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119560261/9fdf9823-111c-4730-aac8-9d18b78f02fa)

### full subtractor
![de 4 ii) a](https://github.com/Bmohamedathil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119560261/805e9d93-04a0-4777-a6c6-cc9460db62b0)

## Timing diagram 

### half subtractor
![de 4 i)b](https://github.com/Bmohamedathil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119560261/20f3e6d4-e960-48b2-a744-7e0de2751006)


### full subtractor

![de 4 ii) b](https://github.com/Bmohamedathil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119560261/1d0c9e51-5756-4782-8119-ec40ae02c36b)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
