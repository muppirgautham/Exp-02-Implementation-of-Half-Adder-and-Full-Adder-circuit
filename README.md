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
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: M G Gautham 
RegisterNumber:  212221230027
```
### output: 
```
HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Logic symbol & Truthtable:
![image](https://user-images.githubusercontent.com/94810884/196046080-1b0a5718-bac3-4ba9-82d5-5460a18bdf69.png)
![image](https://user-images.githubusercontent.com/94810884/196046102-840036e5-f08e-433c-9c2c-c3260b35ea5c.png)

### RTL realization:
![image](https://user-images.githubusercontent.com/94810884/196046120-e90bf458-2cba-42f1-8a37-35281ebf2992.png)

### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/94810884/196046151-57b6d30f-3584-4c09-9e18-b577c75087cf.png)

## Full Adder :

### Logic Symbol:
![image](https://user-images.githubusercontent.com/94810884/196046188-e04a73c3-5e34-40d4-884a-62eb7fc35bef.png)

### RTL:
![image](https://user-images.githubusercontent.com/94810884/196046204-66bbea45-650c-486a-83e8-1b2c7256b759.png)

### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/94810884/196046219-2916d640-94d7-4cb1-9d9a-cfc9e808933d.png)

### TRUTH TABLE :
![image](https://user-images.githubusercontent.com/94810884/196046234-d6ebf4da-37a5-492b-b39c-bde67372d642.png)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
