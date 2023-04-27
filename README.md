# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime

## Procedure:
1.Create a project with required entities. 
2.Create a module along with respective file name. 
3.Run the respective programs for the given boolean equations. 
4.Run the module and get the respective RTL outputs. 
5.Create university program(VWF) for getting timing diagram. 
6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: P NAVEEN KUMAR
RegisterNumber:  212222230092
*/
```
```
module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire  A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule		 
```
## RTL realization
## Output:
## RTL:
![image](https://user-images.githubusercontent.com/119401470/234773895-d1fa0479-72a9-4989-a9ac-7bffbc4f0894.png)
## Timing Diagram:
![image](https://user-images.githubusercontent.com/119401470/234774083-7b4b89c0-91c2-4f67-94fd-cca3ec8fbe11.png)

## Truth table:

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
