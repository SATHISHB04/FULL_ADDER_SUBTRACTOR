# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

NAME:SATHISH.B

REG NO:24900077

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![WhatsApp Image 2024-12-02 at 20 51 04_2a81fe0d](https://github.com/user-attachments/assets/6e678baa-aa44-4b01-86d8-98ab7c8380db)
![WhatsApp Image 2024-12-02 at 20 51 05_adf3b166](https://github.com/user-attachments/assets/f84b8f9b-a9ea-40f5-af0f-17f1e415451f)


**Procedure**

Write the detailed procedure here

**Program:**
```
full adder module exp4( input a,b,c, output sum,carry);
 wire w1,w2,w3;
 assign sum=a^b^c; 
assign w1=a&b; 
assign w2=b&c; 
assign w3=c&a; 
assign carry=w1|w2|w3;
endmodule

full subtractor module experiment4(a,b,c,diff,borr); 
input a,b,c; 
output diff,borr;
 wire w1,w2,w3,w4,w5,w6; xor g1(diff,a,b,c);
 and g2(w4,w1,b); 
and g3(w5,w1,b); 
and g4(w6,b,c); 
or g5(borr,w4,w5,w6);
endmodule
```

**RTL Schematic**
![exp4](https://github.com/user-attachments/assets/5d92b8ce-94a2-421b-a5bc-ff08c16f44fc)
![exp4](https://github.com/user-attachments/assets/a412290a-2bc9-4612-ad54-0113fe215a4e)

**Output Timing Waveform**
![exp4 wave 1](https://github.com/user-attachments/assets/fce3f109-d354-46e6-ae57-a4dfde3a665f)
![exp4 wave 2](https://github.com/user-attachments/assets/2b45f553-e456-43ba-90b5-e7e6dfa28ca3)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



