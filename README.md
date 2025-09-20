# 🧠 RISC-V Reference SoC Tapeout Program – VSD

Welcome to my repository for the **RISC-V Reference SoC Tapeout Program**, a national-level initiative organized by **VSD (VLSI System Design)**. This program offers a **hands-on, end-to-end VLSI experience** — from **RTL design** all the way to **post-silicon validation** and **tapeout**.

---

## 📌 Program Overview

> "The RISC-V Reference SoC Tapeout Program is a national-level initiative to empower participants with real-world VLSI experience and to develop skilled Silicon Designers who don't just simulate — but fabricate."

This repository documents my journey and weekly progress through the program, focusing on:

- ✅ RTL Design & Simulation  
- ✅ Functional & Formal Verification  
- ✅ Synthesis using Open-Source Tools  
- ✅ Floorplanning, Placement, and Routing  
- ✅ Timing Analysis, DRC, and LVS  
- ✅ GDSII Generation and Tapeout Readiness  
- ✅ Post-Silicon Validation  

---

## 🎯 Program Goals

- Gain practical, end-to-end experience in VLSI SoC design.
- Learn and apply open-source EDA tools in real projects.
- Contribute to the fabrication of a working RISC-V-based SoC.
- Develop industry-relevant skills in RTL to GDSII flow.

---


## Tool Check

### Yosys
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
git submodule update --init --recursive
make
sudo make install














