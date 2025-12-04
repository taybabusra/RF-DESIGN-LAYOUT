<h1>📡 Harmonics & Harmonic Distortion (RF Design Guide)</h1>

<h2>🔷 What Are Harmonics?</h2>
<p>
Harmonics are copies of a signal that appear at integer multiples of the fundamental frequency.
They are created by <strong>non-linear devices</strong> such as amplifiers, mixers, and diodes.
</p>

<p>
When a signal passes through a nonlinear device, the output contains:
<ul>
  <li>The fundamental frequency</li>
  <li>Harmonics (2f, 3f, 4f, ...)</li>
</ul>
</p>

<p>
The amplitude of harmonics usually decreases with harmonic order.
High-order harmonics often fall <i>below the noise floor</i>.
</p>

<h2>🔷 What Is the Noise Floor?</h2>
<p>
The <strong>noise floor</strong> is the minimum detectable signal level in a system, caused by:
<ul>
  <li>Thermal noise (kTB)</li>
  <li>Instrument noise (spectrum analyzer, LNA, mixer)</li>
  <li>Environmental noise</li>
</ul>
Signals below the noise floor cannot be accurately measured.
</p>

<h2>🎛 Harmonics: Good or Bad?</h2>

<h3>✔ Useful (Intentional) Harmonics</h3>
<p>
Some systems intentionally generate harmonics, e.g. harmonic mixers, where harmonics of the LO are used to downconvert high-frequency signals.
</p>

<h3>✘ Undesirable Harmonics</h3>
<p>
Most of the time, harmonics are unwanted and are removed using:
<ul>
  <li>Low-pass filters</li>
  <li>Band-pass filters</li>
</ul>
</p>

<p>
Measuring harmonic levels is essential for distortion analysis and regulatory compliance.
</p>

<hr>

<h2>📏 Measuring Harmonics With Zero Span</h2>

<h3>🔷 What Is Zero Span?</h3>
<p>
Zero span mode on a spectrum analyzer stops sweeping frequency and instead measures <strong>amplitude vs. time</strong> at one frequency.
This allows accurate measurement of:
<ul>
  <li>The fundamental</li>
  <li>Each harmonic individually</li>
</ul>
</p>

<hr>

<h1>📉 Harmonic Distortion Metrics</h1>

<h2>1️⃣ Individual Harmonics (dBc)</h2>
<p>
Each harmonic amplitude is measured relative to the fundamental:
<br>
<i>Example: 2nd harmonic = –45 dBc</i>
</p>

<h2>2️⃣ Total Harmonic Distortion (THD)</h2>

<h3>🔷 Why THD Is Important</h3>
<p>
THD shows how much of the output signal power lies in harmonics, indicating how nonlinear the system is.
High THD → more distortion → poorer signal fidelity.
</p>

<h3>🔷 THD Formula</h3>
<pre>
THD = sqrt(V2² + V3² + V4² + ...) / V1
</pre>

<p>Where V1 is the fundamental amplitude and V2, V3... are harmonic amplitudes.</p>

<h3>🔷 THD in dB</h3>
<pre>
THD(dB) = 10 * log10( (P2 + P3 + P4 + ...) / P1 )
</pre>

<h3>✔ Should THD Be Low or High?</h3>
<p><strong>Lower THD is always better.</strong></p>

<ul>
  <li>Low distortion</li>
  <li>Cleaner spectrum</li>
  <li>Less filtering needed</li>
  <li>Better PA/LNA linearity</li>
</ul>

<h3>🔷 THD: Single-Tone vs Multitone</h3>
<p>
THD matters more for:
<ul>
  <li><strong>Single-tone tests</strong> (harmonics only)</li>
</ul>
For multitone signals, <strong>intermodulation distortion (IMD)</strong> becomes dominant and more harmful than harmonics.
</p>

<hr>

<h1>🎚 THD vs THD+N</h1>

<h3>🔷 THD</h3>
<p>Only counts harmonics.</p>

<h3>🔷 THD+N</h3>
<p>
Includes:
<ul>
  <li>Harmonic distortion</li>
  <li>Noise within a measurement bandwidth</li>
</ul>
Important in <strong>audio</strong> and low-level systems.
</p>

<h2>📌 For LNAs: THD or THD+N?</h2>
<p>
Neither is the primary metric.
<br><br>
For LNAs the important specs are:
<ul>
  <li><strong>Noise Figure (NF)</strong></li>
  <li><strong>IIP3 / OIP3</strong> (intermodulation)</li>
  <li><strong>IIP2</strong> (even-order distortion)</li>
  <li><strong>P1dB compression point</strong></li>
  <li><strong>Gain / Stability</strong></li>
</ul>
Harmonic distortion is far less important than <strong>IMD</strong> for LNAs.
</p>

<hr>
<h1>📌 Summary</h1>

<ul>
  <li>Harmonics = multiples of a signal due to nonlinearities</li>
  <li>THD = measure of harmonic distortion (lower is better)</li>
  <li>Zero span = measure amplitude at one frequency</li>
  <li>LNA designers care more about NF and IP3 than THD</li>
  <li>RF systems care more about intermodulation than harmonics</li>
  <li>Filtering is needed to remove harmonics for regulatory compliance</li>
</ul>

