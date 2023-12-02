# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime


## Theory:
A combinational circuit is a circuit in which the output depends on the present
combination of inputs. Combinational circuits are made up of logic gates. The output of
each logic gate is determined by its logic function. Combinational circuits can be made
using various logic gates, such as AND gates, OR gates, and NOT gates.

## Procedure : 

1.Create a project with required entities.

2.Create a module along with respective file name. 

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.


## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by: ANU RADHA .N

RegisterNumber:  23000217
*/

```
module clogic (a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1 , F2 ;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2 = (a&c&(~d));
assign A3 = ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5 = (b&(~c)&d);
assign F1 = A1|A2|A3|A4|A5;
assign B1 =(x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3 =(~w&x&y);
assign B4 = (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule

```
## RTL realization : 
![WhatsApp Image 2023-12-01 at 21 34 42_08672e1e](https://github.com/ANU23000217/Experiment--02-Implementation-of-combinational-logic-/assets/139117108/bc2e50f3-b9c4-497d-b349-87332ec182a4)

### Truth Table :
![Screenshot 2023-12-02 151714](https://github.com/ANU23000217/Experiment--02-Implementation-of-combinational-logic-/assets/139117108/44ba6d52-d2f8-4b03-aee5-98298b492de3)

![Screenshot 2023-12-02 151746](https://github.com/ANU23000217/Experiment--02-Implementation-of-combinational-logic-/assets/139117108/cbd32d50-ff69-4654-ade0-ac015bde2825)

## Timing Diagram:
![Screenshot 2023-12-02 183105](https://github.com/ANU23000217/Experiment--02-Implementation-of-combinational-logic-/assets/139117108/53e45217-cc9d-42eb-93d3-94f6961798d6)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
