<div align="center">

# ⚡ SIMPLIFIED RISC PROCESSOR USING VERILOG HDL ⚡

### Instruction Fetch • Instruction Decode • ALU • Register File • Memory Access • Functional Verification

<br>

## 🚀 My Third VLSI RTL Design Project

### Designed, Simulated & Verified by

# 👩‍💻 SHAIK ZAIBA FARAAZ

**B.Tech – Electronics & Communication Engineering**

*Aspiring VLSI | RTL Design | Digital Electronics | Verilog HDL*

---

### ⚙️ BUILD • SIMULATE • VERIFY • ANALYZE • LEARN ⚙️

</div>

---

# 📌 Project Overview

This project implements a **simplified RISC (Reduced Instruction Set Computer) Processor** using **Verilog HDL**.

The processor demonstrates the fundamental stages of a processor datapath:

- Instruction Fetch
- Instruction Decode
- Register File Access
- ALU Execution
- Memory Access
- Result Verification

The processor executes basic arithmetic, logical, and memory instructions and was verified using a **self-checking testbench with automatic PASS/FAIL verification**.

---

# 📊 Project Status

| Item | Status |
|---|---|
| Processor RTL Design | ✅ Completed |
| Instruction Fetch | ✅ Completed |
| Instruction Decode | ✅ Completed |
| Program Counter | ✅ Completed |
| Register File | ✅ Completed |
| ADD Operation | ✅ Verified |
| SUB Operation | ✅ Verified |
| AND Operation | ✅ Verified |
| OR Operation | ✅ Verified |
| STORE Operation | ✅ Verified |
| LOAD Operation | ✅ Verified |
| Functional Testbench | ✅ Completed |
| Automatic PASS/FAIL Verification | ✅ Completed |
| VCD Waveform Generation | ✅ Completed |
| EPWave Analysis | ✅ Completed |
| Functional Tests | ✅ 7/7 Passed |
| Failed Tests | ✅ 0 |
| GitHub Documentation | 🚀 Completed |

---

# 📖 1. Introduction

A **RISC Processor** is a processor architecture designed around a relatively simple instruction set.

A processor generally performs several important tasks:

1. Fetch an instruction from instruction memory.
2. Decode the instruction.
3. Read the required operands.
4. Perform an arithmetic or logical operation.
5. Access memory when required.
6. Store or update the result.
7. Move to the next instruction.

In this project, these fundamental concepts are implemented in a **simplified processor architecture using Verilog HDL**.

The processor supports basic instructions for:

- Addition
- Subtraction
- Bitwise AND
- Bitwise OR
- Memory Store
- Memory Load

The complete design was simulated and verified using a functional testbench.

---

# 🎯 2. Problem Statement

Design and simulate a **Simplified RISC Processor using Verilog HDL** capable of executing basic arithmetic, logical, and memory instructions.

The processor must include:

- Instruction Fetch Unit
- Program Counter
- Instruction Decode Logic
- ALU
- Register File
- Memory Access
- Arithmetic Operations
- Logical Operations
- Load/Store Operations
- Functional Testbench
- Automatic PASS/FAIL Verification
- VCD Waveform Generation
- Waveform Analysis

---

# 🎯 3. Project Objectives

The main objectives of this project are:

- To understand the basic architecture of a processor.
- To implement an instruction fetch mechanism.
- To design a Program Counter.
- To decode processor instructions.
- To implement a basic register file.
- To perform arithmetic operations using an ALU.
- To perform logical operations using an ALU.
- To implement basic memory access.
- To understand LOAD and STORE operations.
- To develop a complete functional testbench.
- To automatically compare expected and actual outputs.
- To generate simulation waveforms.
- To analyze processor execution using EPWave.
- To document the complete RTL design and verification flow.

---

# ⚙️ 4. Design Specifications

| Parameter | Specification |
|---|---|
| Design | Simplified RISC Processor |
| Architecture Type | Simplified Single-Cycle Processor |
| HDL | Verilog/SystemVerilog |
| Program Counter | 4-bit |
| Instruction Width | 16-bit |
| Opcode Width | 4-bit |
| ALU Result Width | 8-bit |
| Arithmetic Operations | ADD, SUB |
| Logical Operations | AND, OR |
| Memory Operations | LOAD, STORE |
| Register Storage | Register File |
| Memory Access | Data Memory |
| Simulator | Icarus Verilog |
| Online Environment | EDA Playground |
| Waveform Format | VCD |
| Waveform Viewer | EPWave |
| Verification Method | Self-Checking Testbench |
| Total Functional Tests | 7 |
| Passed Tests | 7 |
| Failed Tests | 0 |

---

# 🏗️ 5. Processor Architecture

The simplified processor consists of the following major blocks:

