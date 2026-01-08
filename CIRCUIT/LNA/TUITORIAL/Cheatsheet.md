<h1>📡 Low Noise Amplifier (LNA) – Complete Engineer Cheatsheet</h1>

<p>
This document is a <b>ready-to-use RFIC LNA reference</b> covering:
<ul>
  <li>All major LNA circuit topologies</li>
  <li>What each topology does</li>
  <li>When to use it</li>
  <li>What every engineer must check before & after design</li>
</ul>
</p>

<hr>

<h2>1️⃣ Common Source (CS) LNA</h2>

<img src="images/cs_lna.png" alt="Common Source LNA Schematic" width="400">

<h4>Description</h4>
<p>
A voltage amplifier using a MOSFET in common-source configuration.
</p>

<h4>Key Characteristics</h4>
<ul>
  <li>High gain</li>
  <li>Moderate noise figure</li>
  <li>Poor reverse isolation (Miller effect)</li>
</ul>

<h4>Key Equations</h4>
<p>
Gain: <b>A<sub>v</sub> ≈ g<sub>m</sub> · R<sub>L</sub></b><br>
Noise Figure: <b>NF ≈ 1 + γ / (g<sub>m</sub>R<sub>S</sub>)</b>
</p>

<hr>

<h2>2️⃣ Inductively Degenerated CS LNA (MOST USED)</h2>

<img src="images/inductive_degeneration_lna.png" alt="Inductive Degeneration LNA" width="400">

<h4>Why This Topology Is Popular</h4>
<ul>
  <li>Simultaneous noise and input matching</li>
  <li>Excellent stability</li>
  <li>Low noise figure</li>
</ul>

<h4>Important Result</h4>
<p>
Input impedance can be matched to 50Ω using source inductor:
<br>
<b>Z<sub>in</sub> ≈ ω²L<sub>s</sub>C<sub>gs</sub>/g<sub>m</sub></b>
</p>

<h4>Applications</h4>
<ul>
  <li>Wi-Fi</li>
  <li>Bluetooth</li>
  <li>GPS</li>
</ul>

<hr>

<h2>3️⃣ Common Gate (CG) LNA</h2>

<img src="images/common_gate_lna.png" alt="Common Gate LNA" width="400">

<h4>Description</h4>
<p>
Input applied at the source; gate is AC grounded.
</p>

<h4>Key Property</h4>
<p>
<b>Z<sub>in</sub> ≈ 1/g<sub>m</sub></b> → easy wideband matching
</p>

<h4>Pros & Cons</h4>
<ul>
  <li>✔ Wideband</li>
  <li>✔ Excellent stability</li>
  <li>✘ Higher NF than CS</li>
</ul>

<hr>

<h2>4️⃣ Cascode LNA (CS + CG)</h2>

<img src="images/cascode_lna.png" alt="Cascode LNA" width="400">

<h4>Why Cascode?</h4>
<ul>
  <li>Suppresses Miller effect</li>
  <li>Improves gain and isolation</li>
  <li>Enhances stability</li>
</ul>

<h4>Tradeoff</h4>
<p>
Requires higher voltage headroom.
</p>

<hr>

<h2>5️⃣ Resistive Feedback LNA</h2>

<img src="images/resistive_feedback_lna.png" alt="Resistive Feedback LNA" width="400">

<h4>Description</h4>
<p>
Feedback resistor from output to input provides broadband matching.
</p>

<h4>Key Points</h4>
<ul>
  <li>Wideband operation</li>
  <li>Robust against PVT variation</li>
  <li>Higher NF due to feedback resistor</li>
</ul>

<hr>

<h2>6️⃣ Current Reuse LNA</h2>

<img src="images/current_reuse_lna.png" alt="Current Reuse LNA" width="400">

<h4>Core Idea</h4>
<p>
Multiple gain stages share the same DC current.
</p>

<h4>Advantages</h4>
<ul>
  <li>Low power consumption</li>
  <li>High gain per mA</li>
</ul>

<h4>Drawback</h4>
<p>
Limited voltage headroom.
</p>

<hr>

<h2>7️⃣ Differential LNA</h2>

<img src="images/differential_lna.png" alt="Differential LNA" width="400">

<h4>Definition</h4>
<p>
Two symmetric signal paths producing differential outputs (V<sub>out+</sub>, V<sub>out−</sub>).
</p>

<h4>Benefits</h4>
<ul>
  <li>Even-order distortion cancellation</li>
  <li>Better PSRR</li>
  <li>Higher immunity to substrate noise</li>
</ul>

<hr>

<h2>8️⃣ Balun LNA (Single-Ended → Differential)</h2>

<img src="images/balun_lna.png" alt="Balun LNA" width="400">

<h4>Important Note</h4>
<p>
Input is single-ended, output is differential.
<br>
This is <b>NOT</b> a fully differential LNA.
</p>

<h4>Use Case</h4>
<ul>
  <li>CMOS RFICs without off-chip baluns</li>
</ul>

<hr>

<h2>9️⃣ Noise-Canceling LNA</h2>

<img src="images/noise_canceling_lna.png" alt="Noise Canceling LNA" width="400">

<h4>Concept</h4>
<p>
Noise from the input transistor is sensed and canceled while the signal adds constructively.
</p>

<h4>Advantage</h4>
<p>
Breaks the noise limitation of common-gate LNAs.
</p>

<hr>

<h2>🔍 BEFORE Designing an LNA</h2>

<ul>
  <li>Target frequency & bandwidth</li>
  <li>Noise figure requirement</li>
  <li>Gain target</li>
  <li>Linearity (IIP3, P1dB)</li>
  <li>Supply voltage & power budget</li>
  <li>Single-ended or differential</li>
  <li>Technology (CMOS / SiGe)</li>
</ul>

<hr>

<h2>✅ AFTER Designing an LNA</h2>

<ul>
  <li>S11 &lt; −10 dB</li>
  <li>S21 meets gain target</li>
  <li>Stability factor K &gt; 1</li>
  <li>Noise figure across band</li>
  <li>IIP3 & P1dB verification</li>
  <li>PVT & Monte Carlo checks</li>
</ul>

<hr>

<h2>⚠️ Common Mistakes</h2>

<ul>
  <li>Calling a CS LNA differential</li>
  <li>Ignoring gate resistance noise</li>
  <li>Ignoring low-frequency stability</li>
  <li>Assuming matching always minimizes NF</li>
</ul>

<hr>

<h2>🎯 One-Line Master Statement</h2>

<p>
<b>
A good LNA simultaneously optimizes noise, gain, matching, linearity, and stability for the required bandwidth under power and technology constraints.
</b>
</p>
