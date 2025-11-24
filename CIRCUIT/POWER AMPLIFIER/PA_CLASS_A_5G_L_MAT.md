# 5-GHz Power Amplifier (PA) Design

---

## 1️⃣ Design Specifications

| Parameter          | Target   |
|------------------|---------|
| Supply Current    | ≥ 10 mA |
| Power Gain        | 10 dB   |
| Operating Frequency | 5 GHz  |

---

## 2️⃣ Device & Circuit Parameters (Before Matching)

| Parameter                | Value       |
|--------------------------|------------|
| Transistor Width (W)      | 1 µm       |
| Number of Fingers (M)     | 60         |
| Source Inductor (L)       | 100 nH     |
| PA Load Inductor (L<sub>PA</sub>) | 10 nH |
| Bias Inductor             | 100 pH     |
| Drain Resistance (R)      | 360 Ω      |
| Gate Bias Voltage (V<sub>BIAS</sub>) | 550 mV |
| Supply Voltage (V<sub>DD</sub>)     | 600 mV |

---

## 3️⃣ Circuit Schematic (Before Matching)

![PA Schematic Before Matching](https://github.com/user-attachments/assets/27297d19-31c7-4e5c-ab74-140598e4c589)

---

## 4️⃣ Simulation Result — Before Matching

![Simulation Before Matching](https://github.com/user-attachments/assets/1f58641a-2d94-4c44-8de2-d7db7bf1ef1f)

> **Observation:** The circuit is unconditionally stable, but gain is below target due to unmatched input/output.

---

## 5️⃣ Input Matching Network

![Input Matching Network](https://github.com/user-attachments/assets/dba9d82c-3a9d-4ff9-9105-521d2d91e639)

---

## 6️⃣ Output Matching Network

![Output Matching Network](https://github.com/user-attachments/assets/6da56475-eb55-43af-bd1b-d4004ce0e3a7)

---

## 7️⃣ Final PA Circuit After Matching

![Final PA Circuit](https://github.com/user-attachments/assets/57db9f80-2b69-4aca-bfa2-ecaa228a2a41)

---

## 8️⃣ Final Simulation — After Matching

![Final Simulation](https://github.com/user-attachments/assets/a7a9771e-412b-42f8-be7b-a73e58abc694)

![S21 Result](https://github.com/user-attachments/assets/ff5a6cfe-2dc1-4a9a-bcdd-cd7e81cea892)

> **Highlights:**
> - Input and output are fully complex-conjugate matched.
> - Final gain meets the 10 dB requirement at 5 GHz.
> - Stability preserved after matching.
> - T-network matching (Q = 5) used for both ports.

---

## 9️⃣ Small-Signal Analysis

### 9.1 Maximum Gain vs Frequency (G<sub>max</sub>)

![Gmax vs F](https://github.com/user-attachments/assets/cf3e112c-8a6a-4d38-8722-70a9b04dd969)

### 9.2 MSG vs Frequency (G<sub>MSG</sub>)

![GMSG vs F](https://github.com/user-attachments/assets/b908cac6-1781-4c81-b119-990538d82417)

> **Q:** Why is S21 not 18.25 dB?

### 9.3 Minimum Noise Figure (NF<sub>min</sub>) vs Frequency

![NFmin vs F](https://github.com/user-attachments/assets/51b6d0f8-45e0-4d20-b680-4eae04f2c9c2)

### 9.4 Noise Figure (NF) vs Frequency

![NF vs F](https://github.com/user-attachments/assets/569c251a-747e-41a9-bc03-4125330ad98e)

### 9.5 Transducer Gain (G<sub>T</sub>) vs Frequency

![GT vs F](https://github.com/user-attachments/assets/a7899430-78b2-4361-a792-ca4e6fa5aa7c)

### 9.6 Available Gain (G<sub>A</sub>) vs Frequency

![GA vs F](https://github.com/user-attachments/assets/97194cd9-13ac-4890-a1d7-07d1b2bead9d)

### 9.7 Power Gain (G<sub>P</sub>) vs Frequency

![GP vs F](https://github.com/user-attachments/assets/b989c0b4-8cfd-4fd1-8cea-5cd9f50b5d92)

> **Q:** Without connecting anything at the port, how are these values obtained?

### 9.8 Noise Circle (NC) on Smith Chart

![NC Smith Chart](https://github.com/user-attachments/assets/849edb08-1f3e-408e-858b-773941630e8a)

![NC Smith Chart Zoom](https://github.com/user-attachments/assets/c4b62e21-06e5-48c3-9c77-eb3205f2c5f2)

### 9.9 Gain vs F (GAC)


### 9.10 Single-Sideband (SSB)

![SSB vs F](https://github.com/user-attachments/assets/ceb992af-57fe-4c8c-8157-8fc655273ecb)

---

## 10️⃣ Notes

- All matching networks are designed to maximize gain and minimize NF.
- Simulation confirms that PA meets design targets at 5 GHz.
- Small-signal parameters provide insight into intrinsic transistor behavior.

