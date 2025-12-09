
Q: how transmission line bridges the gap
Q: the pheomenon of wave propagation on transmission line can be approached from an extention of circuit theoury or from a specialization of Maxwell equation.


Article 2.1:
- key difference between circuit theory and transmission line theory is electrical size. -- Electrical length(link)
- Transmission line is a distributed parameter network, where voltages and current can vary in magnitude and phase over it's length.
- To from a transmission line it's mandetory to have a two conductor and dielectric in betwen for wave propagation.

Component of transmission line for a small section:

<img width="216" height="160" alt="image" src="https://github.com/user-attachments/assets/1b934067-84b7-40e3-a50f-7bc0169d8563" />

These parameters are coming from where:
R: line resitance as they are not lossless
L: Magnetic field around conductor
C: electric field around conductor
G: Dielectric loss 
Here R,G are represent the loss.
When we are talking about lossless line we don't count for them.

## CHAT
<!-- README.md: Transmission-line equations (2.1a → 2.3b) + Maxwell curl (phasor) -->

<!-- MathJax for local previewers / static site generators that allow external scripts -->
<div>
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</div>

# Transmission-line equations (derivation: 2.1a → 2.3b) and Maxwell curl (phasor)

This document collects the incremental-circuit equations shown in a standard transmission-line derivation and shows the exact steps that take you from the **time-domain incremental KVL/KCL** (2.1a, 2.1b) → **time-domain telegrapher equations** (2.2a, 2.2b) → **phasor (sinusoidal steady-state) forms** (2.3a, 2.3b). It also includes the phasor form of Maxwell's curl equations.

---

## 1. Notation & small-Δ segment (figure reference)
Consider a short section of transmission line of length \(\Delta z\). The incremental lumped parameters for that section are:
- Series resistance \(R\,\Delta z\),
- Series inductance \(L\,\Delta z\),
- Shunt conductance \(G\,\Delta z\),
- Shunt capacitance \(C\,\Delta z\).

Voltages and currents at the left and right ends are:
- \(v(z,t)\) at position \(z\),
- \(v(z+\Delta z, t)\) at position \(z+\Delta z\),
- \(i(z,t)\) at position \(z\),
- \(i(z+\Delta z, t)\) at position \(z+\Delta z\).

---

## 2. Incremental KVL and KCL (2.1a, 2.1b)

v(z,t) − RΔz·i(z,t) − LΔz·∂i(z,t)/∂t − v(z+Δz,t) = 0
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>Transmission-Line Equations & Maxwell Curl (Phasor)</title>

<!-- KaTeX CSS -->
<link rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css" />

<!-- KaTeX Auto-render -->
<script defer
  src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer
  src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.body);"></script>

<style>
  body {
    font-family: Arial, sans-serif;
    max-width: 860px;
    margin: auto;
    padding: 40px;
    line-height: 1.6;
  }
  h1, h2, h3 {
    margin-top: 2rem;
  }
  code {
    padding: 2px 4px;
    background: #eee;
  }
</style>
</head>

<body>

<h1>Transmission-Line Equations (2.1a → 2.3b) and Maxwell Curl (Phasor)</h1>
<p>
This document derives the transmission-line equations from incremental KVL/KCL
to the time-domain telegrapher equations and then to their phasor forms.  
It also includes the phasor Maxwell curl equations.
</p>

<hr>

<h2>1. Small-Δ Segment and Notation</h2>

<p>For a short segment of length \( \Delta z \):</p>

<ul>
<li>Series resistance: \( R\Delta z \)</li>
<li>Series inductance: \( L\Delta z \)</li>
<li>Shunt conductance: \( G\Delta z \)</li>
<li>Shunt capacitance: \( C\Delta z \)</li>
</ul>

<p>Voltages and currents:</p>
<ul>
<li>\( v(z,t),\; v(z+\Delta z, t) \)</li>
<li>\( i(z,t),\; i(z+\Delta z, t) \)</li>
</ul>

<hr>

<h2>2. Incremental KVL and KCL (2.1a, 2.1b)</h2>

<h3>KVL</h3>
<p>
\[
v(z,t) - R\Delta z\, i(z,t) - L\Delta z\, \frac{\partial i(z,t)}{\partial t}
- v(z+\Delta z,t) = 0
\tag{2.1a}
\]
</p>

<h3>KCL</h3>
<p>
\[
i(z,t) - G\Delta z\, v(z+\Delta z,t)
- C\Delta z\, \frac{\partial v(z+\Delta z,t)}{\partial t}
- i(z+\Delta z,t) = 0
\tag{2.1b}
\]
</p>

<hr>

<h2>3. Limit → Time-Domain Telegrapher Equations (2.2a, 2.2b)</h2>

<p>
\[
\frac{\partial v}{\partial z} =
- R\, i(z,t) - L\, \frac{\partial i}{\partial t}
\tag{2.2a}
\]
</p>

<p>
\[
\frac{\partial i}{\partial z} =
- G\, v(z,t) - C\, \frac{\partial v}{\partial t}
\tag{2.2b}
\]
</p>

<hr>

<h2>4. Sinusoidal Steady State (Phasors)</h2>

<p>
Assume:
\[
v(z,t) = V(z)e^{j\omega t},\qquad
i(z,t) = I(z)e^{j\omega t}
\]
</p>

<p>Time derivative becomes:</p>

<p>
\[
\frac{\partial}{\partial t} \rightarrow j\omega
\]
</p>

<hr>

<h2>5. Substitute into (2.2a) → (2.3a)</h2>

<p>
\[
\frac{dV}{dz} = -(R + j\omega L)I(z)
\tag{2.3a}
\]
</p>

<hr>

<h2>6. Substitute into (2.2b) → (2.3b)</h2>

<p>
\[
\frac{dI}{dz} = -(G + j\omega C)V(z)
\tag{2.3b}
\]
</p>

<hr>

<h2>7. Wave Equations and Parameters</h2>

<h3>Propagation constant:</h3>
<p>
\[
\gamma = \sqrt{(R + j\omega L)(G + j\omega C)}
\]
</p>

<h3>Voltage wave:</h3>
<p>
\[
\frac{d^2 V}{dz^2} = \gamma^2 V(z)
\]
</p>

<h3>Current wave:</h3>
<p>
\[
\frac{d^2 I}{dz^2} = \gamma^2 I(z)
\]
</p>

<h3>Characteristic impedance:</h3>
<p>
\[
Z_0 = \sqrt{\frac{R + j\omega L}{G + j\omega C}}
\]
</p>

<h3>General solutions:</h3>
<p>
\[
V(z) = V^+ e^{-\gamma z} + V^- e^{+\gamma z}
\]
</p>

<p>
\[
I(z) = \frac{1}{Z_0}
\left(
V^+ e^{-\gamma z} - V^- e^{+\gamma z}
\right)
\]
</p>

<hr>

<h2>8. Maxwell Curl Equations (Phasor Form)</h2>

<h3>Faraday's Law</h3>
<p>
\[
\nabla \times \mathbf{E} = -j\omega\mu\,\mathbf{H}
\]
</p>

<h3>Ampère–Maxwell Law</h3>
<p>
\[
\nabla \times \mathbf{H} = j\omega\varepsilon\,\mathbf{E} + \mathbf{J}
\]
</p>

<h3>Source-free case</h3>
<p>
\[
\nabla \times \mathbf{E} = -j\omega\mu\,\mathbf{H}
\]
\[
\nabla \times \mathbf{H} = j\omega\varepsilon\,\mathbf{E}
\]
</p>

<hr>

</body>
</html>
