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

<h1 align="center">📘 Lecture 5: Introduction to Buffer Circuits</h1>

## 🔍 Why Do We Need a Buffer After Designing a Filter?

After designing a filter, the **load resistance** and **source resistance** can:
- Worsen the filter performance  
- Shift the corner frequency  
- Change the gain  
- Distort the phase response  

This leads to a common question:

### ❓ Can the source and load resistance improve filter response?  
**Sometimes yes, but mostly unpredictable.**  
Most of the time, they **distort** the designed response rather than improve it.

👉 This is exactly why **buffer circuits** are introduced.

---

## 🛡️ What Is a Buffer Circuit?

A **buffer** is a circuit that:
- Has **very high input impedance** → draws *almost zero current*  
- Has **very low output impedance** → can drive heavy loads  
- **Isolates** one circuit block from another  
- **Recreates** the input voltage at the output (ideally: gain = 1)

### Why is this useful?
Because:
- No current flows → no voltage drop across source  
- Filter characteristics remain unchanged  
- Cascading multiple filters becomes possible

---

## 🎧 Buffer in Bandpass Filter Implementation

Bandpass filters are often built by **cascading**:
- A high-pass filter  
- A low-pass filter  

But connecting them directly causes **loading effects**, changing the cutoff frequencies.

### ✔️ Solution → Insert a Buffer Between the Stages

<img width="464" height="200" src="https://github.com/user-attachments/assets/4ebaf727-c4a6-4fc9-bc06-92b2c10bd33d" />

The buffer ensures:
- The HPF output does **not** load the LPF  
- The LPF input does **not** distort the HPF output  
- Each section works as if the other one does not exist

---

## ⚡ How a Buffer Works

<img width="455" height="233" src="https://github.com/user-attachments/assets/57a763f6-77cb-41fe-8d04-155a59c7010c" />

- High input impedance → **no current drawn**
- Low output impedance → **strong drive capability**
- Output voltage ≈ Input voltage  
- Perfect for **isolation**

---

## 🔌 Are Common-Drain or Common-Collector Stages Buffers?

Yes ✔️  
- **Common Drain (Source Follower)** in MOSFET  
- **Common Collector (Emitter Follower)** in BJT  

Both act as **buffers** because:
- High input impedance  
- Low output impedance  
- Voltage gain ≈ 1  

But they use *active devices*, not passive ones.

### ⚠️ Are they examples of passive filters?
No.  
They are **active circuits**, but they are *used alongside passive filters* to prevent loading.

---

## 🎚️ Type 2: Single Op-Amp Active Filter

<img width="447" height="228" src="https://github.com/user-attachments/assets/5a923593-8ac2-45d8-94cb-115e1782a37e" />

### ❓ What is an Op-Amp?

An **operational amplifier** is:
- A high-gain differential amplifier  
- With extremely **high input impedance**  
- Very **low output impedance**  
- Ideal for buffering and active filtering  

This allows op-amp filters to:
- Maintain exact cutoff frequencies  
- Provide gain  
- Drive heavy loads  

Op-amp buffers are commonly called **voltage followers**.

---

## 📡 Buffers in RF Applications & Multistage Amplifiers

In RF and high-frequency circuits, buffers are implemented using:

### **Active Devices**
- Source follower (MOSFET)
- Emitter follower (BJT)
- Cascode-based buffer
- MMIC RF buffers

### **Passive Techniques**
- Impedance-matching networks  
- Transformers  
- λ/4 transmission line sections  

### **Specialized RF Buffers**
- Low-noise RF amplifiers (LNA stages)  
- Power buffers before antennas  

These ensure:
- Impedance matching  
- High-frequency stability  
- Proper gain distribution  
- Isolation between stages  

---

## 📡 Buffer vs Repeater — What’s the Difference?

| Feature | Buffer | Repeater |
|--------|--------|----------|
| **Purpose** | Isolate stages, prevent loading | Restore signal strength over long distances |
| **Gain** | ≈ 1 (unity gain) | > 1 (adds gain) |
| **Used in** | Filters, amplifiers, ADC drivers | Communication channels, digital systems |
| **Components** | MOSFET/BJT followers, op-amp followers | Amplifiers, line drivers, regenerative circuits |
| **Function** | Prevents distortion | Restores and reshapes signals |

### In Short:
- **Buffer = prevents distortion**  
- **Repeater = regenerates weak signals**  

---

## 📄 Summary

