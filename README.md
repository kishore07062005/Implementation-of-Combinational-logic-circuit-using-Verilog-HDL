NAME: KISHORE.M

REG NO: 2305002012

### Date: 15/10/2024 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![image](https://github.com/RahulM2005R/Implementation-of-Combinational-logic-circuit-using-Verilog-HDL/assets/166299886/56c66f4c-f544-4cf7-b670-0ad7f447face)
![image](https://github.com/RahulM2005R/Implementation-of-Combinational-logic-circuit-using-Verilog-HDL/assets/166299886/90b6b7aa-8089-4c59-a99c-7503c4882118)


## Truth Table:
![image](https://github.com/RahulM2005R/Implementation-of-Combinational-logic-circuit-using-Verilog-HDL/assets/166299886/d631d2c1-ae69-474d-b6fc-9e11f1b0d015)

## Program:
```verilog
module exp2a(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
```

## RTL Schematic:
![image](https://github.com/RahulMR2005/ex.2/assets/145525365/0f574b7b-dc36-4916-9a7d-09aa12fa9c49)


## Timing Diagram:
![image](https://github.com/RahulMR2005/ex.2/assets/145525365/88caa0b3-55b7-4659-aafa-f5c961679723)



## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



