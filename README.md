[README.md](https://github.com/user-attachments/files/32875858/README.md)
<div align="center">

# Dharanidharan Ravikumar

**Building an understanding of computer architecture — one instruction at a time.**

`RISC-V` · `Computer Architecture` · `Instruction Set Design` · `Systems Programming` · `C`

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dharani-dharan-r-)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/DharanidharanRavikumar)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:dharanidharanravikumar@gmail.com)

</div>

---

## About

I'm a **BSc Computer Technology** graduate currently pursuing a **Master's in Smart Convergence Systems Engineering** at **Dong-A University**, South Korea.

My core interest is in **RISC-V ISA and computer architecture** — not as abstract theory, but as something I can build, test, and observe. I learn architecture by implementing systems that make the underlying hardware behavior visible and measurable.

I am not a generic application developer. I am specifically interested in understanding **how software interacts with processor architecture** — instruction encoding, pipeline behavior, memory hierarchy, and eventually vector extensions and compiler backends.

> *"I learn computer architecture by building systems that make the architecture observable."*

---

## Current Focus

```
RISC-V ISA & RV32I          ████████████████████  Active
Instruction Encoding         ████████████████████  Active
C / Systems Programming      ████████████████░░░░  Building
RISC-V Assembly              ████████████████░░░░  Building
CPU Pipelines                ████████████░░░░░░░░  Exploring
Memory Hierarchy & Cache     ████████░░░░░░░░░░░░  Exploring
```

### What I'm Working With

| Domain | Topics |
| :--- | :--- |
| **ISA** | RV32I instructions, instruction formats, encoding/decoding, immediate reconstruction, sign extension |
| **Architecture** | Registers, PC, SP, RA, caller/callee-saved conventions, stack frames, privilege levels |
| **Assembly** | RISC-V assembly, C-to-assembly mapping, machine code analysis |
| **Pipelines** | Fetch-decode-execute, pipeline stages, hazard concepts, forwarding/stall concepts |
| **Memory** | Memory hierarchy, cache concepts, virtual memory / TLB / MMU (exploring) |

---

## Selected Projects

### RISC-V RV32I Instruction Simulator

A standalone CPU instruction simulator built from scratch in C. Implements the full fetch → decode → execute cycle for RV32I instructions using match/mask-style decoding against real RISC-V machine code.

**Supports:** `ADD` `SUB` `ADDI` `LW` `SW` `BEQ` `JAL` `JALR` `LUI` and more

**Key learnings:**
- Debugged a JALR decoding issue caused by an incorrect match constant
- Investigated LUI + ADDI sign-extension behavior when constructing 32-bit constants
- Tested against machine code generated with the RISC-V GNU toolchain

[![Repo](https://img.shields.io/badge/Repository-riscv--simulator-181717?style=flat&logo=github)](https://github.com/DharanidharanRavikumar/riscv-simulator)

---

### RISC-V RV32I Instruction Decoder

A dedicated instruction decoder module that isolates the decoding stage from execution. Takes raw 32-bit hexadecimal machine instructions and extracts all architectural fields — opcode, rd, rs1, rs2, funct3, funct7, immediates, and shift amounts — across all six RV32I instruction formats.

**Handles:** `R-type` `I-type` `S-type` `B-type` `U-type` `J-type`

**Key concepts explored:**
- Split immediate reconstruction across non-contiguous bit fields
- Sign extension for branch and jump offsets
- Shift instruction discrimination via funct7
- Complete opcode → funct3 → funct7 decoding hierarchy

[![Repo](https://img.shields.io/badge/Repository-riscv--decoder-181717?style=flat&logo=github)](https://github.com/DharanidharanRavikumar/riscv-decoder)

---

## Roadmap

My learning path is intentionally sequential — each stage builds on verified understanding from the previous one.

```
  ┌─────────────────────────────────┐
  │  RISC-V ISA & RV32I            │  ✓ Foundation
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Instruction Encoding/Decoding  │  ✓ Completed
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  CPU Datapath & Pipelining     │  ← Current
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Pipeline Hazards & Forwarding │
  │  Stalls · Branch Handling      │
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Pipeline Performance Analysis │
  │  CPI · IPC · Branch Behavior   │
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Cache & Memory Hierarchy      │
  │  Locality · Replacement Policy  │
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Virtual Memory / TLB / MMU    │
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  RVV (Vector Extension)        │
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Compiler Fundamentals         │
  │  LLVM / RISC-V Backend         │
  └────────────┬────────────────────┘
               ▼
  ┌─────────────────────────────────┐
  │  Open-Source Contributions     │
  │  Research / PhD                │
  └─────────────────────────────────┘
```

### Future Projects (Planned)

| Project | Focus Area |
| :--- | :--- |
| Pipeline Simulator | 5-stage pipeline, data/control hazards, forwarding paths |
| Pipeline Hazard Analyzer | Hazard detection, stall insertion, CPI impact analysis |
| Cache Analyzer | Cache hit/miss behavior, locality patterns, replacement policies |
| Virtual Memory Explorer | TLB simulation, page table walks, address translation |
| Performance Explorer | Instruction-level performance, IPC analysis, branch prediction |

---

## Skills

| Category | |
| :--- | :--- |
| **Architecture** | RISC-V ISA · RV32I · Instruction Encoding · CPU Pipeline Concepts · Memory Hierarchy · Cache Concepts |
| **Systems** | C · RISC-V Assembly · Machine Code · ELF / Toolchain · Git / GitHub |
| **Exploring** | RVV · Compiler Architecture · LLVM · Performance Analysis · Open-Source Contribution |

---

## Research Interests

- RISC-V architecture and instruction set design
- CPU microarchitecture and pipeline behavior
- Memory hierarchy and cache optimization
- Performance analysis at the instruction level
- Vector architectures (RVV)
- Compiler architecture and RISC-V backend (LLVM)
- Open-source processor and software ecosystems

I am building toward research-level work in these areas. My current projects are part of a deliberate effort to develop the implementation-level understanding required for meaningful contributions to architecture research.

---

<div align="center">

**Currently studying at Dong-A University, South Korea**

Master's in Smart Convergence Systems Engineering

![Profile Views](https://komarev.com/ghpvc/?username=DharanidharanRavikumar&color=333333&style=flat&label=Profile+Views)

</div>