- Filters get distorted by source/load resistances → **buffer solves this**  
- Buffers have **high input impedance** and **low output impedance**  
- Used to isolate cascaded filters (especially bandpass filters)  
- Implemented using:  
  - Common drain / source follower  
  - Common collector / emitter follower  
  - Op-amp voltage follower  
  - RF buffer amplifiers  
- Buffer ≠ Repeater — buffers isolate, repeaters amplify  


<h1 align="center">📘 Lecture 6: 1-Pole Low-Pass Filter — Examples & Common Problems</h1>

## 🧩 Problem 1: Identifying Low-Pass vs High-Pass Filters

A quick trick:

- **High frequencies** → pass through the capacitor to **ground**  
- **Low frequencies** → stay at the output  
- Therefore → **Low-Pass Filter (LPF)**

<img width="471" src="https://github.com/user-attachments/assets/dfac81e0-2279-478e-887c-aa0b239a9bff" />

<img width="467" src="https://github.com/user-attachments/assets/2bb89f59-57f3-45d6-a2a8-29267279c490" />

### ✔️ Interpretation
- At **high frequency**, capacitor impedance is **very small**, acting like a short → signal goes to **ground**.
- At **low frequency**, capacitor impedance is **large**, so the signal remains at the **output**.

Thus, the circuit behaves as a **1-pole low-pass filter**.

---

## 🧩 Problem 2: Matching Responses Across Filter Types

To obtain **identical frequency response**, the **time constant** must match:

\[
RC = \frac{L}{R} = \frac{L}{C}
\]

This is why RC, RL, and LC filters can be compared by ensuring equal time constants.

<img width="394" src="https://github.com/user-attachments/assets/c04c0ddb-2196-4177-b476-fc3193584d3f" />

### ✔️ Why this matters
- The **corner frequency** of any 1-pole filter is governed by its **time constant**.
- Matching τ ensures:
  - Same −3 dB frequency  
  - Same roll-off  
  - Same phase behavior  

---

## 🧩 Problem 3: Effect of Load Resistance on the Pole Location

When a load resistor is attached:

<img width="473" src="https://github.com/user-attachments/assets/90196cea-2f8b-44d8-b99f-85fd8290cb7f" />

### ✔️ Key Principle
A **smaller load resistor** draws **more current**, which effectively **reduces** the resistance seen by the capacitor.

This causes:

\[
\tau = R_{\text{eq}}C
\]

to become **smaller**, and therefore the **corner frequency increases**:

\[
\omega_c = \frac{1}{\tau} = \frac{1}{R_{\text{eq}}C}
\]

### ❓ So does a higher load shift the pole left or right?

| Load Resistance | Time Constant | Corner Frequency | Pole Movement |
|----------------|---------------|------------------|---------------|
| **Large load (high R)** | Large τ | **Lower** ωc | **Pole shifts LEFT** (towards low frequency) |
| **Small load (low R)** | Small τ | **Higher** ωc | **Pole shifts RIGHT** (towards high frequency) |

### ✔️ Answer:
A **higher load resistance shifts the pole to the LEFT** (lower frequency).  
A **smaller load resistance shifts the pole to the RIGHT** (higher frequency).

---

## 📄 Summary

- LPF can be identified by observing how a capacitor reacts to different frequencies.  
- Matching **time constants** makes RC, RL, and LC filters behave identically.  
- Adding a load resistor modifies the effective resistance → moving the pole.  
- **Higher load resistance → pole shifts left (lower cutoff)**  
- **Lower load resistance → pole shifts right (higher cutoff)**


<h1 align="center">📘 Lecture 7: All About the 2-Pole RLC Passive Filter</h1>

<hr>

<h2>⭐ Why Do We Need Multi-Pole Systems?</h2>

<p>A <b>single-pole (1st-order) filter</b> provides:</p>
<ul>
  <li>Only one cutoff frequency</li>
  <li>Slow roll-off (−20 dB/dec)</li>
  <li>No ability to create a band-pass or band-stop response</li>
</ul>

<p>Modern RF/analog circuits require:</p>
<ul>
  <li>Sharper filtering</li>
  <li>Higher selectivity</li>
  <li>Resonant behavior</li>
  <li>Control over both low & high frequency limits</li>
</ul>

<p>➡️ <b>A band-pass filter requires at least two poles.</b></p>

<hr>

<h2>🆚 When to Choose Single-Pole vs Multi-Pole?</h2>

<h3>✔ Single-Pole (1st Order)</h3>
<p>Use when:</p>
<ul>
  <li>Simple LPF/HPF is enough</li>
  <li>No sharp selectivity needed</li>
  <li>Used for bias networks, DC blocking, simple conditioning</li>
