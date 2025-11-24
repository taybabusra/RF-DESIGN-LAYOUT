<h1 align="center">5-GHz Power Amplifier Design</h1>

<hr/>

<h2>1️⃣ Design Specifications</h2>

<table>
  <tr><th>Parameter</th><th>Target</th></tr>
  <tr><td>Supply Current</td><td>≥ 10 mA</td></tr>
  <tr><td>Power Gain</td><td>10 dB</td></tr>
  <tr><td>Operating Frequency</td><td>5 GHz</td></tr>
</table>

<hr/>

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

<hr/>

<h2>3️⃣ Circuit Schematic (Before Matching)</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/27297d19-31c7-4e5c-ab74-140598e4c589" width="600"/>
</p>

<hr/>

<h2>4️⃣ Simulation Result — Before Matching</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/1f58641a-2d94-4c44-8de2-d7db7bf1ef1f" width="900"/>
</p>

<p>The circuit is unconditionally stable, but gain is below target due to unmatched input/output.</p>

<hr/>

<h2>5️⃣ Input Matching Network</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/dba9d82c-3a9d-4ff9-9105-521d2d91e639" width="600"/>
</p>

<hr/>

<h2>6️⃣ Output Matching Network</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/6da56475-eb55-43af-bd1b-d4004ce0e3a7" width="600"/>
</p>

<hr/>

<h2>7️⃣ Final PA Circuit After Matching</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/57db9f80-2b69-4aca-bfa2-ecaa228a2a41" width="700"/>
</p>

<hr/>

<h2>8️⃣ Final Simulation — After Matching</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a7a9771e-412b-42f8-be7b-a73e58abc694" width="700"/>
</p>

<hr/>

<h2>✅ Summary</h2>

<ul>
  <li>Input and output are fully complex-conjugate matched.</li>
  <li>Final gain meets the 10 dB requirement at 5 GHz.</li>
  <li>Stability preserved after matching.</li>
  <li>T-network matching (Q = 5) used for both ports.</li>
</ul>

<hr/>
