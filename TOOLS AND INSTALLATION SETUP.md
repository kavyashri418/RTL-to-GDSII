# 🛠️ Tools Installation Guide

This document contains installation instructions for all essential tools used in the **RISC-V Reference SoC Tapeout Program**.

---

## 📋 System Requirements

Ensure your system meets the following minimum requirements:

- 💾 **RAM**: 6 GB  
- 💽 **Storage**: 50 GB HDD  
- 🧠 **CPU**: 4 vCPUs  
- 🐧 **Operating System**: Ubuntu 20.04 or later

---

## 1. 🔧 Yosys – RTL Synthesis

Yosys is an open-source logic synthesis framework that converts Verilog RTL into gate-level netlists suitable for physical design.

```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys

# Install dependencies
sudo apt install make  # (if not already installed)
sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev

# Build and install
make config-gcc
make
sudo make install

```
## 2. 💻 Icarus Verilog (Iverilog)

Iverilog is an open-source Verilog compiler and simulator for digital circuit design and verification.

```bash
sudo apt-get update
sudo apt-get install iverilog

```

## 3. 📈 GTKWave – Waveform Viewer

GTKWave is a waveform viewer for post-simulation analysis of digital signals, primarily Verilog and VHDL.

```bash
sudo apt-get update
sudo apt install gtkwave

```

## 4. ⚡ Ngspice – Circuit Simulator

Ngspice is a mixed-signal circuit simulator used for analyzing time-varying voltages, currents, noise, and small-signal behavior.

Download from: https://sourceforge.net/projects/ngspice/files/ to a local directory, unpack it using:

```bash
tar -zxvf ngspice-37.tar.gz
cd ngspice-37
mkdir release
cd release
../configure --with-x --with-readline=yes --disable-debug
make
sudo make install

```

## 5. 🧱 Magic – VLSI Layout Tool

Magic is a VLSI layout editor for interactive physical design, with built-in DRC and circuit extraction capabilities.

Install dependencies:

```bash
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev \
  libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
```

Clone and build Magic:

```bash
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```

## 🧪Tool Version Checks

Run the following commands to verify installations:

```bash
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
```

## 📝 Note

All installations assume a Debian-based Linux system (e.g., Ubuntu 20.04+).
Make sure to run sudo apt-get update before each major installation step.
You may need to restart the terminal or log out/in after installing system tools.
