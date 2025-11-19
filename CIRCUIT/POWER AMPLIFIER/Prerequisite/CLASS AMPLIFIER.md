<h1 align="center">📘 Complete Guide to Amplifier Classes (BJT & MOSFET)</h1>
<p align="center"><b>Designed for Analog IC, RF, and Layout Engineers</b></p>

<hr>

<h2>📌 What is Amplifier Efficiency?</h2>
<p>
Efficiency (η) is the ratio of useful AC output power delivered to the load to the total DC power consumed:
</p>

<pre>
η = P<sub>AC-load</sub> / P<sub>DC</sub>
</pre>

<hr>

<h1>🅰️ CLASS A AMPLIFIER</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Conduction angle: <b>360°</b></li>
  <li>Transistor conducts for the entire input cycle</li>
  <li>Very low distortion</li>
  <li>Poor efficiency: <b>25% (resistive load)</b></li>
  <li>Better efficiency: <b>50% (transformer-coupled)</b></li>
  <li>Used in: small-signal amplifiers, LNAs, analog stages</li>
</ul>

<h2>✔ What is the Q-Point?</h2>
<p>The <b>Q-point (Quiescent Point)</b> is the DC operating point — the perfectly centered point on the load line where the transistor stays active without clipping.</p>

<h3>Typical BJT Bias:</h3>
<pre>
V<sub>CE</sub> = ½ V<sub>CC</sub>
V<sub>BE</sub> ≈ 0.6–0.7 V
I<sub>C</sub> = β I<sub>B</sub>
β = h<sub>FE</sub>
</pre>

<img width="514" height="285" src="https://github.com/user-attachments/assets/0bfa58e5-59b7-4863-9d67-5ce8426eff53" />

<h2>✔ Improving Class A Efficiency</h2>
<p>Replace the load resistor <b>RC</b> with a <b>transformer-coupled load</b>:</p>

<ul>
  <li>AC swing becomes symmetric</li>
  <li>DC voltage is not wasted across RC</li>
  <li>Energy stored in magnetic field improves transfer</li>
</ul>

<p><b>Efficiency doubles → 50%</b></p>

<img width="503" height="287" src="https://github.com/user-attachments/assets/fbe2f706-2e86-4a3e-b119-d4f8ab0ca55a" />

<hr>

<h1>🅱️ CLASS B AMPLIFIER</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Conduction: <b>180°</b></li>
  <li>Two complementary BJTs/MOSFETs (Push–Pull)</li>
  <li>Theoretical efficiency: <b>78.5%</b></li>
  <li>Bias at <b>cutoff</b></li>
</ul>

<img width="507" height="305" src="https://github.com/user-attachments/assets/6f6f30c7-ab5c-408e-a70e-e084eaf717eb" />

<h2>❌ Problem: Crossover Distortion</h2>
<p>Occurs when both transistors are off near 0V.</p>

<h3>✔ Solution: Class AB Biasing</h3>
<p>Add small diodes or V<sub>BE</sub> multipliers to pre-bias transistors slightly above cutoff.</p>

<img width="512" height="298" src="https://github.com/user-attachments/assets/38c0b775-a8c1-4869-bd99-b19b5f2c3857" />

<hr>

<h1>🅰️🅱️ CLASS AB AMPLIFIER</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Conduction angle: <b>180°–360°</b></li>
  <li>Fixes crossover distortion</li>
  <li>Efficiency between Class A and B</li>
  <li>Widely used in Audio, Medium-Power RF drivers</li>
</ul>

<hr>

<h1>🅲 CLASS C AMPLIFIER</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Conduction: <b>&lt; 180°</b></li>
  <li>Highly non-linear → used only in <b>RF</b></li>
  <li>Efficiency: <b>high</b> (≈ 80–90%)</li>
  <li>Requires resonant LC tank to reconstruct the signal</li>
</ul>

<img width="469" height="248" src="https://github.com/user-attachments/assets/2257671b-f7b0-478b-a94e-402860be0f73" />

<hr>

