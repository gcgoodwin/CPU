

# 8-Bit CPU Project

Designing a complete 8-bit CPU from discrete MOSFET transistors and digital logic principles.

---

## Overview

This project explores computer architecture by designing a complete 8-bit processor from the transistor level upward. Rather than relying on pre-built processor cores, each subsystem is designed individually and integrated into a unified architecture.

The processor is designed to execute instructions, perform arithmetic and logical operations, store data in registers, manage program flow, and interface with memory. Every major subsystem is developed from fundamental digital logic building blocks and verified through simulation.

---

## CPU Architecture

### Arithmetic Logic Unit (ALU)

The Arithmetic Logic Unit performs all arithmetic and logical computations required by the processor.

| Opcode | Operation |
|----------|----------|
| 000 | Addition |
| 001 | Subtraction |
| 010 | Bitwise AND |
| 011 | Bitwise OR |
| 100 | Bitwise XOR |
| 101 | Bitwise NOT |
| 110 | Shift Left |
| 111 | Shift Right |

The ALU accepts two 8-bit operands and produces an 8-bit result along with status information such as carry-out.

### Register File

The register file provides high-speed storage for values currently being used by the processor. Registers allow data to be temporarily stored, modified, and transferred between subsystems without accessing external memory.

### Program Counter

The Program Counter stores the address of the next instruction to be executed. After each instruction completes, the Program Counter advances automatically unless modified by a branch or jump instruction.

### Instruction Register

The Instruction Register stores the instruction currently being executed, allowing the processor to decode and act upon it during the current clock cycle.

### Control Unit

The Control Unit coordinates processor activity by generating control signals for every subsystem. Responsibilities include instruction decoding, ALU operation selection, register management, memory access control, and program flow management.

### Clock System

A centralized clock synchronizes all processor operations. Each clock cycle advances the processor through the stages of instruction execution and ensures coordinated communication between subsystems.

### Memory Interface

The memory interface enables communication between the processor and external memory systems. This subsystem handles instruction fetching, data loading, and data storage.

---

## Arithmetic Logic Unit Design

The ALU is constructed from fundamental digital logic building blocks.

### Logic Gates

Implemented gates include:

- AND
- OR
- XOR
- NOT

### Half Adders

Half adders perform single-bit binary addition and generate a sum output and carry output.

### Full Adders

Full adders extend half adders by incorporating an incoming carry signal. Each full adder accepts two operand bits and a carry input, producing a sum output and carry output.

### Ripple-Carry Adder

Eight full adders are connected together to form an 8-bit ripple-carry adder. Carry signals propagate between stages, enabling multi-bit arithmetic operations.

### Adder/Subtractor

Subtraction is implemented using two's complement arithmetic. By conditionally inverting the second operand and injecting an initial carry, the same hardware performs both addition and subtraction.

### Multiplexer Network

An 8-to-1 multiplexer network selects the final ALU output. All operations are generated simultaneously, while the opcode determines which result is routed to the output bus.

---

## Example Instruction Execution

1. An instruction is fetched from memory.
2. The Program Counter advances.
3. The Instruction Register stores the instruction.
4. The Control Unit decodes the instruction.
5. Registers provide operands.
6. The ALU executes the requested operation.
7. The result is written back to a register or memory.
8. The next instruction begins execution.

---

## Features

- 8-bit processor architecture
- Custom Arithmetic Logic Unit
- Binary addition and subtraction
- Bitwise logic operations
- Shift operations
- Register-based storage
- Instruction decoding
- Memory interface architecture
- Clock-driven execution
- Modular subsystem design
- Transistor-level implementation
- LTspice simulation and verification

---

## Repository Structure

```text
.
├── README.md
├── docs/
│   ├── architecture/
│   ├── schematics/
│   └── screenshots/
│
├── ltspice/
│   ├── logic_gates/
│   ├── adders/
│   ├── multiplexers/
│   ├── registers/
│   └── cpu/
│
├── cad/ (In Progress)
│
├── journals/ (In Progress)
│
└── parts-list/ (In Progress)
```

## Technologies Used

- LTspice
- CMOS Logic Design
- Digital Logic Design
- Computer Architecture Principles
- GitHub

---

## Project Goal

The objective of this project is to demonstrate how a processor can be built from fundamental digital logic components, providing a complete view of computer architecture from transistors to instruction execution.

By designing and documenting each subsystem individually, this project aims to expose the mechanisms underlying modern computing while producing a complete CPU architecture that can be simulated, analyzed, and expanded.

---

## Author

**Goodwin Chen**

Summer 2026
