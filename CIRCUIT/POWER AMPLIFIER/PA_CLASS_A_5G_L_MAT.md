<h1>5-GHz Power Amplifier (PA) Design</h1>

<hr>

<h2>1️⃣ Design Specifications</h2>

<table>
<tr><th>Parameter</th><th>Target</th></tr>
<tr><td>Supply Current</td><td>≥ 10 mA</td></tr>
<tr><td>Power Gain</td><td>10 dB</td></tr>
<tr><td>Operating Frequency</td><td>5 GHz</td></tr>
</table>

<hr>

<h2>2️⃣ Device & Circuit Parameters (Before Matching)</h2>

<table>
<tr><th>Parameter</th><th>Value</th></tr>
<tr><td>Transistor Width (W)</td><td>1 µm</td></tr>
<tr><td>Number of Fingers (M)</td><td>60</td></tr>
<tr><td>Source Inductor (L)</td><td>100 nH</td></tr>
<tr><td>PA Load Inductor (L<sub>PA</sub>)</td><td>10 nH</td></tr>
<tr><td>Bias Inductor</td><td>100 pH</td></tr>
<tr><td>Drain Resistance (R)</td><td>360 Ω</td></tr>
<tr><td>Gate Bias Voltage (V<sub>BIAS</sub>)</td><td>550 mV</td></tr>
<tr><td>Supply Voltage (V<sub>DD</sub>)</td><td>600 mV</td></tr>
</table>

<hr>

<h2>3️⃣ Circuit Schematic (Before Matching)</h2>
<img src="https://github.com/user-attachments/assets/27297d19-31c7-4e5c-ab74-140598e4c589" width="600">

<hr>

<h2>4️⃣ Simulation Result — Before Matching</h2>
<img src="https://github.com/user-attachments/assets/1f58641a-2d94-4c44-8de2-d7db7bf1ef1f" width="600">

<p><b>Observation:</b> The circuit is unconditionally stable, but gain is below target due to unmatched input/output.</p>

<hr>

<h2>5️⃣ Input Matching Network</h2>
<img src="https://github.com/user-attachments/assets/dba9d82c-3a9d-4ff9-9105-521d2d91e639" width="600">

<hr>

<h2>6️⃣ Output Matching Network</h2>
<img src="https://github.com/user-attachments/assets/6da56475-eb55-43af-bd1b-d4004ce0e3a7" width="600">

<hr>

<h2>7️⃣ Final PA Circuit After Matching</h2>
<img src="https://github.com/user-attachments/assets/57db9f80-2b69-4aca-bfa2-ecaa228a2a41" width="600">

<hr>

<h2>8️⃣ Final Simulation — After Matching</h2>

<img src="https://github.com/user-attachments/assets/a7a9771e-412b-42f8-be7b-a73e58abc694" width="600">
<br>
<img src="https://github.com/user-attachments/assets/ff5a6cfe-2dc1-4a9a-bcdd-cd7e81cea892" width="600">

<ul>
<li>Input and output are fully complex-conjugate matched.</li>
<li>Final gain meets the 10 dB requirement at 5 GHz.</li>
<li>Stability preserved after matching.</li>
<li>T-network matching (Q = 5) used for both ports.</li>
</ul>

<hr>

<h2>9️⃣ Small-Signal Analysis</h2>

<h3>9.1 Maximum Gain vs Frequency (G<sub>max</sub>)</h3>
<img src="https://github.com/user-attachments/assets/cf3e112c-8a6a-4d38-8722-70a9b04dd969" width="600">

<h3>9.2 MSG vs Frequency (G<sub>MSG</sub>)</h3>
<img src="https://github.com/user-attachments/assets/b908cac6-1781-4c81-b119-990538d82417" width="600">
<p><b>Q:</b> Why is S21 not 18.25 dB?</p>

<h3>9.3 Minimum Noise Figure (NF<sub>min</sub>) vs Frequency</h3>
<img src="https://github.com/user-attachments/assets/51b6d0f8-45e0-4d20-b680-4eae04f2c9c2" width="600">

