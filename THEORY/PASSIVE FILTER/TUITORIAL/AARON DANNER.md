<h1 align="center">📘 Lecture 1: Introduction to Passive Filters</h1>

<p>
A <b>filter</b> is an electrical circuit that <b>allows some frequencies to pass</b> while <b>blocking or attenuating others</b>.  
Filters are easily identified by looking for combinations of <b>R (resistors)</b>, <b>L (inductors)</b>, and <b>C (capacitors)</b>.
</p>

<div align="center">
  <img src="https://github.com/user-attachments/assets/b9364d33-81fb-463b-83c6-74ed24f68d6a" width="500"/>
</div>

<hr/>

<h2>🔹 What Is a Pole Filter?</h2>

<h3>👉 What Is a Pole?</h3>

<p>
A pole defines the <b>order of 's'</b> in the denominator of the transfer function.  
In this lecture, we focus on the <b>single-pole filter</b>.
</p>

<p>
Intuitively, the number of poles ≈ number of <b>energy-storing elements</b> (inductors or capacitors).
</p>

<ul>
  <li>Sometimes two inductors or two capacitors can be combined mathematically → still a <b>one-pole circuit</b>.</li>
</ul>

<hr/>

<h2>🔹 What Is a Transfer Function?</h2>

<p>
The transfer function describes the relationship between input and output:
</p>

<pre>
H(s) = Vout / Vin
</pre>

<div align="center">
  <img src="https://github.com/user-attachments/assets/11b94a70-9f42-4a5f-aa37-eb4ae00cd07a" width="500"/>
</div>

<hr/>

<h2>🔹 What Is Impedance?</h2>

<p>
Impedance is the <b>frequency-dependent opposition</b> to current flow, used to calculate transfer functions.
</p>

<pre>
H(jω) → Fourier domain
H(s)  → Laplace domain
</pre>

<hr/>

<h2>🔹 Why Do Some Circuits Pass Only Low or High Frequencies?</h2>

<p>
The answer lies in the nature of <b>L</b> and <b>C</b>:
</p>

<ul>
  <li>Capacitor → low impedance at <b>high</b> frequency</li>
  <li>Inductor → low impedance at <b>low</b> frequency</li>
</ul>

<p>
Depending on how R, L, and C are arranged, circuits behave as:
</p>

<ul>
  <li>Low-pass filter</li>
  <li>High-pass filter</li>
  <li>Band-pass filter</li>
  <li>Band-stop filter</li>
</ul>

<div align="center">
  <img src="https://github.com/user-attachments/assets/efb632a2-d65a-44c4-b738-f88fc24ced3b" width="500"/>
</div>

<hr/>

<h2>🔹 Magnitude Response</h2>

<div align="center">
  <img src="https://github.com/user-attachments/assets/a252df0a-f15d-48d8-ab44-b2c76a27f556" width="350"/>
</div>

<p>
To clearly visualize filter behavior, magnitude is plotted on a <b>logarithmic scale</b>.
</p>

<hr/>

<h2>🔹 What Is Roll-Off?</h2>

<p>
Roll-off describes how fast the filter attenuates frequencies beyond the cutoff.
</p>

<h3>✔ Single-Pole Filter Roll-Off:</h3>

<pre>
20 dB/decade per pole
</pre>

<p>
More poles → sharper roll-off.
</p>

<hr/>

<h2>🔹 What Is Corner (Cutoff) Frequency?</h2>

<p>
The cutoff (corner) frequency is defined where:
</p>

<pre>
ωT = 1
</pre>

<p>
At this point:
</p>

<ul>
  <li>Output power drops to <b>half</b> the input power.</li>
  <li>Voltage reduces to <b>0.707 (−3 dB)</b>.</li>
  <li>This is also called the <b>characteristic frequency</b> of the filter.</li>
</ul>

<div align="center">
  <img src="https://github.com/user-attachments/assets/626dd11a-f1b4-42d7-a8ba-6db5d08f5f6b" width="400"/>