<h1>🅳 CLASS D (Switching) AMPLIFIER</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Transistors operate as <b>switches</b></li>
  <li>PWM or PDM signal</li>
  <li>Efficiency: <b>90–95%</b></li>
  <li>Used in audio, power conversion</li>
</ul>

<h3>Design & Layout Focus</h3>
<ul>
  <li>Dead-time control</li>
  <li>Minimize switching losses</li>
  <li>Low-parasitic layout</li>
</ul>

<hr>

<h1>🅴 CLASS E (Switching RF PA)</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Zero-Voltage Switching (ZVS) operation</li>
  <li>Very high efficiency: <b>> 90%</b></li>
  <li>Used in RF transmitters</li>
  <li>Requires precise LC tuning + transistor shaping network</li>
</ul>

<hr>

<h1>🅵 CLASS F (Harmonic-Tuned PA)</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Uses harmonic traps to shape voltage/current waveforms</li>
  <li>Excellent efficiency (80–90%)</li>
  <li>Used in RF Power Amplifiers</li>
</ul>

<h3>Layout Focus</h3>
<ul>
  <li>Transmission line accuracy</li>
  <li>On-chip inductors with correct Q factor</li>
</ul>

<hr>

<h1>🅶 / 🅷 CLASS G & H</h1>

<h2>✔ Key Properties</h2>
<ul>
  <li>Use multiple or dynamically switching supply rails</li>
  <li>Improved efficiency for audio amplifiers</li>
</ul>

<hr>

<h1>🏁 SUMMARY TABLE (Quick View)</h1>

<table border="1" cellpadding="8">
<tr>
  <th>Class</th>
  <th>Conduction</th>
  <th>Efficiency</th>
  <th>Use Case</th>
  <th>Key Circuit Focus</th>
  <th>Key Layout Focus</th>
</tr>

<tr>
  <td>A</td>
  <td>360°</td>
  <td>Low (25–50%)</td>
  <td>LNA, Analog Stages</td>
  <td>Biasing, Linearity</td>
  <td>Device matching, noise minimization</td>
</tr>

<tr>
  <td>B</td>
  <td>180°</td>
  <td>Medium (~78%)</td>
  <td>Push–Pull</td>
  <td>Crossover distortion</td>
  <td>Symmetry, thermal matching</td>
</tr>

<tr>
  <td>AB</td>
  <td>180°–360°</td>
  <td>Medium</td>
  <td>Audio, RF Drivers</td>
  <td>gm linearity, bias control</td>
  <td>Thermal coupling, matching</td>
</tr>

<tr>
  <td>C</td>
  <td>&lt; 180°</td>
  <td>High</td>
  <td>RF Power Amplifier</td>
  <td>Tank design, resonance</td>
  <td>Inductor layout, high-Q routing</td>
</tr>

<tr>
  <td>D</td>
  <td>Switching</td>
  <td>Very High</td>
  <td>Audio, Power</td>
  <td>Dead-time, switching loss</td>
  <td>Low parasitics, current routing</td>
</tr>

<tr>
  <td>E</td>
  <td>Switching RF</td>
  <td>Very High</td>
  <td>RF PA</td>
  <td>ZVS, LC tuning</td>
  <td>PA routing, thermal design</td>
</tr>

<tr>
  <td>F</td>
  <td>Harmonic tuned</td>
  <td>Very High</td>
  <td>RF PA</td>
  <td>Harmonic shaping</td>
  <td>Transmission-line layout</td>
</tr>

<tr>
  <td>G/H</td>
  <td>Dynamic rails</td>
  <td>High</td>
  <td>Audio</td>
  <td>Supply tracking</td>
  <td>Multiple-rail routing</td>
</tr>
</table>

<hr>

<h2>🎯 Final Notes for Circuit & Layout Engineer</h2>

<ul>
  <li><b>Circuit Engineer:</b> focus on biasing, linearity, harmonic control, PA stability.</li>
  <li><b>Layout Engineer:</b> emphasize symmetry, matching, parasitic reduction, current-handling, EM-aware routing.</li>
  <li><b>RF PA:</b> pay special attention to inductors, capacitors, transmission lines, grounding.</li>
</ul>

<hr>

<p align="center"><b>2nd source of opinione</b></p>

