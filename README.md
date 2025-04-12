# ASIC Implementation of Motion Estimator in 14nm CMOS
 
👨‍💻 **Contributors**: Mohammed Ata Ur Rahman, Harika Kumbham   

---

## 🧠 Project Overview

This project implements a **Motion Estimator** using the **Block Matching Algorithm** on a 14nm CMOS ASIC platform. The goal is to optimize video compression by identifying motion vectors between sequential grayscale video frames — reducing storage and transmission costs significantly.

By implementing this estimator in hardware, we achieved better speed and energy efficiency compared to software approaches. Our design supports **real-time encoding at 15 FPS** and is optimized for power, area, and timing closure.

---

## 📐 Design Specifications

- **Technology Node**: 14nm FinFET CMOS  
- **Clock Frequencies**: 130 MHz & 260 MHz  
- **Input Format**:  
  - Reference Block: 16×16 pixels (8-bit grayscale)  
  - Search Window: 31×31 pixels  
- **Algorithm**: Block Matching for Motion Estimation  
- **Throughput Goal**: 15 Frames per Second  
- **Tools Used**:  
  - Verilog, Synopsys Design Compiler, ICC2, PrimeTime  
  - VCS for simulation  
  - FPGA prototyping (planned)

---

## 🏗️ Design Architecture

The hardware design includes:

- ✅ **Processing Elements**: Calculate distortion between reference and search blocks  
- ✅ **Comparator Module**: Selects the lowest distortion vector  
- ✅ **Controller**: Manages scan control signals and memory access  
- ✅ **Top-Level Integration**: Combines all modules for full Motion Estimation

A pipelined structure using 16 parallel Processing Elements was adopted for performance.

---

## 🧪 Verification

- Developed testbenches for individual submodules  
- Waveform simulations run using Synopsys VCS  
- Functional verification of top module with corner-case input values  
- FPGA-based emulation was designed but not executed in this version

---

## 🔧 Synthesis

- Synthesized RTL with **Design Compiler**
- Clock frequency set to **260 MHz (3.846 ns period)**
- Post-synthesis reports include:
  - Gate-level netlist
  - Power and Area estimates
  - Setup and Hold timing reports
- Static Timing Analysis attempted with **PrimeTime**

---

## 🧱 Physical Design

Performed using **ICC2**, including:

- Floorplanning  
- Placement  
- Clock Tree Synthesis  
- Routing  
- Design Rule Checking (DRC)  
- Post-layout STA and sign-off

The design passed all required timing and DRC constraints.

---

## 📈 Results

- ✅ Successfully completed full ASIC Design Flow  
- ✅ Functional and timing verification achieved  
- ✅ Low-area and low-power implementation  
- ❌ FPGA emulation planned but not completed

---

## 📁 Project Deliverables

- Verilog RTL source code  
- Testbenches and simulation waveforms  
- Synthesis reports  
- Netlist and timing constraints  
- Floorplan, placement, and routed layout images  
- Post-layout analysis reports

---

## 👥 Contributors and Roles

### ✦ Harika Kumbham  
- RTL Design of Motion Estimator modules  
- Synthesis and Netlist generation  
- Physical Design Flow (Floorplanning, CTS, Routing)  
- Post-layout Timing Analysis and Reports  
- GitHub repository management and documentation  
🔗 [GitHub Profile](https://github.com/harikakumbham) 

### ✦ Mohammed Ata Ur Rahman  
- Submodule verification and testbench development  
- RTL Simulation using VCS  
- Waveform analysis and debugging  
- Physical Design Report analysis  
- Project Presentation and Documentation  
🔗 [GitHub Profile](https://github.com/mohammedataurrahman)

---

## 🚀 Future Enhancements

- Implement FPGA-based emulation for real-time testing  
- Extend design for color video support  
- Increase frame rate for high-performance applications  
- Port design to advanced technology nodes (7nm, 5nm)

---

## 📝 Acknowledgements

Special thanks to **Prof. [HAMID MAHMOODI** for guidance throughout the project and for enabling us to explore the complete RTL-to-GDSII flow.

“If everything you try works, you aren’t trying hard enough.”
— Gordon Moore, Co-founder of Intel

---
