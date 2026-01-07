<h1>Error Vector Magnitude (EVM)</h1>

<p>
<b>Error Vector Magnitude (EVM)</b> is a key performance metric used in digital communication systems
to quantify modulation accuracy. It measures how far the received signal deviates from the ideal
constellation points in the IQ plane.
</p>

<hr>

<h2>1. Concept of EVM</h2>
<p>
In an ideal system, each received symbol lies exactly on its intended constellation point.
Due to noise and hardware impairments, the received symbol is displaced.
The vector difference between the ideal and measured symbol is called the <b>error vector</b>.
</p>

<p><b>EVM measures the magnitude of this error vector.</b></p>

<hr>

<h2>2. Mathematical Definition</h2>

<p><b>Error Vector:</b></p>
<p>
S<sub>error</sub> = S<sub>measured</sub> − S<sub>ideal</sub>
</p>

<p><b>RMS EVM:</b></p>
<p>
EVM<sub>RMS</sub> =
√( Σ |S<sub>measured</sub> − S<sub>ideal</sub>|² / Σ |S<sub>ideal</sub>|² )
</p>

<p><b>EVM Percentage:</b></p>
<p>
EVM(%) = EVM<sub>RMS</sub> × 100
</p>

<p><b>EVM in dB:</b></p>
<p>
EVM(dB) = 20 log<sub>10</sub>(EVM<sub>RMS</sub>)
</p>

<hr>

<h2>3. RMS EVM vs Peak EVM</h2>

<table border="1" cellpadding="6" cellspacing="0">
<tr>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>RMS EVM</td>
<td>Average error over all symbols (most commonly used)</td>
</tr>
<tr>
<td>Peak EVM</td>
<td>Maximum error observed for any symbol</td>
</tr>
</table>

<hr>

<h2>4. Causes of High EVM</h2>

<ul>
<li>Thermal noise</li>
<li>Phase noise</li>
<li>Frequency offset</li>
<li>I/Q imbalance</li>
<li>Power amplifier nonlinearity</li>
<li>Timing jitter</li>
</ul>

<p>
EVM captures the combined effect of all these impairments.
</p>

<hr>

<h2>5. Relationship Between EVM and SNR</h2>

<p>
For many systems (approximation):
</p>

<p>
EVM<sub>RMS</sub> ≈ 1 / √SNR
</p>

<p>
SNR(dB) ≈ −20 log<sub>10</sub>(EVM)
</p>

<p>
Example:
<ul>
<li>EVM = 10% → SNR ≈ 20 dB</li>
<li>EVM = 3% → SNR ≈ 30 dB</li>
</ul>
</p>

<hr>

<h2>6. Typical EVM Requirements</h2>

<table border="1" cellpadding="6" cellspacing="0">
<tr>
<th>Modulation</th>
<th>Max EVM (%)</th>
</tr>
<tr>
<td>QPSK</td>
<td>≈ 17.5%</td>
</tr>
<tr>
<td>16-QAM</td>
<td>≈ 12.5%</td>
</tr>
<tr>
<td>64-QAM</td>
<td>≈ 8%</td>
</tr>
<tr>
<td>256-QAM</td>
<td>≈ 3.5%</td>
</tr>
<tr>
<td>1024-QAM</td>
<td>≈ 2%</td>
</tr>
</table>

<hr>

<h2>7. Importance of EVM</h2>

<ul>
<li>Directly measures modulation quality</li>
<li>Includes all RF and baseband impairments</li>
<li>Faster than BER measurement</li>
<li>Widely used in LTE, 5G, Wi-Fi, SDR, and RF IC testing</li>
</ul>

<hr>

<h2>8. EVM vs BER</h2>

<table border="1" cellpadding="6" cellspacing="0">
<tr>
<th>EVM</th>
<th>BER</th>
</tr>
<tr>
<td>Measures signal quality</td>
<td>Measures bit errors</td>
</tr>
<tr>
<td>Fast to measure</td>
<td>Requires long data streams</td>
</tr>
<tr>
<td>Hardware-oriented metric</td>
<td>System-level metric</td>
</tr>
</table>

<hr>

<h2>9. One-Line Summary</h2>

<p>
<b>Error Vector Magnitude (EVM) is the RMS magnitude of the difference between measured and ideal
constellation points, normalized to the ideal signal power, and is a primary indicator of
digital modulation quality.</b>
</p>

