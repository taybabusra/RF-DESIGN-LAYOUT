<h1>📡 Angle Modulation – Full Overview</h1>

<h2>1. What is Angle Modulation?</h2>
<p>
<strong>Angle modulation</strong> is a type of analog modulation in which the
<strong>angle (phase) of a high-frequency carrier</strong> is varied according
to the <strong>instantaneous amplitude of the message signal</strong>, while the
<strong>carrier amplitude remains constant</strong>.
</p>

<p>The angle of a sinusoidal carrier consists of:</p>
<ul>
  <li>Phase</li>
  <li>Frequency (rate of change of phase)</li>
</ul>

<p>Therefore, angle modulation is classified into:</p>
<ul>
  <li><strong>Frequency Modulation (FM)</strong></li>
  <li><strong>Phase Modulation (PM)</strong></li>
</ul>

<hr>

<h2>2. General Expression of Angle-Modulated Signal</h2>

<p>Carrier signal:</p>
<p>
<code>c(t) = A<sub>c</sub> cos(&omega;<sub>c</sub> t)</code>
</p>

<p>Angle-modulated signal:</p>
<p>
<code>s(t) = A<sub>c</sub> cos[&omega;<sub>c</sub> t + &phi;(t)]</code>
</p>

<p>
Where <code>&phi;(t)</code> represents the angle variation caused by the message signal.
</p>

<hr>

<h2>3. Frequency Modulation (FM)</h2>

<h3>Definition</h3>
<p>
In <strong>Frequency Modulation</strong>, the <strong>instantaneous frequency</strong>
of the carrier is varied proportional to the message signal.
</p>

<h3>Mathematical Expression</h3>
<p>
<code>s<sub>FM</sub>(t) = A<sub>c</sub> cos[&omega;<sub>c</sub> t + k<sub>f</sub> ∫ m(t) dt]</code>
</p>

<h3>Instantaneous Frequency</h3>
<p>
<code>f<sub>i</sub>(t) = f<sub>c</sub> + k<sub>f</sub> m(t)</code>
</p>

<h3>Frequency Deviation</h3>
<p>
<code>&Delta;f = k<sub>f</sub> |m(t)|<sub>max</sub></code>
</p>

<h3>FM Modulation Index</h3>
<p>
<code>&beta; = &Delta;f / f<sub>m</sub></code>
</p>

<hr>

<h2>4. Phase Modulation (PM)</h2>

<h3>Definition</h3>
<p>
In <strong>Phase Modulation</strong>, the <strong>phase of the carrier</strong>
is varied directly proportional to the message signal.
</p>

<h3>Mathematical Expression</h3>
<p>
<code>s<sub>PM</sub>(t) = A<sub>c</sub> cos[&omega;<sub>c</sub> t + k<sub>p</sub> m(t)]</code>
</p>

<h3>PM Modulation Index</h3>
<p>
<code>&beta; = k<sub>p</sub> |m(t)|<sub>max</sub></code>
</p>

<h3>Instantaneous Frequency</h3>
<p>
<code>f<sub>i</sub>(t) = f<sub>c</sub> + (k<sub>p</sub>/2&pi;) (dm(t)/dt)</code>
</p>

<p><strong>Key Insight:</strong></p>
<ul>
  <li>FM depends on the <strong>integral</strong> of the message</li>
  <li>PM depends on the <strong>derivative</strong> of the message</li>
</ul>

<hr>

<h2>5. Relationship Between FM and PM</h2>

<table border="1" cellpadding="6">
  <tr>
    <th>Feature</th>
    <th>FM</th>
    <th>PM</th>
  </tr>
  <tr>
    <td>Varied Parameter</td>
    <td>Frequency</td>
    <td>Phase</td>
  </tr>
  <tr>
    <td>Message Dependency</td>
    <td>Integral of m(t)</td>
    <td>m(t)</td>
  </tr>
  <tr>
    <td>Noise Immunity</td>
    <td>Very High</td>
    <td>High</td>
  </tr>
  <tr>
    <td>Bandwidth</td>
    <td>Large</td>
    <td>Large</td>
  </tr>
