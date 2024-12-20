### Name : YESWANTH PEDDEPI
### REG NO : 24010970
### EXP NO 4 : FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

### AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

### EQUIPMENTS REQUIRED :

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

### FULL ADDER AND FULL SUBSTRACTOR : 

### FULL ADDER : 

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

### FIGURE-1 FULL ADDER :

### FULL SUBSTRACTOR : 

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

### TRUTHTABLE :

 Full Adder
 
![Screenshot 2024-12-20 142401](https://github.com/user-attachments/assets/b067686c-ad1d-45ed-964c-653403209039)

 Full Substractor
 
![Screenshot 2024-12-20 142412](https://github.com/user-attachments/assets/9041ffa6-a837-4ca6-b952-e4e4870f022c)

### PROCEDURE :

 Full Adder:
 
 1.Open Quartus II and create a new project. 2.Use schematic design entry to draw the full adder circuit. 3.The
 circuit consists of XOR, AND, and OR gates. 4.Compile the design, verify its functionality through simulation.
 5.Implement the design on the target device and program it.
 
 Full Subtractor:
 
 1.Follow the same steps as for the full adder. 2.Draw the full subtractor circuit using schematic design. 3.The
 circuit includes XOR, AND, OR gates to perform subtraction. 4.Compile, simulate, implement, and program
 the design similarly to the full adder.

### PROGRAM :
### Full Adder
 module fulladd_top(a,b,cin,sum,carry); input a,b,cin; output sum,carry; wire w1,w2,w3,w4;
 xor(w1,a,b); xor(sum,w1,cin);
 and(w2,a,b); and(w3,b,cin); and(w4,cin,a);
 or(carry,w2,w3,w4); endmodule
### Full Subtractor
 
 module fullsub_top(a,b,Bin,BO,DIFF); input a,b,Bin; output BO,DIFF; assign DIFF = a ^ b ^ Bin; assign BO = (a
 & b) | ((a ^ b) & Bin); endmodule


### RTL SCHEMATIC :
![Screenshot 2024-12-20 142421](https://github.com/user-attachments/assets/57058039-ee8e-41aa-ba8b-47513716b01a)

### OUTPUT TIMING WAVEFORM :
Full Adder

![Screenshot 2024-12-20 142428](https://github.com/user-attachments/assets/f3211dda-8f95-48eb-b968-af0e58b2249e)

Full Substractor

![Screenshot 2024-12-20 142437](https://github.com/user-attachments/assets/d078f765-a2ec-41d4-abdd-b49d820b8e70)

### RESULT :

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



