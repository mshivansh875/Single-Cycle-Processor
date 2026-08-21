# 🖥️ Single-Cycle Processor

> A SimpleRISC ISA implementation where each instruction executes in a single clock cycle.

## Overview

This project implements a **single-cycle processor** that executes one complete instruction per clock cycle. Unlike multi-cycle processors, this architecture prioritizes simplicity and uniform execution time at the cost of clock period efficiency.

The processor implements the **SimpleRISC ISA** (Instruction Set Architecture), a 32-bit reduced instruction set computer designed for educational purposes and hardware implementation.

## ✨ Features

| Feature | Details |
|---------|---------|
| **ISA Support** | SimpleRISC (21 operations) |
| **Registers** | 16 general-purpose registers |
| **Word Size** | 32 bits |
| **Execution Model** | Single-cycle execution |
| **Architecture Stages** | 5 pipeline stages |

## 🏗️ Architecture

The processor is built around a **5-stage pipeline architecture**:

1. **Instruction Fetch (IF)** - Retrieves instruction from memory
2. **Instruction Decode (ID)** - Decodes instruction and fetches operands
3. **Execution (EX)** - Performs ALU operations
4. **Memory Access (MEM)** - Reads/writes data from memory
5. **Write Back (WB)** - Writes results back to registers

In a single-cycle design, all stages complete within one clock cycle, ensuring deterministic timing at the cost of a lower clock frequency.

### Block Diagram

<img width="855" height="995" alt="Single Cycle Processor Architecture" src="https://github.com/user-attachments/assets/306811ac-6ce4-4c3b-b73e-b8225148d486" />

## 📊 SimpleRISC ISA Details

### Supported Operations (21 total)

- **Arithmetic**: ADD, SUB, MUL, DIV, MOD
- **Logical**: AND, OR, XOR, NOT
- **Shift**: SLL, SRL, SRA
- **Load/Store**: LW, SW
- **Branch**: BEQ, BNE, BGT, BLT, BLE, BGE
- **Others**: JMP, HALT

### Register File

- **16 general-purpose registers** (R0 - R15)
- Each register is **32 bits wide**
- R0 typically reserved as zero register (architecture-dependent)

## 🚀 Getting Started

### Prerequisites
- Hardware Description Language (HDL) simulator or synthesizer
- Verilog or VHDL knowledge
- Understanding of digital logic and computer architecture

### Implementation

[Add specific instructions for running simulations, synthesis, or testing here]

## 📁 Project Structure

```
Single-Cycle-Processor/
├── README.md              # This file
├── src/                   # Source files (Verilog/VHDL)
├── docs/                  # Detailed documentation
├── testbench/             # Test cases and simulations
└── circuits/              # Circuit diagrams and schematics
```

## 📚 Design Considerations

### Advantages
- ✅ Simple control logic
- ✅ Deterministic execution timing
- ✅ No pipeline hazards
- ✅ Easy to understand and implement

### Limitations
- ⚠️ Low clock frequency due to long critical path
- ⚠️ Inefficient hardware utilization
- ⚠️ Not suitable for high-performance applications

## 🔗 References

For detailed information about the architecture and implementation:
- See the **documentation** directory for comprehensive design details
- Review the **circuit diagrams** for a detailed view of each component
- Check the **testbench** directory for example programs

## 👤 Author

**Shivansh Mishra**  
GitHub: [@mshivansh875](https://github.com/mshivansh875)

---

**Note**: This is an educational project designed to demonstrate computer architecture principles. For production systems, consider multi-cycle or pipelined processor designs for better performance.