<h3>9.4 Noise Figure (NF) vs Frequency</h3>
<img src="https://github.com/user-attachments/assets/569c251a-747e-41a9-bc03-4125330ad98e" width="600">

<h3>9.5 Transducer Gain (G<sub>T</sub>) vs Frequency</h3>
<img src="https://github.com/user-attachments/assets/a7899430-78b2-4361-a792-ca4e6fa5aa7c" width="600">

<h3>9.6 Available Gain (G<sub>A</sub>) vs Frequency</h3>
<img src="https://github.com/user-attachments/assets/97194cd9-13ac-4890-a1d7-07d1b2bead9d" width="600">

<h3>9.7 Power Gain (G<sub>P</sub>) vs Frequency</h3>
<img src="https://github.com/user-attachments/assets/b989c0b4-8cfd-4fd1-8cea-5cd9f50b5d92" width="600">
<p><b>Q:</b> Without connecting anything at the port, how are these values obtained?</p>

<h3>9.8 Noise Circle (NC) on Smith Chart</h3>
<img src="https://github.com/user-attachments/assets/849edb08-1f3e-408e-858b-773941630e8a" width="450">
<img src="https://github.com/user-attachments/assets/c4b62e21-06e5-48c3-9c77-eb3205f2c5f2" width="450">

<h3>9.9 Gain vs Frequency (GAC)</h3>
<!-- Add image if you have it -->

<h3>9.10 Single-Sideband (SSB)</h3>
<img src="https://github.com/user-attachments/assets/ceb992af-57fe-4c8c-8157-8fc655273ecb" width="600">

<hr>

<h2>🔟 Notes</h2>
<ul>
<li>All matching networks are designed to maximize gain and minimize noise figure.</li>
<li>Simulation confirms PA meets design targets at 5 GHz.</li>
<li>Small-signal parameters reveal intrinsic transistor behavior.</li>
</ul>

<hr>

<h1>11️⃣ Harmonic Balance (HB) Simulation</h1>

<h3>11.1 Voltage</h3>
<img src="https://github.com/user-attachments/assets/fc106501-d18b-477b-93f8-e46ed9db07f6" width="250">
<img src="https://github.com/user-attachments/assets/26ef3b94-0ad2-4cd7-aafb-507262fcbd6f" width="600">

<hr>

<h3>11.2 Power Gain</h3>
<img src="https://github.com/user-attachments/assets/e7e26f75-9145-4217-8adf-066a4797c806" width="250">
<img src="https://github.com/user-attachments/assets/e54647e0-3634-4a7b-8b29-98b7712f43fd" width="600">

<hr>

<h3>11.3 Current Gain</h3>
<p>(Add image if available)</p>

<hr>

<h3>11.4 1 dB Compression Point</h3>

<b>Input-Referred 1 dB Compression:</b><br>
<img src="https://github.com/user-attachments/assets/895a3e32-1aee-44d4-aac5-c8b97b1a5e07" width="600"><br><br>

<b>Output-Referred 1 dB Compression:</b><br>
<img src="https://github.com/user-attachments/assets/0b039877-66a3-4690-9e06-52b4d433790b" width="600">

<hr>

<h3>11.5 Input Relation vs Gain</h3>
<img src="https://github.com/user-attachments/assets/1aee5ba4-33ca-44fc-8c47-1cbd3dfc76ec" width="800">

<hr>

<h3>11.6 Output Relation vs Gain</h3>
<img src="https://github.com/user-attachments/assets/197c6a4d-5f24-42e9-984e-4d49892246f2" width="800">

<hr>

<h3>11.7 Harmonic Distortion</h3>

<b>Input Harmonic Distortion:</b><br>
<img src="https://github.com/user-attachments/assets/6525bf2c-8678-48db-ab8c-71b6b8ab3b90" width="450"><br><br>

<b>Output Harmonic Distortion:</b><br>
<img src="https://github.com/user-attachments/assets/b4be8f12-595c-4f99-9c55-04441e08ca09" width="800">

<hr>
