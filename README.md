# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:

Half Adder :

module expotwo (a,b,sum,carry);

input a,b;

output sum,carry;

xor(sum,a,b); 

and(carry,a,b);

endmodule


Full Adder :

module expotwofull (a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = ((a^b)^c);

assign carry = ((a&b)|(b&c)|(c&a));

endmodule

/*

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: HARISH RAGAV S

RegisterNumber:  22008415

*/
Logic symbol & Truthtable
RTL realization

### Output:
### RTL

Half Adder

![1](https://user-images.githubusercontent.com/119345345/211158358-ea3e3d21-bbb5-45b0-bb6d-48367d255a8f.jpg)

Full Adder

![2](https://user-images.githubusercontent.com/119345345/211158372-4c6a6864-c0bd-480d-868e-d9130255b4c8.jpg)

### TIMING DIAGRAM

Half Adder

![Timing](https://user-images.githubusercontent.com/119345345/211159409-e5554666-534d-4c91-b1a5-d4df69925caa.jpg)


Full Adder

![Timing](https://user-images.githubusercontent.com/119345345/211159447-a62509cb-5e04-468e-bfee-7235324e780a.jpg)



### TRUTH TABLE

Half Adder

![image](https://user-images.githubusercontent.com/119345345/211159085-27b2a992-9306-48e4-8415-aa7c815abd90.png)

Full Adder

![image](https://user-images.githubusercontent.com/119345345/211159097-f9c0b529-741f-4730-a866-59f97468e075.png)



### Result:
Thus the half adder and full adder circuits are designed and the truth tables is verified using quartus software.



