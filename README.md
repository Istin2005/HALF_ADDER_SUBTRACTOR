# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit
```
Developed by: ISTIN B
RegisterNumber: 212223040068
```

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
![DE E-3 truthtable](https://github.com/04Varsha/HALF_ADDER_SUBTRACTOR/assets/149035374/c06bba9c-9c1e-4e92-a1e3-869583ce44c7)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
~~~
*Half_adder*
module halfadd(a,b,s,c);
input a,b;
output s,c;
xor(s,a,b);
and(c,a,b);
endmodule

*Half_subtractor*
module halfsub(diff,borrow,a,b);
output diff,borrow;
input a,b;
wire w1;
xor(diff,a,b);
not(w1,a);
and(borrow,w1,b);
endmodule

~~~


**RTL Schematic**

##halfadder
![Screenshot 2024-10-17 112813](https://github.com/user-attachments/assets/6baeae11-089c-4cac-8b2c-9a586f085c44)

##halfsubtractor
![halfsub](https://github.com/user-attachments/assets/bdfc0d17-4c60-4cf7-b770-8e9c1d3afe29)




**Output/TIMING Waveform**

HALF ADDER:

![Screenshot 2024-10-17 112841](https://github.com/user-attachments/assets/b1789a35-83c9-4ede-8539-03f346873adb)


HALF SUTRACTOR:

![halfsub2](https://github.com/user-attachments/assets/de8fa602-d80c-43cd-8a30-efc647a3911a)



**Result:**
The code is excecuted successfully.
