# 8×8 SRAM Memory Design using Cadence Virtuoso

## Overview
This project presents the complete design and simulation of an 8×8 SRAM memory array using 6T SRAM cells, implemented in Cadence Virtuoso as part of the Digital VLSI Design course at IIT Tirupati.

---

## 6T SRAM Cell
The fundamental storage element is a 6T SRAM cell consisting of two cross-coupled CMOS inverters and two access transistors controlled by the wordline (WL).

![6T SRAM Cell](schematics/6T_SRAM_Cell.png)

### Static Noise Margin (SNM)
The DC butterfly curve confirms stable bistable operation of the SRAM cell.

![Butterfly Curve](simulations/Butterfly_Curve_SNM.png)

---

## Peripheral Circuits

### Precharge Circuit
Equalizes BL and BLB to VDD prior to read operations.

![Precharge Circuit](schematics/Precharge_Circuit.png)

### Write Driver
Drives complementary data onto BL and BLB during write cycles.

![Write Driver](schematics/Write_Driver.png)

### Sense Amplifier
Latch-type differential sense amplifier used to amplify small bitline voltage differences.

![Sense Amplifier](schematics/Sense_Amplifier.png)

Read operation waveform:

![Sense Amp Read](simulations/Sense_Amplifier_Working.png)

---

## 1-Bit SRAM Integration
Integration of the 6T SRAM cell with precharge, write driver, and sense amplifier.

![1-Bit SRAM](schematics/1bit_SRAM_Integration.png)

Transient simulation verifying correct read and write functionality:

![1-Bit SRAM Waveform](simulations/1bit_SRAM_Working.png)

---

## Decoder Design
A hierarchical 3×8 decoder implemented using two 2×4 decoder blocks.

![2x4 Decoder](schematics/Decoder_2x4.png)
![3x8 Decoder](schematics/Decoder_3x8.png)

---

## 8×8 SRAM Array
Complete memory array consisting of 64 identical 6T cells with column-wise shared peripheral circuits.

![8x8 SRAM Array](schematics/SRAM_8x8_Array.png)

---

## Tools Used
- Cadence Virtuoso
- CMOS 45 nm technology (course-provided)

---

## Credits

Project by **[Benedict Jowin C](https://www.linkedin.com/in/benedict-jowin/)**  
IIT Tirupati | Electrical Engineering | Class of 2027