</div>

<hr/>

<h2>🔹 Phase Response</h2>

<p>
Besides magnitude, every filter also introduces <b>phase shift</b>.
</p>

<div align="center">
  <img src="https://github.com/user-attachments/assets/53d46e1e-f22d-42aa-804d-4c638ff47a6e" width="380"/>
</div>

<p>
A single-pole low-pass filter produces a phase shift between:
</p>

<pre>
0°  to  −90°
</pre>

<p>
Higher frequency → larger negative phase shift.
</p>

<hr/>

<h2>📌 Summary</h2>

<ul>
  <li>Filters pass selected frequencies and block others.</li>
  <li>A single pole corresponds to a first-order filter.</li>
  <li>Transfer function: <b>H(s) = Vout/Vin</b>.</li>
  <li>Impedance defines the frequency behavior of R, L, and C.</li>
  <li>Single-pole filters have <b>20 dB/decade</b> roll-off.</li>
  <li>Corner frequency occurs at <b>−3 dB</b> output.</li>
  <li>Phase shift for a single-pole LPF ranges from <b>0° to −90°</b>.</li>
</ul>

<hr/>

<h1 align="center">📘 Lecture 2: Bode Plots with One-Pole Filters</h1>

<p>
For an RC low-pass filter, the <b>time constant</b> is <b>RC</b>, and the <b>transient settling time</b> is approximately <b>5RC</b>.  
Understanding Bode plots helps us predict filter behavior in the frequency domain.
</p>

<hr/>

<h2>🔹 What Is a Bode Plot?</h2>

<p>
A <b>Bode plot</b> consists of two graphs:
</p>

<ul>
  <li><b>Magnitude plot</b> → |H(jω)| in dB vs frequency (log scale)</li>
  <li><b>Phase plot</b> → ∠H(jω) in degrees vs frequency</li>
</ul>

<p>
It is essential for circuit design because it shows <b>how filters behave at different frequencies</b> and how phase shifts affect signal timing.
</p>

<div align="center">
  <img src="https://github.com/user-attachments/assets/121193e0-a5d0-4299-8ea8-3948768952a3" width="350">
</div>

<hr/>

<h2>🔹 Do Magnitude and Phase Intersect at One Point?</h2>

<p>
No — magnitude (in dB) and phase (in degrees) are plotted with <b>different units</b> and scales.  
They never “intersect”; they are simply plotted together for understanding frequency behavior.
</p>

<hr/>

<h2>🔹 What Is a Load? Why Does It Matter?</h2>

<p>
A <b>load</b> is any component connected to the output (often a resistor).  
Adding a load changes the <b>effective impedance</b> seen by the filter, which can:
</p>

<ul>
  <li>Shift the cutoff (corner) frequency</li>
  <li>Change the gain</li>
  <li>Modify phase response</li>
</ul>

<p>
Only when the load resistance is <b>very large</b> compared to filter impedances does the filter behave ideally.
</p>

<hr/>

<h2>🔹 When Does the Load Alter the Corner Frequency?</h2>

<p>
Load affects the corner frequency when:
</p>

<ul>
  <li><b>R<sub>load</sub></b> is comparable to the filter resistance</li>
  <li><b>R<sub>load</sub></b> is comparable to the capacitive reactance X<sub>C</sub> at critical frequencies</li>
</ul>

<p>
Load does <b>not</b> affect the filter when:
</p>

<ul>
  <li><b>R<sub>load</sub> ≫ R</b> and <b>R ≫ X<sub>C</sub></b> (at corner frequency)</li>
</ul>

<div align="center">
  <img src="https://github.com/user-attachments/assets/19dbc47b-9cc4-445f-b4e0-e3d5036340c3" width="180">
</div>

<p><i>Why?</i>  
Because if R<sub>load</sub> is huge, almost <b>no current flows through it</b>, so it does not load or distort the RC network.  
The filter behaves as if the load is not there.</p>