```text
                           ┌─────────────────┐
                           │ PROGRAM COUNTER │
                           │       PC        │
                           └────────┬────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │   INSTRUCTION   │
                           │     MEMORY      │
                           └────────┬────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │   INSTRUCTION   │
                           │     FETCH       │
                           └────────┬────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │   INSTRUCTION   │
                           │     DECODE      │
                           └────────┬────────┘
                                    │
                   ┌────────────────┴────────────────┐
                   │                                 │
                   ▼                                 ▼
          ┌─────────────────┐                ┌─────────────────┐
          │  REGISTER FILE  │                │ CONTROL / OPCODE│
          │                 │                │     DECODE      │
          └────────┬────────┘                └────────┬────────┘
                   │                                  │
                   └────────────────┬─────────────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │       ALU       │
                           │ ADD / SUB / AND │
                           │       / OR      │
                           └────────┬────────┘
                                    │
                     ┌──────────────┴──────────────┐
                     │                             │
                     ▼                             ▼
              ┌─────────────┐               ┌─────────────┐
              │ REGISTER    │               │ DATA MEMORY │
              │ WRITE BACK  │               │ LOAD/STORE  │
              └─────────────┘               └─────────────┘
---

# 🌊 6. Processor Execution & Waveform Overview

The processor was simulated and its internal signals were observed using a VCD waveform.

The waveform demonstrates the complete execution flow of the processor, including:

- Clock synchronization
- Reset initialization
- Program Counter progression
- Instruction fetching
- Opcode decoding
- ALU execution
- Automatic verification

## 📡 Key Output Signals

```text
┌──────────────────────────────────────────────────────────────────────┐
│                 SIMPLIFIED RISC PROCESSOR OUTPUT                    │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  clk          ──► Synchronizes processor execution                  │
│                                                                      │
│  reset        ──► Initializes the processor                          │
│                                                                      │
│  PC           ──► 0 → 1 → 2 → 3 → 4 → 5 → 6 → 7                    │
│                                                                      │
│  instruction  ──► Fetches a new 16-bit instruction                  │
│                                                                      │
│  opcode       ──► ADD → SUB → AND → OR → STORE → LOAD               │
│                                                                      │
│  alu_result   ──► Displays arithmetic/logical execution result      │
│                                                                      │
│  total_tests  ──► Counts executed verification tests                │
│                                                                      │
│  passed_tests ──► 0 → 1 → 2 → 3 → 4 → 5 → 6 → 7                    │
│                                                                      │
│  failed_tests ──► 0 throughout simulation                           │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
TIME ───────────────────────────────────────────────────────────────────►

CLK       __|‾|__|‾|__|‾|__|‾|__|‾|__|‾|__|‾|__

RESET     ‾‾‾‾‾‾‾‾|_________________________________

PC        0──────1──────2──────3──────4──────5──────6──────7

FETCH        INST1  INST2  INST3  INST4  INST5  INST6

OPCODE        ADD    SUB    AND    OR   STORE   LOAD

ALU RESULT      ✓      ✓      ✓      ✓      ─      ✓

TOTAL TESTS  0──────1──────2──────3──────4──────5──────6──────7

PASSED       0──────1──────2──────3──────4──────5──────6──────7

FAILED       0──────────────────────────────────────────────────────0
                 ┌──────────────┐
                 │    START     │
                 └──────┬───────┘
                        │
                        ▼
                 ┌──────────────┐
                 │    RESET     │
                 └──────┬───────┘
                        │
                        ▼
                 ┌──────────────┐
                 │ FETCH        │
                 │ INSTRUCTION  │
                 └──────┬───────┘
                        │
                        ▼
                 ┌──────────────┐
                 │ DECODE       │
                 │ OPCODE       │
                 └──────┬───────┘
                        │
                        ▼
              ┌─────────────────────┐
              │ READ REGISTER DATA  │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │ EXECUTE INSTRUCTION │
              └──────────┬──────────┘
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
        ADD/SUB        AND/OR       LOAD/STORE
          │              │              │
          └──────────────┼──────────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ UPDATE RESULT / │
                │ MEMORY          │
                └────────┬────────┘
                         │
                         ▼
                   PC = PC + 1
                         │
                         ▼
                   NEXT INSTRUCTION
=====================================
         VERIFICATION SUMMARY
=====================================
TOTAL TESTS : 7
PASSED      : 7
FAILED      : 0
RESULT      : ALL TESTS PASSED
=====================================
# 🔢 9. Instruction Set

| Opcode | Instruction | Category | Operation |
|---|---|---|---|
| `0000` | ADD | Arithmetic | `A + B` |
| `0001` | SUB | Arithmetic | `A - B` |
| `0010` | AND | Logical | `A & B` |
| `0011` | OR | Logical | `A \| B` |
| `0100` | LOAD | Memory | Read from Memory |
| `0101` | STORE | Memory | Write to Memory |

Instruction
     │
     ▼
┌──────────────┐
│    FETCH     │
└──────┬───────┘
       ▼
┌──────────────┐
│    DECODE    │
└──────┬───────┘
       ▼
┌──────────────┐
│ REGISTER READ│
└──────┬───────┘
       ▼
┌──────────────┐
│   EXECUTE    │
└──────┬───────┘
       ▼
┌──────────────┐
│ WRITE BACK / │
│ MEMORY ACCESS│
└──────────────┘

