# 8-Bit CPU Project

Building an 8-bit CPU from discrete NPN transistors to understand what is really happening beneath the code.

---

## Overview

I have used computers for years, but I wanted to understand what actually happens inside a processor when it adds numbers, stores data, or executes an instruction. This project is my attempt to answer that question by building an 8-bit CPU from the transistor level upward.

The long-term goal is to create a complete processor that can perform arithmetic and logic operations, store values in registers, execute instructions, manage program flow, and communicate with memory. Instead of treating the CPU as one enormous circuit, I am breaking it into smaller systems that I can design, simulate, build, test, and improve one at a time.

The first major build phase is an **8-bit adder/subtractor**. This circuit will form the arithmetic foundation of the future Arithmetic Logic Unit and will let me focus on reliable transistor-level logic, carry propagation, two's complement subtraction, wiring, and debugging before moving on to the rest of the CPU.

---

## Project Scope and Build Plan

This project is designed as a series of connected stages rather than a single all-at-once build.

### Phase 1: 8-Bit Adder/Subtractor

The first physical build will be an 8-bit circuit that can add or subtract two binary numbers. It will be created from smaller logic blocks, including gates, half adders, and full adders.

This phase will help me test the practical challenges of working with discrete NPN transistors, including signal reliability, fan-out, voltage levels, component layout, and troubleshooting a larger circuit.

### Future Phases: Complete 8-Bit CPU

After the adder/subtractor is working reliably, I plan to expand the project into a complete 8-bit CPU by developing and connecting the remaining subsystems:

- Arithmetic Logic Unit
- Register file
- Program Counter
- Instruction Register
- Control Unit
- Clock system
- Memory interface

Each subsystem will be developed and tested individually before being integrated into the final processor.

---

## Planned CPU Architecture

### Arithmetic Logic Unit (ALU)

The Arithmetic Logic Unit will handle the processor's arithmetic and logical operations. The 8-bit adder/subtractor built during the first phase will eventually become one of the central parts of this unit.

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

The completed ALU is planned to accept two 8-bit operands and produce an 8-bit result, along with status information such as carry-out.

### Register File

The register file will provide fast temporary storage for values currently being used by the processor. It will allow data to be stored, modified, and transferred between different parts of the CPU without constantly accessing external memory.

### Program Counter

The Program Counter will store the address of the next instruction to be executed. It will normally advance after each instruction, but branch or jump instructions will be able to replace its value.

### Instruction Register

The Instruction Register will hold the instruction currently being executed so that the Control Unit can decode it and coordinate the correct operation.

### Control Unit

The Control Unit will act as the coordinator of the CPU. It will generate the signals needed to select ALU operations, move data between registers, access memory, and control the order in which instructions are executed.

### Clock System

A centralized clock will keep the processor's operations synchronized. Each clock cycle will move the CPU through the steps required to fetch, decode, and execute an instruction.

### Memory Interface

The memory interface will allow the CPU to fetch instructions, load data, and store results in an external memory system.

---

## First Build: 8-Bit Adder/Subtractor

The first build is focused specifically on the arithmetic circuit that will later become part of the full ALU.

### Logic Gates

The circuit will be built from fundamental logic gates, including:

- AND
- OR
- XOR
- NOT

### Half Adders

A half adder adds two single binary bits and produces a sum bit and a carry bit. It is one of the simplest building blocks used to understand binary addition.

### Full Adders

A full adder expands on the half adder by including a carry input from the previous bit. Each full adder accepts two operand bits and a carry-in, then produces a sum and a carry-out.

### Ripple-Carry Adder

Eight full adders will be connected in sequence to create an 8-bit ripple-carry adder. The carry from each bit will feed into the next stage, allowing the circuit to add two complete 8-bit values.

### Subtraction with Two's Complement

The same circuit will also perform subtraction using two's complement. When subtraction mode is enabled, the second operand will be inverted and the initial carry-in will be set to 1. This allows the adder hardware to calculate both addition and subtraction without requiring a separate subtractor circuit.

### Testing and Verification

The circuit will first be tested through simulation and then built physically with discrete components. I plan to verify individual gates and adder stages before combining them into the complete 8-bit system. Documenting failures and design changes is an important part of the project because the debugging process is where much of the learning happens.

---

## How the Completed CPU Will Execute an Instruction

Once all of the planned subsystems are built and connected, an instruction cycle should follow this general process:

1. An instruction is fetched from memory.
2. The Program Counter advances.
3. The Instruction Register stores the instruction.
4. The Control Unit decodes the instruction.
5. Registers provide the required operands.
6. The ALU performs the requested operation.
7. The result is written back to a register or memory.
8. The CPU begins the next instruction.

---

## Planned Features

- 8-bit processor architecture
- Custom Arithmetic Logic Unit
- 8-bit addition and subtraction
- Bitwise logic operations
- Shift operations
- Register-based storage
- Instruction decoding
- Memory interface
- Clock-driven execution
- Modular subsystem design
- Discrete NPN transistor implementation
- LTspice simulation and verification
- Physical circuit construction and testing

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
├── cad/
│   └── 8-bit-adder/
│
├── journals/
│   └── Week-1-3-Journal/
│
└── parts-list/
    └── Cart-Parts/
```

---

## Technologies and Concepts

- LTspice
- Discrete NPN transistor logic
- Digital logic design
- Binary arithmetic
- Two's complement
- Computer architecture
- Circuit construction and debugging
- GitHub

---

## Why I Am Building This

The purpose of this project is not only to end with a working CPU. I want to understand how a computer can grow from individual transistors into gates, adders, registers, control signals, and eventually a machine capable of executing instructions.

Beginning with the 8-bit adder/subtractor gives me a realistic first milestone while still contributing directly to the larger CPU. By building each subsystem myself and documenting the problems I encounter, I hope to develop a much deeper understanding of both digital electronics and computer architecture than I could gain from studying diagrams alone.

---

## Author

**Goodwin Chen**

Summer 2026