<hr/>

<h2>🔹 Source Resistance Also Matters</h2>

<div align="center">
  <img src="https://github.com/user-attachments/assets/c887070c-9618-46d0-82af-52c4a7d4ba3c" width="180">
</div>

<p>
Source resistance adds to the filter’s effective R and therefore shifts the <b>corner frequency</b>.
</p>

<h3>👉 How to Compensate Loading or Source Effects?</h3>

<ul>
  <li>Choose <b>smaller capacitors</b> or <b>larger resistors</b> to restore cutoff</li>
  <li>Use <b>buffer amplifiers</b> (op-amps) so load does not affect the filter</li>
  <li>Design for the <b>actual</b> R<sub>source</sub> and R<sub>load</sub> instead of ideal assumptions</li>
</ul>

<hr/>

<h1 align="center">🎚 High-Pass Filter</h1>

<div align="center">
  <img src="https://github.com/user-attachments/assets/4af610b1-ca1d-420a-b983-50761a5572a9" width="300">
</div>

<p>
A high-pass filter has:
</p>

<ul>
  <li><b>One zero</b> (at ω = 0)</li>
  <li><b>One pole</b> (at ω = 1/RC or R/L)</li>
  <li>Same time constant as LPF: <b>RC</b> or <b>L/R</b></li>
</ul>

<h2>🔹 Amplitude Plot</h2>

<div align="center">
  <img src="https://github.com/user-attachments/assets/05a645f5-f16c-466d-ac83-a3facf5bb7cc" width="350"><br><br>
  <img src="https://github.com/user-attachments/assets/d2286ca4-650b-4339-9ef3-4795ca81ced2" width="350">
</div>

<p>
At low frequencies → output is small (capacitor blocks DC).  
At high frequencies → output follows input (capacitor becomes short).
</p>

<hr/>

<h2>🔹 Phase Response of High-Pass Filter</h2>

<p>
Phase lies between:
</p>

<pre>
+90° (low frequencies) → 0° (high frequencies)
</pre>

<p>
At low frequency, the capacitor leads, giving a +90° phase shift.  
At high frequency, the circuit behaves like a resistor → no phase shift.
</p>

<hr/>

<h2>🔹 Why Do Capacitors Lead and Inductors Lag?</h2>

<p>
This comes from the voltage–current equations:
</p>

<pre>
Capacitor:     i = C dv/dt   → current leads voltage  
Inductor:      v = L di/dt   → voltage leads current
</pre>

<p>
This results in a maximum phase shift of <b>±90°</b> for each L or C.  
To get higher phase shifts (e.g., 125°, 178°), you need <b>multiple poles</b>.
</p>

<hr/>

<h2>🔹 Load/Source Effects in High-Pass Filters</h2>

<p>
Just like low-pass filters, high-pass filters are also affected by:
</p>

<ul>
  <li>Load resistance</li>
  <li>Source resistance</li>
</ul>

<p>
They change both the <b>zero</b> and the <b>pole</b>, thus altering cutoff and phase response.
</p>

<hr/>

<h1 align="center">📘 Summary: Low-Pass vs High-Pass</h1>

<div align="center">
  <img src="https://github.com/user-attachments/assets/cd84faf3-f4d1-46dc-8a86-9bfdc6ddab36" width="420">
</div>

<hr/>

<h1 align="center">🎯 Pole–Zero Design</h1>

<div align="center">
  <img src="https://github.com/user-attachments/assets/e432e25a-25b7-4f2e-a3a7-09a32f58f291" width="450">
</div>

<p>
Pole–zero placement gives us <b>design freedom</b> to choose R, C, or L values.  
Higher R or lower C shifts the pole to <b>lower frequencies</b>; the opposite shifts it higher.
</p>

<hr/>




<h1 align="center">📘 Lecture 3: Choosing the Right Capacitor in RC/LC Filters</h1>

## 🔍 RC Filter: Which Component to Choose First?

