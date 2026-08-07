# BCD Adder using Verilog

## Overview

This project implements a Binary Coded Decimal (BCD) Adder using Verilog HDL.

A BCD adder adds two BCD digits and produces a valid BCD output.

If the binary sum exceeds 9, the circuit adds 6 (0110) to obtain the correct BCD result.

---

## Features

- Verilog implementation
- Testbench included
- Easy to simulate
- Suitable for FPGA/ASIC learning

---

## Truth

If

Binary Sum <= 9

Output = Binary Sum

Else

Output = Binary Sum + 6

Carry = 1

---

## Files

src/

- full_adder.v
- bcd_adder.v

testbench/

- bcd_adder_tb.v

simulation/

- waveform.png
- output.txt

---

## Simulation

Compile

```bash
iverilog -o bcd bcd_adder.v bcd_adder_tb.v
```

Run

```bash
vvp bcd
```

Generate waveform

```bash
gtkwave dump.vcd
```

---

## Sample Output

```
3 + 4 = 7

5 + 7 = 12 → 2 Carry 1

9 + 9 = 18 → 8 Carry 1

8 + 2 + 1 = 11 → 1 Carry 1
```

---

## Applications

- Digital Calculators
- Digital Clocks
- Embedded Systems
- FPGA Design
- Arithmetic Logic Units

---

