# High-Speed-16bit-Vedic-Multiplier-with-MAC-Unit

##  Overview

This project presents the design and implementation of a **16-Bit Signed Vedic Multiplier with a Multiply-Accumulate (MAC) Unit** using **Verilog HDL**. The multiplier is based on the **Urdhva Tiryakbhyam (Vertical and Crosswise)** algorithm from Vedic Mathematics, which enables fast and efficient multiplication by generating partial products in parallel.

The MAC unit combines multiplication and accumulation operations, making it suitable for high-speed arithmetic applications such as Digital Signal Processing (DSP), image processing, and embedded systems.

---

##  Features

- 16-Bit Signed Vedic Multiplier
- Multiply-Accumulate (MAC) Architecture
- Verilog HDL Implementation
- Supports Positive and Negative Numbers
- Accumulator Enable and Clear Functionality
- Comprehensive Testbench Verification
- FPGA/ASIC Compatible Design
- Efficient and High-Speed Arithmetic Operations

---

##  MAC Operation

The MAC unit performs the operation:

MAC = Accumulator + (A × B)

Where:

- **A** = 16-bit signed multiplicand
- **B** = 16-bit signed multiplier
- **Accumulator** stores the running sum of multiplication results
- **acc_en** enables accumulation
- **acc_clr** clears the accumulator

---

##  Test Cases

The following test cases were used to verify signed multiplication functionality.

| Test Case | Operand A | Operand B | Expected Result |
|------------|-----------|-----------|----------------|
| 1 | +25 | +15 | +375 |
| 2 | +12 | -8 | -96 |
| 3 | -20 | +10 | -200 |
| 4 | -5 | -4 | +20 |
| 5 | +10 | +10 | +100 |
| 6 | +5 | +5 | +25 |
| 7 | -2 | +6 | -12 |

### Testbench Inputs

```verilog
a = 16'd25; b = 16'd15; #20;
a = 16'd12; b = -16'd8; #20;
a = -16'd20; b = 16'd10; #20;
a = -16'd5; b = -16'd4; #20;
a = 16'd10; b = 16'd10; #20;
a = 16'd5; b = 16'd5; #20;
a = -16'd2; b = 16'd6; #20;
```

---

##  Accumulator Reset Verification

```verilog
acc_clr = 1;
#10;
acc_clr = 0;
#10;
```

This test verifies that the accumulator is properly cleared and resumes normal operation after reset.

---

##  Randomized Testing

To further validate the design, random input combinations were applied.

```verilog
repeat (4) begin
    a = $random;
    b = $random;
    #20;
end
```

Random testing helps ensure correct operation across a broad range of signed input values.

---

##  Simulation Procedure

1. Apply Reset
2. Enable Accumulation
3. Execute Fixed Test Cases
4. Verify Multiplication Results
5. Clear Accumulator
6. Perform Randomized Testing
7. Observe Outputs and Waveforms

---

##  Applications

- Digital Signal Processing (DSP)
- FIR Filters
- IIR Filters
- Image Processing
- Machine Learning Accelerators
- Embedded Arithmetic Units
- FPGA-Based Computing
- High-Speed VLSI Systems

---

##  Tools Used

- Verilog HDL
- ModelSim

---

##  Advantages of Vedic Multiplication

- Faster Multiplication
- Reduced Propagation Delay
- Parallel Partial Product Generation
- Efficient Hardware Utilization
- Scalable Architecture
- Suitable for High-Speed DSP Applications

---

##  Algorithm Used

### Urdhva Tiryakbhyam (Vertical and Crosswise)

The Urdhva Tiryakbhyam Sutra is a Vedic Mathematics technique that generates all partial products simultaneously, resulting in faster multiplication and improved hardware performance compared to conventional multiplication methods.

---
