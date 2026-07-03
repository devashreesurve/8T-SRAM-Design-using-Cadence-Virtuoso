# 8T-SRAM-Design-using-Cadence-Virtuoso

# Overview

This project presents the design, physical implementation, and post-layout verification of a Transmission Gate-Based 8T SRAM Cell targeted for ultra-low-power biomedical applications.

A conventional 6T SRAM cell experiences significant read stability degradation at sub-threshold voltages, making it unsuitable for low-power implantable devices. To address this limitation, an 8T SRAM architecture with a decoupled read path was designed and evaluated.

Both the conventional **6T SRAM** and the proposed **8T SRAM** cells were implemented in **Cadence Virtuoso** using the **45 nm Predictive Technology Model (PTM)**. The layouts were verified through **Design Rule Check (DRC)** and **Layout Versus Schematic (LVS)**, followed by parasitic extraction and post-layout simulations.

Simulation results demonstrate that the proposed 8T SRAM cell significantly improves read stability while reducing leakage power, making it a suitable memory architecture for biomedical and ultra-low-power System-on-Chip (SoC) applications.

---

# Project Objectives

- Design a conventional 6T SRAM cell
- Design an improved 8T SRAM cell with a decoupled read path
- Create physical layouts in Cadence Virtuoso
- Perform DRC and LVS verification
- Extract layout parasitics
- Perform post-layout simulations
- Compare Read SNM, Hold SNM, leakage power, and delay
- Evaluate robustness under Process, Voltage, and Temperature (PVT) variations

---

# Key Features

- Custom SRAM Cell Design
- Transmission Gate-Based 8T Architecture
- Cadence Virtuoso Schematic Design
- Physical Layout Design
- DRC Clean Layout
- LVS Verified Layout
- Parasitic Extraction
- Post-Layout Simulation
- Static Noise Margin (SNM) Analysis
- Leakage Power Analysis
- Delay Analysis
- PVT Corner Analysis
- 45nm PTM Technology

---

# Design Flow

```
Specification
      │
      ▼
Schematic Design
      │
      ▼
Physical Layout
      │
      ▼
DRC Verification
      │
      ▼
LVS Verification
      │
      ▼
Parasitic Extraction
      │
      ▼
Post-Layout Simulation
      │
      ▼
Performance Analysis
```

---

# Project Architecture

## Conventional 6T SRAM

The conventional 6T SRAM cell consists of:

- Two Cross-Coupled CMOS Inverters
- Two NMOS Access Transistors
- Shared Read/Write Word Line

Although compact, the coupled read/write path reduces Read Static Noise Margin (RSNM) at low supply voltages.

---

## Proposed 8T SRAM

The proposed design introduces two additional transistors to create an independent read port.

Advantages include:

- Decoupled Read Path
- Improved Read Stability
- Reduced Read Disturb
- Lower Leakage Current
- Better Reliability at 0.45 V

---

# Physical Layout

The SRAM layouts were designed using Cadence Virtuoso in 45 nm PTM technology.

Design considerations included:

- Compact Cell Layout
- Shared Diffusion Regions
- Matched Transistor Placement
- Metal Routing Optimization

---

# Layout Verification

## Design Rule Check (DRC)

✔ No Design Rule Violations

## Layout Versus Schematic (LVS)

✔ Layout matches the schematic successfully

These verification steps ensure that the fabricated layout is electrically equivalent to the designed schematic.

---

# Simulation Flow

```
Schematic
      │
      ▼
Layout
      │
      ▼
Parasitic Extraction
      │
      ▼
Transient Simulation
      │
      ▼
SNM Analysis
      │
      ▼
Power Analysis
      │
      ▼
PVT Analysis
```

---

# Static Noise Margin Analysis

Static Noise Margin (SNM) was evaluated using the butterfly curve generated from the voltage transfer characteristics of the cross-coupled inverters.

## Read SNM

| Cell | Read SNM |
|--------|----------:|
| 6T SRAM | 21 mV |
| 8T SRAM | 187 mV |

The proposed 8T SRAM provides nearly **8.9× improvement in Read Static Noise Margin**, significantly enhancing read stability under sub-threshold operation.

---

# Hold Static Noise Margin

| Cell | Hold SNM |
|--------|----------:|
| 6T SRAM | 220 mV |
| 8T SRAM | 220 mV |

The hold stability remains unchanged while improving read reliability.

---

# Leakage Power Analysis

| Cell | Leakage Power |
|--------|--------------:|
| 6T SRAM | 118.5 nW |
| 8T SRAM | 81.5 nW |

The proposed architecture reduces leakage power by approximately **31.2%**, making it highly suitable for battery-operated biomedical devices.

---

# Delay Analysis

Transient simulations were performed to evaluate read and write timing.

Observations:

- Stable read operation
- Reliable write operation
- Slight increase in read delay due to the buffered read path
- Improved reliability outweighs the small delay penalty

---

# PVT Analysis

Performance was evaluated across multiple Process, Voltage, and Temperature corners.

Results show:

- Stable operation across all corners
- Positive Read SNM maintained
- Improved robustness compared to conventional 6T SRAM

---

# Results Summary

| Parameter | 6T SRAM | 8T SRAM |
|------------|---------:|---------:|
| Read SNM | 21 mV | 187 mV |
| Hold SNM | 220 mV | 220 mV |
| Leakage Power | 118.5 nW | 81.5 nW |
| Read Stability | Poor | Excellent |
| DRC | Pass | Pass |
| LVS | Pass | Pass |

---

# Tools Used

- Cadence Virtuoso
- Spectre Simulator
- 45nm PTM Technology
- DRC Verification
- LVS Verification
- Post-Layout Extraction

---

# Applications

- Implantable Biomedical Devices
- Ultra-Low-Power Memory
- Wearable Electronics
- Internet of Medical Things (IoMT)
- Energy-Efficient SoCs
- Embedded Memory Systems
- Low-Power VLSI Design

---

# Future Work

- SRAM Array Design
- 9T and 10T SRAM Architectures
- Advanced Process Nodes (28 nm / 14 nm)
- Sense Amplifier Integration
- Memory Compiler Development
- Tape-Out for Silicon Validation

---

# Skills Demonstrated

- SRAM Design
- Custom IC Design
- Cadence Virtuoso
- CMOS Layout
- DRC Verification
- LVS Verification
- Post-Layout Simulation
- Static Noise Margin Analysis
- Leakage Power Optimization
- PVT Corner Analysis
- Semiconductor Memory Design

---

# Author

**Devashree Surve**

B.E. Electronics Engineering (VLSI Design & Technology)

Interested in RTL Design • Memory Design • Physical Design • ASIC Verification


---

⭐ If you found this repository useful, please consider giving it a star.
