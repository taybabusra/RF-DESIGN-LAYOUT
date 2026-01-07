<h1>Quadrature Phase Shift Keying (QPSK)</h1>

<p>
Quadrature Phase Shift Keying (QPSK) is a digital modulation scheme that transmits
<strong>two bits per symbol</strong> by modulating the phase of a carrier using
<strong>two orthogonal components</strong>: In-phase (I) and Quadrature (Q).
It is one of the most widely used modulation schemes in modern communication systems.
</p>

<hr>

<h2>1. Fundamental Concept</h2>

<p>
QPSK can be viewed as <strong>two independent BPSK signals</strong> transmitted simultaneously
on orthogonal carriers:
</p>

<ul>
  <li>In-phase component: <code>cos(2πf<sub>c</sub>t)</code></li>
  <li>Quadrature component: <code>sin(2πf<sub>c</sub>t)</code></li>
</ul>

<p>
This orthogonality allows QPSK to double the data rate without increasing bandwidth.
</p>

<hr>

<h2>2. Mathematical Signal Model</h2>

<h3>Passband Representation</h3>

<p>
The transmitted QPSK signal is:
</p>

<pre>
s(t) = √(2E<sub>s</sub>/T<sub>s</sub>) [ I<sub>k</sub> cos(2πf<sub>c</sub>t) − Q<sub>k</sub> sin(2πf<sub>c</sub>t) ]
</pre>

<p>
where:
</p>

<ul>
  <li><code>I<sub>k</sub>, Q<sub>k</sub> ∈ {+1, −1}</code></li>
  <li><code>E<sub>s</sub> = 2E<sub>b</sub></code></li>
  <li><code>T<sub>s</sub> = 2T<sub>b</sub></code></li>
</ul>

<h3>Phase Representation</h3>

<pre>
s(t) = √(2E<sub>s</sub>/T<sub>s</sub>) cos(2πf<sub>c</sub>t + θ<sub>k</sub>)
</pre>

<p>
with:
</p>

<pre>
θ<sub>k</sub> ∈ { ±π/4, ±3π/4 }
</pre>

<hr>

<h2>3. Constellation and Gray Coding</h2>

<p>
QPSK uses four constellation points equally spaced by 90°. Gray coding is applied
to minimize bit errors.
</p>

<table border="1" cellpadding="6">
  <tr>
    <th>Bits</th>
    <th>Phase</th>
  </tr>
  <tr>
    <td>00</td>
    <td>+45°</td>
  </tr>
  <tr>
    <td>01</td>
    <td>+135°</td>
  </tr>
  <tr>
    <td>11</td>
    <td>−135°</td>
  </tr>
  <tr>
    <td>10</td>
    <td>−45°</td>
  </tr>
</table>

<p>
With Gray coding, adjacent constellation points differ by only one bit, reducing BER.
</p>

<hr>

<h2>4. Spectral Efficiency and Bandwidth</h2>

<p>
Symbol rate and bit rate are related as:
</p>

<pre>
R<sub>s</sub> = R<sub>b</sub>/2
</pre>

<p>
With raised-cosine pulse shaping:
</p>

<pre>
BW = (1 + α)R<sub>s</sub> = (1 + α)R<sub>b</sub>/2
</pre>

<p>
Thus, QPSK achieves <strong>twice the data rate of BPSK</strong> for the same bandwidth.
</p>

<hr>

<h2>5. Bit Error Rate (BER)</h2>

<p>
In an AWGN channel, the BER of QPSK is:
</p>

<pre>
P<sub>b</sub> = Q( √(2E<sub>b</sub>/N<sub>0</sub>) )
</pre>

<p>
This is identical to BPSK because each bit is carried independently on the I and Q channels.
</p>

<hr>

<h2>6. QPSK Transmitter Architecture</h2>

<ul>
  <li>Serial-to-parallel bit conversion</li>
  <li>Gray-coded symbol mapping</li>
  <li>Pulse shaping (Root Raised Cosine)</li>
  <li>I/Q modulation using cosine and sine carriers</li>
  <li>Summation and RF upconversion</li>
</ul>

<p>
In RFIC design, amplitude and phase matching between I and Q paths is critical.
</p>

<hr>

<h2>7. QPSK Receiver Architecture</h2>

<ul>
  <li>RF downconversion</li>
  <li>Carrier recovery (Costas loop)</li>
  <li>Matched filtering</li>
  <li>Symbol timing recovery</li>
  <li>I/Q detection and decision logic</li>
</ul>

<hr>

<h2>8. Practical RF Impairments</h2>

<ul>
  <li><strong>I/Q imbalance:</strong> Gain and phase mismatch distort the constellation</li>
  <li><strong>Phase noise:</strong> Causes constellation rotation and EVM degradation</li>
  <li><strong>Frequency offset:</strong> Continuous phase rotation</li>
  <li><strong>PA nonlinearity:</strong> Pulse shaping introduces envelope variation</li>
</ul>

<hr>

<h2>9. Important QPSK Variants</h2>

<ul>
  <li><strong>OQPSK:</strong> I and Q staggered to avoid 180° phase jumps</li>
  <li><strong>π/4-QPSK:</strong> Limits phase transitions and reduces spectral splatter</li>
</ul>

<p>
These variants are preferred in practical RF transmitters.
</p>

<hr>

<h2>10. Error Vector Magnitude (EVM)</h2>

<pre>
EVM = √( E[|S<sub>error</sub>|²] / E[|S<sub>ideal</sub>|²] )
</pre>

<p>
Typical QPSK systems require:
</p>

<ul>
  <li>EVM &lt; 17.5%</li>
</ul>

<hr>

<h2>11. Applications</h2>

<ul>
  <li>LTE uplink</li>
  <li>Satellite communication (DVB-S)</li>
  <li>Wi-Fi control channels</li>
  <li>GPS</li>
  <li>Optical coherent communication</li>
</ul>

<hr>

<h2>12. Key Takeaway</h2>

<p>
QPSK provides an optimal balance between spectral efficiency, power efficiency,
and implementation complexity, making it a fundamental modulation scheme in
modern digital communication and RF IC design.
</p>
