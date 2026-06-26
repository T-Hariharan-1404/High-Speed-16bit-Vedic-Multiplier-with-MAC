# Source Code

This folder contains the Verilog HDL implementation of the **High-Speed 16-Bit Signed Vedic Multiplier with Multiply-Accumulate (MAC) Unit**.

## Files

| File | Description |
|------|-------------|
| carry_select_adder.v | Carry Select Adder used to accelerate addition operations in the multiplier and MAC architecture. |
| vedic4x4.v | 4×4 Vedic Multiplier implementing the Urdhva Tiryakbhyam algorithm. |
| vedic8x8.v | 8×8 Vedic Multiplier constructed using multiple 4×4 Vedic multiplier blocks. |
| vedic16x16_signed.v | Top-level 16-bit signed Vedic multiplier supporting both positive and negative operands. |
| mac16x16_vedic.v | Multiply-Accumulate (MAC) module integrating the signed Vedic multiplier with an accumulator. |
| top_vedic_mac_example.v | Example top-level module demonstrating the integration of the MAC architecture. |
| vedic_mac_fpga_top.v | FPGA top-level module for hardware implementation and synthesis. |
| tb_vedic_mac.v | Testbench used to verify the functionality of the multiplier and MAC unit. |

## Design Hierarchy

```
4×4 Vedic Multiplier
        │
        ▼
8×8 Vedic Multiplier
        │
        ▼
16×16 Signed Vedic Multiplier
        │
        ▼
Carry Select Adder
        │
        ▼
Multiply-Accumulate (MAC) Unit
        │
        ▼
FPGA Top Module
```

## Features

- Hierarchical Vedic multiplier design
- Signed 16-bit multiplication
- Carry Select Adder for faster addition
- Multiply-Accumulate (MAC) architecture
- Verilog HDL implementation
- FPGA/ASIC compatible
- Fully verified using ModelSim

## Simulation Steps

1. Compile all Verilog source files.
2. Compile `tb_vedic_mac.v`.
3. Run the simulation.
4. Observe the waveform and console outputs.
5. Verify multiplication and accumulation results.

## Supported Operations

- Positive × Positive
- Positive × Negative
- Negative × Positive
- Negative × Negative
- Continuous MAC operation
- Accumulator reset
