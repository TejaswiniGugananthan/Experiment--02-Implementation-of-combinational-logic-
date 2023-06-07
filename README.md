### Implementation-of-combinational-logic
### AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
### Equipments Required:
  1.Hardware – PCs, Cyclone II , USB flasher.
  2.Software – Quartus prime.
### Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 
AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB
Y= A.B
OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation.
Y= A+B
### Procedure:
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the results.
### Program:
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Tejaswini.G
RegisterNumber:  212222230157
```python
module logic(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1=((~a)&(~b)&(~c)&(~d));
assign A2=(a&(~c)&(~d));
assign A3=((~b)&c&(~d));
assign A4=((~a)&b&c&d);
assign A5=(b&(~c)&d);
assign B1=(x&(~y)&z);
assign B2=((~x)&(~y)&z);
assign B3=((~w)&x&y);
assign B4=(w&(~x)&y);
assign B5=(w&x&y);
assign f1=A1|A2|A3|A4|A5;
assign f2=B1|B2|B3|B4|B5;
endmodule
```
### Output:
### RTL realization:
<img width="212" alt="de" src="https://user-images.githubusercontent.com/121222763/234528704-93e4551e-5074-42b5-a68a-7d25548037b1.png">
<img width="214" alt="de 1" src="https://user-images.githubusercontent.com/121222763/234528735-c992ff71-298e-4592-9ed0-8dfb648e321e.png">

### Timing Diagram:
<img width="758" alt="de 2" src="https://user-images.githubusercontent.com/121222763/234528822-09baa8c3-f2f7-4e3f-a707-becc072692e5.png">

### Truth table:

![WhatsApp Image 2023-04-26 at 14 07 45](https://user-images.githubusercontent.com/121222763/234522624-56fff42e-df4f-4b2a-a1a3-e662f6c1f132.jpg)
### Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
