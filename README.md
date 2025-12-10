AIM:
To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.
Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.
 
Diff = A ⊕ B ⊕ Bin
Borrow out = A'Bin + A'B + BBin
Program:
```
module FullSub (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule

```
Developed by: V Karthi  RegisterNumber: 25017522
RTL Schematic:
[FullSub RTL.pdf](https://github.com/user-attachments/files/24074391/FullSub.RTL.pdf)

Output Timing Waveform:
[FullSub wave.pdf](https://github.com/user-attachments/files/24074395/FullSub.wave.pdf)

Result: Thus, the Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