</ul>

<h3>✔ Multi-Pole (2nd Order or Higher)</h3>
<p>Use when:</p>
<ul>
  <li>Band-pass or notch filtering is required</li>
  <li>Sharper roll-off (−40 dB/dec for 2 poles)</li>
  <li>Resonance or narrow bandwidth is needed</li>
  <li>Used in RF, IF filters, LNAs, mixers, matching networks</li>
</ul>

<hr>

<h1>🎛 Understanding the 2-Pole LRC Filter</h1>

<p>An RLC circuit has <b>two reactive components</b>, giving a <b>2-pole response</b> defined by:</p>

<ul>
  <li><b>ω₀</b> — resonant frequency</li>
  <li><b>Q</b> — quality factor (selectivity)</li>
</ul>

<p>You can take the output across:</p>
<ul>
  <li><b>Capacitor</b> → Low-Pass (2 poles, 0 zeros)</li>
  <li><b>Inductor</b> → High-Pass (2 poles, 2 zeros)</li>
  <li><b>Resistor</b> → Band-Pass (2 poles, 1 zero)</li>
</ul>

<img width="467" src="https://github.com/user-attachments/assets/6bb85ada-97b1-473a-8d4f-7cf79eec98af" />
<img width="468" src="https://github.com/user-attachments/assets/d503b296-e96a-441d-bdc9-4b8a3273fc5f" />
<img width="468" src="https://github.com/user-attachments/assets/7b59043f-15f1-4db5-95a4-01f548f2a91c" />

<hr>

<h1>🎚 Understanding the Quality Factor (Q)</h1>

<p>The <b>Q-factor</b> determines:</p>
<ul>
  <li>Sharpness of resonance</li>
  <li>Bandwidth of band-pass filters</li>
  <li>Peaking in LPF/HPF</li>
  <li>Damping of the system</li>
</ul>

<h3>Higher Q →</h3>
<ul>
  <li>Sharper peak</li>
  <li>Narrower bandwidth</li>
  <li>More selective filtering</li>
</ul>

<h3>Lower Q →</h3>
<ul>
  <li>More damping</li>
  <li>Wider bandwidth</li>
  <li>Less peaking</li>
</ul>

<h2>📉 LPF and HPF Responses with Q</h2>

<img width="467" src="https://github.com/user-attachments/assets/aa3b373a-b333-40ed-adf2-2150c7f5b6b4" />
<img width="467" src="https://github.com/user-attachments/assets/734f6765-d7e1-435e-9d55-1b8b6544542d" />

<hr>

<h1>📦 Other 2-Pole Topologies</h1>

<h3>📌 Series-Fed Band-Pass</h3>
<img width="467" src="https://github.com/user-attachments/assets/b0bdb509-5925-4c02-929c-4ba35a2018b0" />

<h3>📌 Shunt-Fed Band-Pass</h3>
<img width="166" src="https://github.com/user-attachments/assets/505af8b0-cdb8-4bf3-9181-752cc9006ccc" />

<hr>

<h1>🎯 What Are Notch Filters?</h1>

<p>A <b>notch filter</b> (band-stop filter) suppresses a <b>very narrow frequency band</b> while passing all other frequencies.</p>

<h3>🔧 Applications:</h3>
<ul>
  <li>Eliminating interference</li>
  <li>Removing 50/60 Hz hum</li>
  <li>EMI/RFI suppression</li>
  <li>RF tone rejection</li>
  <li>Receiver & mixer filtering</li>
</ul>

<p>Yes — <b>notch filters are widely used in RF systems.</b></p>

<h3>📡 Why does a notch look like S11?</h3>
<p>Because S11 dips when:</p>
<ul>
  <li>Impedance becomes extreme (very high or very low)</li>
  <li>Reflection decreases</li>
  <li>Energy is absorbed or diverted</li>
</ul>

<img width="274" src="https://github.com/user-attachments/assets/2ffa79bb-14ac-4636-bf75-784312635f22" />

<hr>

<h1>📝 Summary</h1>

<ul>
  <li>Single-pole filters are simple but cannot create band-pass or notch responses.</li>
  <li>Two-pole RLC filters allow resonance, sharp roll-off, and selective filtering.</li>
  <li>Output across C → LPF, L → HPF, R → BPF.</li>
  <li>Q-factor controls sharpness and bandwidth.</li>
  <li>Notch filters are essential in RF for interference rejection.</li>
</ul>

<hr>