In an **RC filter**, the corner frequency \( f_c \) is determined by the **time constant**:

\[
f_c = \frac{1}{2\pi RC}
\]

Only the **product RC** matters — but practically, **we choose the capacitor (C) first**.

### ✅ Why choose **C first**?
- Capacitors come in **much wider ranges** (pF → µF → mF) than resistors.
- In labs, many precise capacitor values are available (1 pF, 2.2 pF, 4.7 pF, 10 pF …).
- Once **C is chosen**, calculating the matching **R** is easy:
  
  \[
  R = \frac{1}{2\pi f_c C}
  \]

---

## ⚠ Avoid Electrolytic Capacitors in Filters  
**Do NOT use electrolytic capacitors** for filters when corner frequency accuracy matters.

✔ Use electrolytic only when your goal is:  
- **Block DC**  
- **Pass AC**  
- **Large capacitance (µF–mF)** is needed with *low precision*

❌ Electrolytics have:  
- High ESR  
- Poor tolerance (±20% or worse)  
- Strong frequency dependence  
- Non-linear behavior

---

## ⚠ Very Small Caps (1 pF Range)
When capacitances are **too small**, they behave like **parasitic** capacitances:

- PCB pad capacitance  
- MOSFET drain–gate capacitance  
- Stray wiring capacitance  

So avoid **ultra-small caps** unless operating in RF/high-frequency ranges.

---

## 🔍 RL Filter: Which Component to Select First?

In an **RL filter**, the corner frequency is:

\[
f_c = \frac{R}{2\pi L}
\]

Here we choose the **inductor (L) first**, because:

- Inductors have **limited, discrete values** in lab stock  
- Inductors are bulkier, more expensive, and harder to tune  
- Once L is selected, compute R easily:

\[
R = 2\pi f_c L
\]

---

## ❓ Q: For LC Filter, What Do We Choose First?

For an **LC filter**, the resonant frequency is:

\[
f_0 = \frac{1}{2\pi \sqrt{LC}}
\]

### 💡 Practical Rule:
👉 **Choose the inductor (L) first**, then calculate C.

### Why choose L first?
- Inductor values are restricted (10 nH – 100 µH range)
- Inductors are expensive and size-dependent  
- Capacitors are available in huge variety, making C easy to adjust

So:

\[
C = \frac{1}{(2\pi f_0)^2 L}
\]

---

## 🧠 Choosing RC vs RL vs LC Filters

### ✔ RC Filter (Most common at low frequencies)
Use when:
- Low frequency (<100 kHz)
- Simple, low-cost filtering
- No need for high Q

**Why RC?**  
Huge variety of capacitor values available → easy to hit the exact cutoff.

---

### ✔ RL Filter  
Use when:
- Higher current is involved  
- Low-loss filtering is required  
- High-power circuits  

---

### ✔ LC Filter (Preferred in RF)
Use for:
- **RF circuits**
- **High-Q filters**
- **Narrow bandwidth filters**
- **Antenna matching**
- **Oscillators**

### Why LC for RF instead of RC or RL?
🔸 **Better Q-factor**  
RC filters have resistors → introduce loss → low Q  
LC filters use reactive components → very high Q → sharp cutoff

🔸 **Frequency-sensitive & tunable**  
Small changes in L/C precisely tune resonant frequency.

🔸 **Lower loss at RF**  
Resistors waste power, inductors/caps do not.

🔸 **Impedance matching**  
LC networks allow matching between RF stages, antennas, amplifiers.

Thus:

> **RC filters are great for low-frequency, low-Q applications  
> LC filters dominate RF design because they offer high Q and low loss.**

---

## 📄 Summary

| Filter Type | Choose First | Why? |
|------------|--------------|------|
| **RC** | Capacitor (C) | Wide range, stable values, easy to select |
| **RL** | Inductor (L) | Limited values available, harder to tune |
| **LC** | Inductor (L) | Inductor range is limited; capacitor can be tuned freely |