</table>

<hr>

<h2>6. Narrowband and Wideband Angle Modulation</h2>

<h3>Narrowband Angle Modulation</h3>
<ul>
  <li>Modulation index &beta; &lt;&lt; 1</li>
  <li>Small frequency deviation</li>
  <li>Bandwidth ≈ 2B</li>
</ul>

<h3>Wideband FM</h3>
<ul>
  <li>Modulation index &beta; &gt;&gt; 1</li>
  <li>Large frequency deviation</li>
  <li>Used in FM broadcasting</li>
</ul>

<hr>

<h2>7. Bandwidth of Angle Modulation (Carson’s Rule)</h2>

<p>
<code>BW = 2(&Delta;f + f<sub>m</sub>) = 2f<sub>m</sub>(&beta; + 1)</code>
</p>

<p>
Used for both <strong>FM</strong> and <strong>PM</strong>.
</p>

<hr>

<h2>8. Spectral Characteristics</h2>
<ul>
  <li>Infinite number of sidebands</li>
  <li>Sideband amplitudes follow Bessel functions</li>
  <li>Total transmitted power remains constant</li>
</ul>

<hr>

<h2>9. Noise Performance</h2>

<p>
Angle modulation offers superior noise immunity because noise mainly affects
<strong>amplitude</strong>, while information is carried in
<strong>frequency or phase</strong>.
</p>

<table border="1" cellpadding="6">
  <tr>
    <th>Modulation</th>
    <th>Noise Immunity</th>
  </tr>
  <tr>
    <td>AM</td>
    <td>Poor</td>
  </tr>
  <tr>
    <td>PM</td>
    <td>Better</td>
  </tr>
  <tr>
    <td>FM</td>
    <td>Best</td>
  </tr>
</table>

<hr>

<h2>10. Generation of Angle Modulation</h2>

<h3>FM Generation</h3>
<ul>
  <li>Direct FM using VCO</li>
  <li>Indirect FM (Armstrong Method)</li>
</ul>

<h3>PM Generation</h3>
<ul>
  <li>Phase modulator</li>
  <li>Balanced modulator with phase shifter</li>
</ul>

<hr>

<h2>11. Detection (Demodulation)</h2>

<h3>FM Detectors</h3>
<ul>
  <li>Foster–Seeley discriminator</li>
  <li>Ratio detector</li>
  <li>PLL FM detector</li>
</ul>

<h3>PM Detector</h3>
<ul>
  <li>Phase detector</li>
  <li>PLL-based demodulator</li>
</ul>

<hr>

<h2>12. Advantages</h2>
<ul>
  <li>High noise immunity</li>
  <li>Constant envelope</li>
  <li>Better SNR than AM</li>
</ul>

<h2>13. Disadvantages</h2>
<ul>
  <li>Large bandwidth requirement</li>
  <li>Higher circuit complexity</li>
</ul>

<hr>

<h2>14. Applications</h2>

<table border="1" cellpadding="6">
  <tr>
    <th>Application</th>
    <th>Modulation</th>
  </tr>
  <tr>
    <td>FM Radio Broadcasting</td>
    <td>FM</td>
  </tr>
  <tr>
    <td>TV Audio</td>
    <td>FM</td>
  </tr>
  <tr>
    <td>Two-way Radio</td>
    <td>FM</td>
  </tr>
  <tr>
    <td>Satellite & Telemetry</td>
    <td>PM</td>
  </tr>
</table>

<hr>

<h2>15. One-Line Exam Summary</h2>
<p>
<strong>
Angle modulation varies the frequency or phase of a carrier according to the
message signal, providing excellent noise performance at the expense of larger bandwidth.
</strong>
</p>

