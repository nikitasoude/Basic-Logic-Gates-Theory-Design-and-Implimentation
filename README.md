Basic Logic Gates - Theory, Design & Implementation**

### Concept Overview
Logic gates are the building blocks of digital circuits. They perform basic logical functions and are implemented using electronic switches like transistors.

### Types of Basic Logic Gates
1. **AND Gate**
   - **Output** = `A • B`
   - **Truth Table:**

| A | B | Y (A AND B) |
|:-:|:-:|:------------:|
| 0 | 0 |      0       |
| 0 | 1 |      0       |
| 1 | 0 |      0       |
| 1 | 1 |      1       |

2. **OR Gate**
   - **Output** = `A + B`
   - **Truth Table:**

| A | B | Y (A OR B) |
|:-:|:-:|:-----------:|
| 0 | 0 |      0      |
| 0 | 1 |      1      |
| 1 | 0 |      1      |
| 1 | 1 |      1      |

3. **NOT Gate (Inverter)**
   - **Output** = `~A`
   - **Truth Table:**

| A | Y (~A) |
|:-:|:-------:|
| 0 |    1    |
| 1 |    0    |

4. **NAND Gate**
   - **Output** = `~(A • B)`
   - **Truth Table:**

| A | B | Y (~(A AND B)) |
|:-:|:-:|:---------------:|
| 0 | 0 |        1        |
| 0 | 1 |        1        |
| 1 | 0 |        1        |
| 1 | 1 |        0        |

5. **NOR Gate**
   - **Output** = `~(A + B)`
   - **Truth Table:**

| A | B | Y (~(A OR B)) |
|:-:|:-:|:--------------:|
| 0 | 0 |        1       |
| 0 | 1 |        0       |
| 1 | 0 |        0       |
| 1 | 1 |        0       |

6. **XOR Gate**
   - **Output** = `A ⊕ B`
   - **Truth Table:**

| A | B | Y (A XOR B) |
|:-:|:-:|:-------------:|
| 0 | 0 |       0       |
| 0 | 1 |       1       |
| 1 | 0 |       1       |
| 1 | 1 |       0       |

### Example Verilog Code for Basic Logic Gates
```verilog
module logic_gates (
    input wire A, B,
    output wire AND_out, OR_out, NOT_out, NAND_out, NOR_out, XOR_out
);
    assign AND_out = A & B;
    assign OR_out  = A | B;
    assign NOT_out = ~A;
    assign NAND_out = ~(A & B);
    assign NOR_out  = ~(A | B);
    assign XOR_out  = A ^ B;
endmodule

// Testbench
module testbench;
    reg A, B;
    wire AND_out, OR_out, NOT_out, NAND_out, NOR_out, XOR_out;

    logic_gates uut (.A(A), .B(B), .AND_out(AND_out), .OR_out(OR_out), .NOT_out(NOT_out),
                     .NAND_out(NAND_out), .NOR_out(NOR_out), .XOR_out(XOR_out));

    initial begin
        $monitor("A=%b B=%b | AND=%b OR=%b NOT(A)=%b NAND=%b NOR=%b XOR=%b",
                  A, B, AND_out, OR_out, NOT_out, NAND_out, NOR_out, XOR_out);
        
        A = 0; B = 0; #10;
        A = 0; B = 1; #10;
        A = 1; B = 0; #10;
        A = 1; B = 1; #10;

        $finish;
    end
endmodule
```

### Code Explanation
- **`assign` Statements:** Implements logic gate operations.
- **`$monitor` Task:** Tracks all logic gate outputs in real-time.
- **Test Cases:** Ensures each gate behaves correctly according to the truth tables.

### Execution Steps
1. Copy the Verilog code into your simulator (e.g., ModelSim, Xilinx Vivado, etc.).
2. Compile and run the code.
3. Verify the output matches the expected truth table values.

### Real-World Example for Practice
- Design a **4-input XOR Gate** using only NAND gates.
