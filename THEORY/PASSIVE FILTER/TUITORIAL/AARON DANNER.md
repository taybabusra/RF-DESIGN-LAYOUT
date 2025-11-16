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
<h1 align="center">📘 Lecture 2:Bode plots with one pole filters</h1>
 
For RC low pass filter the time constant is 
