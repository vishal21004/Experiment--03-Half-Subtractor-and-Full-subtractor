### Experiment--03-Half-Subtractor-and-Full-subtractor

### Implementation-of-Half-subtractor-and-Full-subtractor-circuit

### AIM:

To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:

Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

### Theory

Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

### Half Subtractor Full Subtractor

### Half Subtractor

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

### Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 

![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.

### Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.  
```
### Half Sub

module halfsub(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire X;
xor(Diff,A,B);
not(X,A);
and(Borrow,X,B);
endmodule

### Full Sub

module fullsub(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (~A &(B ^ C) | (B & C));
assign Borrow = ( A^B^C);
endmodule
```
*/

### Output:

### Truthtable

### Half Sub

![image](https://user-images.githubusercontent.com/120443233/230734229-35b06a7b-e45c-4558-8f4d-a59f61f5c1e5.png)

### Full Sub

![image](https://user-images.githubusercontent.com/120443233/230734259-4315eefc-142d-4dae-b9d2-998578ed2668.png)

### Logic Symbol

### Half Sub

![image](https://user-images.githubusercontent.com/120443233/230734297-77634bba-f9cd-417e-8717-105fa1cd0e3b.png)

### Full Sub

![image](https://user-images.githubusercontent.com/120443233/230734319-4354c080-42c2-4d7a-bf2f-8b60f8129931.png)

### RTL realization

### Half Sub

![image](https://user-images.githubusercontent.com/120443233/230734342-d04f848b-cb1e-46b0-bfd7-345a8807b734.png)

### Full Sub

![image](https://user-images.githubusercontent.com/120443233/230734364-7cf7da1f-623d-4ef5-9e5d-ef65c124c54e.png)

### Timing diagram 

### Half Sub

![image](https://user-images.githubusercontent.com/120443233/230734391-a6a14a09-7b87-43b8-9465-efb1a1c53fa3.png)

### Full Sub

![image](https://user-images.githubusercontent.com/120443233/230734406-e49391c2-ef94-4849-a1cb-5d4061c0b096.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

