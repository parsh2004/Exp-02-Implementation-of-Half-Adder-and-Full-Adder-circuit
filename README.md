# Exp-02 Implementation of Half Adder and Full Adder circuit

# Implementation of Half Adder and Full Adder circuit:

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### EQUIPMENT'S REQUIRED:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### HALF ADDER:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### FULL ADDER:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER:


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER: 

### PROCEDURE:

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### PROGRAM:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:Paarkavy B 
RegisterNumber:212221230072
*/
VERILOG PROGRAMMING FOR HALF ADDER:
 
module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

VERILOG PROGRAMMING FOR FULL ADDER: 

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

### OUTPUT:

### HALF ADDER:

### LOGIC SYMBOLS USED IN HALF ADDER:

![output](logic.png)

### RTL REALIZATION:

![output](RTL02.png)

### TIMING DIAGRAM:

![output](Timing02.png)

### TRUTH TABLE:

![output](Table02.png)

### FULL ADDER:

### LOGIC SYMBOLS USED IN FULL ADDER:

![Symbol](https://user-images.githubusercontent.com/93509383/166180445-ee76799f-4ec1-49a3-bca4-bfb18da5ba5e.png)





### RTL REALIZATION:

![output](realization02.png)

### TIMING DIAGRAM:

![Diagram](https://user-images.githubusercontent.com/93509383/166180248-4e5ed61e-b0d9-4dcf-b87f-738ae4665dc8.png)


### TRUTH TABLE:

![output](2.png)

### RESULT:
Hence, a Half adder and Full adder circuit is designed and its truth table is verified using Verilog Programming.
