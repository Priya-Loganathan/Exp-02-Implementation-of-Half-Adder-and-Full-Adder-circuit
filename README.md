# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Theory
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

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: DELLI PRIYA L
RegisterNumber:  212222230029
```
HALF ADDER  
module halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

FULL ADDER  
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule 
```

### Logic symbol:
<img width="162" alt="210394807-f0abebca-ed18-4300-9533-c8be717bf3d1" src="https://user-images.githubusercontent.com/121166075/232668860-6b465388-17ae-4d48-9f9b-1d2766427f5d.png">  
<img width="145" alt="210394842-56ad9780-b0bf-4091-8330-58f7b0a9b1bb" src="https://user-images.githubusercontent.com/121166075/232668879-024f1fe1-6670-451d-bee6-0d50546e2a14.png">  
<img width="157" alt="210394854-0f7bebd5-084e-42a4-b621-a96ba502d937" src="https://user-images.githubusercontent.com/121166075/232668892-6eb482d7-596a-4f32-8aec-9cd5e5b44cf8.png">  

### Truth table:
![210396385-88c8d334-817f-438d-a83a-76ff5151a49a](https://user-images.githubusercontent.com/121166075/232669011-3bde16b4-2fa2-49a6-81de-9620ebbc054f.jpg)
![210396429-e8b265c9-05a8-4cc8-b3ed-e540335a6e7d](https://user-images.githubusercontent.com/121166075/232669056-21f3e799-a22b-4f43-8ea2-87ed13d58e66.jpg)

## Output:
### RTL Realization:
- HALF ADDER
![halfadder](https://user-images.githubusercontent.com/121166075/232669369-ce0fefff-a819-4efb-bd9b-c3e4df9e32cf.png)

- FULL ADDER
![fulladder](https://user-images.githubusercontent.com/121166075/232669443-e2c2e4fe-d558-4650-9d28-0973fed88a4e.png)

### Timing Diagram:
- HALF ADDER
![halfadder td](https://user-images.githubusercontent.com/121166075/232669622-3d6f7949-71f3-43c8-ba7b-a9a5d681657c.png)
- FULL ADDER
![fulladder td](https://user-images.githubusercontent.com/121166075/232669698-97d41d04-e46c-415f-84e8-7af3377c17ad.png)

### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