---

<h1 align="center">📘 Lecture 4: Problems for 1-Pole Filters with Design Freedom</h1>

## 🔄 Tau (τ) vs. Period (T): Why the Confusion?
- **τ (Time Constant)** → Defines how fast a 1-pole filter responds.  
  \[
  \tau = RC \quad \text{or} \quad \tau = \frac{L}{R}
  \]
- **T (Period)** → The time taken for one full cycle of a waveform.  
  \[
  T = \frac{1}{f}
  \]

Both have the unit **seconds**, but their meaning is different:
- τ = system response time  
- T = input signal time cycle  

---

## 🧪 Design 1: Effect of Load on Corner Frequency

<img width="443" height="215" src="https://github.com/user-attachments/assets/49dc2a88-3c94-44d2-869d-5f754c905fa3" />

Here:
- R is in the **10 kΩ range**, which is reasonable.
- If the **load resistance is very large** (hundreds of kΩ or MΩ),
  then the voltage divider effect becomes negligible.
- Therefore, **corner frequency stays unchanged**.

**Key Idea:**  
A 1-pole filter behaves ideally when load resistance ≫ filter resistance.

---

## 🧪 Design 2: High-Frequency Realities – Lumped vs Distributed Networks

<img width="428" height="149" src="https://github.com/user-attachments/assets/78e32f8d-2bec-4f22-a824-35030f009e95" />

At very high frequencies:
- Components become electrically **smaller**.
- Wires, PCB traces, and even device packages start to behave like:
  - inductors  
  - capacitors  
  - transmission lines  

This is where the idea of:
- **Lumped elements** (ideal R, L, C)
- **Distributed elements** (transmission line behavior)

becomes important.

**Rule of Thumb:**  
If the physical length is **≥ λ/20**, treat the network as **distributed**.

---

## 🧪 Design 3: Inductor in Series — Why It Blocks High Frequencies?

### 🌀 Impedance of an Inductor
\[
Z_L = j\omega L
\]

- At **low frequency** (ω ≈ 0)  
  \[
  Z_L \to 0 \quad (\text{acts like a short})
  \]  
  DC passes easily → inductor is “invisible”.

- At **high frequency** (ω → large)  
  \[
  Z_L \to \infty \quad (\text{acts like an open})
  \]  
  AC at high frequency is **blocked**.

### ❓ Does noise have higher frequencies?
**Yes.**  
Most unwanted noise sources (switching noise, digital edges, EMI) have **much higher frequency content** than the main signal.

### 📌 Real-Life Use: Choke
<img width="451" height="111" src="https://github.com/user-attachments/assets/fb248105-5f7a-451b-aa64-520aa4dcc078" />

A **high-frequency choke** is placed in series with the power line to:
- Block high-frequency noise  
- Allow DC to pass into the circuit  

This is exactly the use-case of a **1-pole RL high-pass and low-pass behavior**.

---

## 🧪 Design 4: Capacitor Blocking DC

<img width="368" height="102" src="https://github.com/user-attachments/assets/d106b67a-2e4e-474e-90b4-21e0af15f56e" />

Two parallel plates separated by a dielectric:
- Are **not touching** → **no DC conduction**
- But they **do allow AC** due to displacement current:

\[
i_C = C \frac{dv}{dt}
\]

- High frequency → large \( \frac{dv}{dt} \) → AC passes  
- DC → \( \frac{dv}{dt} = 0 \) → no current

**Thus, capacitors block DC and pass AC.**

---

## 📄 Summary

| Concept | Explanation |
|--------|-------------|
| **τ vs T** | τ = time constant of the system, T = waveform period |
| **Filter + Load** | High load resistance prevents corner frequency shifts |
| **High-frequency design** | Lumped → low frequency, Distributed → high frequency |
| **Inductor in series** | Passes DC, blocks high-frequency noise |
| **Capacitor block DC** | No direct path → only AC displacement current |

---
