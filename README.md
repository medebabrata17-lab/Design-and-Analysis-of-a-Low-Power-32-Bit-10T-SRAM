
# Design and Analysis of a Low-Power 32-bit 10T SRAM Cell

## Overview

This project presents the design, simulation, analysis, and physical layout implementation of a low-power 32-bit 10T SRAM architecture for performance-critical applications.

The proposed SRAM cell addresses key limitations of conventional 6T SRAM, particularly read disturbance, reduced Static Noise Margin (SNM), leakage power, and reliability at reduced supply voltages.

The design was implemented and evaluated using Cadence Virtuoso with the GPDK180 180 nm CMOS process technology.

---

## Objectives

- Design a low-power 10T SRAM cell with improved read stability.
- Reduce static and dynamic power consumption.
- Improve Static Noise Margin (SNM).
- Eliminate read disturbance by isolating the storage nodes during read operations.
- Verify SRAM functionality through transistor-level simulations.
- Implement a 1×32-bit SRAM array using hierarchical cell instantiation.
- Develop the physical layout of the SRAM cell.
- Analyze power, stability, delay, and area characteristics.

---

## Proposed 10T SRAM Architecture

The proposed SRAM cell consists of three major functional blocks:

### 1. Bistable Storage Latch

Four transistors form two cross-coupled CMOS inverters that store the binary data.

### 2. Write Access Path

Two NMOS access transistors connect the storage nodes to the write bit lines BL and BLB during write operations.

### 3. Dedicated Read Buffer

Four additional transistors implement an isolated read path using transmission-gate-based circuitry.

The dedicated read path prevents direct disturbance of the internal storage nodes during read operations.

---

## Key Features

- 10-transistor SRAM architecture
- Dedicated read path
- Read/write path isolation
- Improved read Static Noise Margin
- Reduced read power
- Low-power operation
- 1×32-bit word-organized array
- Transistor-level schematic implementation
- Physical layout implementation
- Cadence Virtuoso based simulation and analysis
- GPDK180 180 nm CMOS technology

---

## Design Flow

The project followed the following VLSI design flow:

1. SRAM architecture study
2. Literature survey
3. 10T cell topology design
4. Transistor-level schematic implementation
5. Testbench development
6. Transient simulation
7. DC analysis
8. Static Noise Margin characterization
9. Power analysis
10. 32-bit array implementation
11. Physical layout design
12. Area analysis
13. Performance evaluation

---

## Tools and Technologies

| Category | Tools / Technology |
|---|---|
| EDA Tool | Cadence Virtuoso |
| Simulator | Spectre |
| Process Technology | GPDK180 |
| Technology Node | 180 nm CMOS |
| Design | 10T SRAM |
| Array | 1×32-bit |
| Analysis | Transient, DC, SNM, Power |
| Physical Design | Cadence Virtuoso Layout |

---

## Results

The implemented SRAM cell was evaluated for functionality, stability, power consumption, and physical area.

### Static Noise Margin

The simulated butterfly curve produced an SNM of approximately:

**0.52 V**

for a 1.8 V supply.

The read SNM remains close to the hold SNM due to the isolated read architecture.

### Power Consumption

The measured average power consumption was approximately:

**116.1 pW**

across the simulated operational sequence.

The dedicated read path reduces unnecessary switching on the high-capacitance write bit lines during read operations.

### Physical Area

The implemented cell has approximate dimensions of:

**13.75 µm × 31.25 µm**

The additional transistors required by the 10T architecture introduce an area overhead compared with conventional 6T SRAM.

### 32-bit Array

The verified single-bit SRAM cell was hierarchically instantiated to construct a:

**1 × 32-bit SRAM array**

The array was verified for multi-bit write and read operations.

---

## Applications

The proposed architecture can be considered for applications where memory stability and energy efficiency are important, including:

- Processor cache memories
- Register files
- Embedded SoCs
- Instruction buffers
- Low-power IoT systems
- Automotive electronics
- Performance-critical memory subsystems

---

## Project Publication

A research paper based on this work was presented/published at:

**International Conference on Digital Technology and Engineering (ICDTE), Bangalore, India, 2025**

Paper:

> "A comparative analysis of 6T, 8T, and 10T SRAM cells: performance evaluation and robustness assessment proving 10T superiority"

Authors:

- Shriya Gomes
- Arkaprova Mitra
- Debabrata Paul
- Rupam Maiti
- N. S. Desai

---

## Project Team

**Arkaprova Mitra**  
Electronics & Communication Engineering  
R V Institute of Technology and Management, Bengaluru

**Team Members**
- Shriya Gomes
- Debabrata Paul
- Rupam Maiti

**Project Guide**
- Mrs. Nivedita S Desai
- Assistant Professor, Department of ECE, RVITM

---

## Future Scope

Future development of the project can include:

- Integration of sense amplifiers and write drivers
- Decoder and pre-charge circuit design
- Memory compiler development
- Alternative read-buffer architectures
- Current-mode and Schmitt-trigger-based sensing
- Multi-port SRAM extensions
- Write-assist techniques
- Radiation-tolerant SRAM designs
- Security-oriented SRAM and PUF applications
- Larger memory array implementation

---

## Repository Contents

```text
├── README.md
├── Report/
│   └── Final_Major_Project_Report.pdf
├── Results/
│   ├── 10T_SRAM_Cell_Schematic.png
│   ├── Testbench.png
│   ├── Transient_Analysis.png
│   ├── Butterfly_Curve_SNM.png
│   ├── 32_Bit_SRAM_Array.png
│   └── Layout.png
└── Publication/
    └── 10T_SRAM_Paper.pdf
