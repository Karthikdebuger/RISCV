# 🖥️ RISC-V Reference SoC Tapeout Program VSD

<div align="center">

![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)
![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)
![Participants](https://img.shields.io/badge/Participants-3500+-success?style=for-the-badge)
![India](https://img.shields.io/badge/Made%20in-India-saffron?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjgiIGZpbGw9IiNGRjk5MzMiLz4KPHJlY3QgeT0iOCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjgiIGZpbGw9IiNGRkZGRkYiLz4KPHJlY3QgeT0iMTYiIHdpZHRoPSIyNCIgaGVpZ2h0PSI4IiBmaWxsPSIjMTM4ODA4Ii8+Cjwvc3ZnPgo=)

</div>

Welcome to my journey through the **SoC Tapeout Program VSD**!  

This repository documents my **week-by-week progress**, with tasks organized under each week.

<div align="center">

> *"In this program, we learn to design a System-on-Chip (SoC) from basic RTL to GDSII using open-source tools. It is part of India's largest collaborative RISC-V tapeout initiative, empowering 3500+ participants to build silicon and advance the nation’s semiconductor ecosystem."*

</div>

<div align="center">

📝 RTL Design → 🔄 Synthesis → 🏗️ Physical Design → 🎯 Tapeout Ready


</div>

---

# 📝 Task 1 — Documentation of Digital VLSI SoC Design and Planning  

## 📌 Introduction  
This document provides a **summary of Digital VLSI SoC Design and Planning**, highlighting the complete flow from **chip modeling** to **GDSII tapeout**.  
It explains the design methodology, verification steps, and the importance of modular **System-on-Chip (SoC)** integration.  

---

### Workflow Steps

## 🔹 O1 — Chip Modeling
- Starts with **application specifications** (C model).  
- Functionality validated using a **C testbench**.  
- Ensures correctness of design intent **before RTL implementation**.  

---

## 🔹 O2 — RTL Architecture 
- Hardware functionality described using **RTL (Verilog)** → *soft copy of hardware*.  
- Design partitioned into main modules:  
  - 🖥️ **Processor**  
  - 🔌 **Peripherals / IPs**  
- Verified against the C specification to ensure functional equivalence.  

---

## 🔹 Synthesis & Netlist Generation  
- RTL synthesized into a **Gate-Level Netlist (GLN)**.  
- Outputs include:  
  - ✅ Synthesized Gate-Level Netlist  
  - ✅ Standard cell libraries and macros  
  - ✅ Analog IPs (PLL, Clock multipliers, SRAM models)  

---

## 🔹 O3 — SoC Integration  
- Combines **Processor + Peripherals + IPs** into a complete SoC.  
- All blocks are combined (Processor, IPs, Macros, Analog IPs).  
- Integration also involves GPIOs and interconnects.  

---

## 🔹 Physical Design  
- Involves physical design steps:  
  - 📐 Floorplanning  
  - 🕒 Clock Tree Synthesis (CTS)  
  - 🛠️ Placement & Routing  
- Hardened macros and analog IP libraries are included.  
- Generates the final **GDSII file** for fabrication.  

---

## 🔹 Physical Verification & Fabrication
- ✅ **DRC (Design Rule Check):** Ensures layout follows foundry rules.  
- ✅ **LVS (Layout vs Schematic):** Confirms physical layout matches RTL netlist.  
- GDSII is sent for fabrication to produce the final chip.  

---

## 🔹 O4 — Final SoC  
- Operates within **100 MHz – 130 MHz** range.  
- Reusable SoC platform adaptable to multiple end-user applications:  
  - ⌚ iWatch  
  - 🔌 Arduino Boards  
  - 📺 TV Panels  
  - ❄️ AC Systems  

---

## ✅ Key Takeaways  
- **End-to-End Flow:** Specs → RTL → Synthesis → SoC Integration → Verification → TapeIn → Industry → Tapeout → Chip.  
- **Verification at every stage** ensures reliability and manufacturability.  
- **Scalable modular design** enables targeting diverse real-world applications.  
- **Key Outputs:**  
  - O1: Specs in C (with testbench)  
  - O2: RTL in Verilog  
  - O3: Integrated SoC (netlist + macros)  
  - O4: Final SoC  
- **Equivalence:** O1 == O2 == O3 == O4  


---

## 🙏 **Acknowledgment**

<div align="center">

### 🏆 **Program Leadership & Support**

I am thankful to [**Kunal Ghosh**](https://github.com/kunalg123) and the **[VLSI System Design (VSD)](https://vsdiat.vlsisystemdesign.com/)** team for the opportunity to participate in the **RISC-V SoC Tapeout Program**.

</div>

---

## 📈 **Weekly Progress Tracker**

![Week 0](https://img.shields.io/badge/Week%200-Tools%20Setup-success?style=flat-square)
![Week 1](https://img.shields.io/badge/Week%201-Coming%20Soon-lightgrey?style=flat-square)
![Week 2](https://img.shields.io/badge/Week%202-Upcoming-lightgrey?style=flat-square)

### 🚀 **Journey Continues...**

Stay tuned for upcoming weeks covering RTL design, synthesis, physical design, and final tapeout preparation!

---

**🔗 Program Links:**  
[![VSD Website](https://img.shields.io/badge/VSD-Official%20Website-blue?style=flat-square)](https://vsdiat.vlsisystemdesign.com/)  
[![RISC-V](https://img.shields.io/badge/RISC--V-International-green?style=flat-square)](https://riscv.org/)  
[![Efabless](https://img.shields.io/badge/Efabless-Platform-orange?style=flat-square)](https://efabless.com/)  

**👨‍💻 Participant:** [karthikdebuger](https://github.com/Karthikdebuger)
