# 17 GHz Class-A Power Amplifier Design

This project presents the design and simulation of a **17 GHz Class-A Power Amplifier (PA)**. The amplifier is designed to achieve high gain and good efficiency while targeting a **2 GHz bandwidth (16–18 GHz)**. The design flow includes transistor characterization, impedance matching, S-parameter analysis, and large-signal Harmonic Balance (HB) simulations.

---

# Design Specifications

| Parameter | Specification |
|-----------|--------------:|
| Center Frequency | **17 GHz** |
| Bandwidth | **2 GHz (16–18 GHz)** |
| Bias Current | **15 mA** |
| Output Saturation Power (Psat) | **5 dBm** |
| Output 1-dB Compression Point (OP1dB) | **1 dBm** |
| Power Added Efficiency (PAE) | **40%** |
| Amplifier Class | **Class-A** |

---

# Design Flow

```
Transistor Design
        │
        ▼
Small-Signal Simulation
        │
        ▼
Extract S & Z Parameters
        │
        ▼
Impedance Calculation
        │
        ▼
Output Matching Network
        │
        ▼
S-Parameter Verification
        │
        ▼
Harmonic Balance Simulation
        │
        ▼
Performance Evaluation
```

---

# Initial Circuit (Before Matching)

The amplifier was initially designed without any matching network to evaluate its intrinsic RF characteristics.

## Circuit Before Matching

<img width="899" height="407" alt="Circuit Before Matching" src="https://github.com/user-attachments/assets/0c404be5-90f4-4a4a-ba6d-38382fefd919" />

---

# Small-Signal Analysis Before Matching

## S-Parameters

<img width="897" height="394" alt="S Parameters" src="https://github.com/user-attachments/assets/2b3a8013-dba4-4154-9e40-c994f71bdfae" />

### Observation

- Poor impedance matching
- High reflection coefficient
- Matching network required

---

## Z-Parameters

<img width="446" height="390" alt="Z Parameters" src="https://github.com/user-attachments/assets/a7594c34-49ff-4781-9a88-2ecf2e205f77" />

<img width="702" height="290" alt="Impedance Values" src="https://github.com/user-attachments/assets/1b22cf97-be89-4c50-ace4-9be6fd9c852f" />

### Observation

The transistor output impedance obtained from the Z-parameter simulation was used to design the output matching network.

---

# Output Matching Network

Several matching iterations were performed to transform the transistor output impedance to **50 Ω** at the operating frequency.

## Final Matching Circuit

<img width="937" height="316" alt="Matched Circuit" src="https://github.com/user-attachments/assets/4127209c-2ff0-485f-85a8-d20f0c1a7178" />

---

# Impedance Matching Calculation

<img width="845" height="380" alt="Impedance Calculation" src="https://github.com/user-attachments/assets/2b54a92e-f5fa-4fdf-9f84-4c0a69d18fee" />

The matching network was designed using the calculated output impedance and transformed to a standard **50 Ω** load.

---

# S-Parameter Verification

The matched amplifier was verified at the center frequency and both band-edge frequencies.

---

## At 17 GHz

<img width="848" height="379" alt="17 GHz Simulation" src="https://github.com/user-attachments/assets/b06d9b46-6d3c-4368-b96e-682814ab6316" />

### Result

- Best impedance matching
- Maximum gain
- Minimum reflection

---

## At 18 GHz

<img width="843" height="375" alt="18 GHz Simulation" src="https://github.com/user-attachments/assets/a8740e21-0234-4f4f-b709-ab95f8b2b477" />

### Result

Performance starts degrading away from the center frequency.

---

## At 16 GHz

<img width="448" height="357" alt="16 GHz Simulation" src="https://github.com/user-attachments/assets/72e7b998-503d-434a-af39-a64f4c201e05" />

### Result

The matching quality decreases further, indicating a narrowband matching network.

---

# Bandwidth Analysis

## Expected

- Frequency Range: **16–18 GHz**
- Bandwidth: **2 GHz**

## Obtained

The matching network provides excellent matching only near **17 GHz** and degrades rapidly at **16 GHz** and **18 GHz**.

### Current Limitation

- Narrowband impedance matching
- Reduced gain at band edges
- Increased return loss away from the center frequency

### Future Improvement

Design a broadband matching network capable of maintaining good performance over at least **1 GHz**, while preserving:

- High gain
- Good input/output matching
- High PAE
- Stable operation

---

# Harmonic Balance Simulation

Large-signal Harmonic Balance (HB) simulations were performed to evaluate nonlinear amplifier performance.

---

## Power Gain

<img width="442" height="292" alt="Power Gain" src="https://github.com/user-attachments/assets/fabc61b2-e424-4d53-ac6b-0e52181320cb" />

---

## Output-Referred Characteristics

<img width="844" height="380" alt="Output Referred" src="https://github.com/user-attachments/assets/a4153ea2-1b11-41f2-951f-0844c1b910a5" />

---

## Power Added Efficiency (PAE)

<img width="897" height="406" alt="PAE" src="https://github.com/user-attachments/assets/fbdb297d-7a86-4370-907c-7ba91a7973f6" />

---

# Performance Summary

| Specification | Target | Current Status |
|---------------|-------:|:--------------:|
| Center Frequency | 17 GHz | ✅ |
| Bandwidth | 2 GHz | ⚠️ Narrowband |
| Class-A Operation | Yes | ✅ |
| Bias Current | 15 mA | ✅ |
| Output Matching | Completed | ✅ |
| S-Parameter Analysis | Completed | ✅ |
| Harmonic Balance Simulation | Completed | ✅ |
| PAE | 40% | Under Optimization |
| Psat | 5 dBm | Under Verification |
| OP1dB | 1 dBm | Under Verification |

---

# Software Used

- Keysight ADS
- Harmonic Balance Simulator
- S-Parameter Simulator
- Smith Chart Tool
- Impedance Matching Network Designer

---

# Conclusion

A **17 GHz Class-A Power Amplifier** was successfully designed and analyzed using small-signal and large-signal simulations. The output matching network provides excellent matching at the center frequency; however, the current design exhibits narrowband behavior and does not fully satisfy the target **2 GHz bandwidth**. Future work will focus on broadband matching techniques to improve gain, return loss, and efficiency across the entire operating band.

---
