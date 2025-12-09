
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

From KVL around the Δz loop:
\[
v(z,t) - R\Delta z\,i(z,t) - L\Delta z\;\frac{\partial i(z,t)}{\partial t} - v(z+\Delta z,t) = 0. \tag{2.1a}
\]

From KCL at the right node (current leaving the series branch equals currents through shunt branches):
\[
i(z,t) - G\Delta z\,v(z+\Delta z,t) - C\Delta z\;\frac{\partial v(z+\Delta z,t)}{\partial t} - i(z+\Delta z,t) = 0. \tag{2.1b}
\]

---

## 3. Divide by \(\Delta z\) and take the limit \(\Delta z \to 0\): time-domain telegrapher equations (2.2a, 2.2b)

Divide (2.1a) and (2.1b) by \(\Delta z\) and let \(\Delta z\to 0\). Defining partial derivatives in the limit yields the standard telegrapher PDEs:

\[
\boxed{\ \frac{\partial v(z,t)}{\partial z} = -R\,i(z,t)\;-\;L\;\frac{\partial i(z,t)}{\partial t}\ } \tag{2.2a}
\]

\[
\boxed{\ \frac{\partial i(z,t)}{\partial z} = -G\,v(z,t)\;-\;C\;\frac{\partial v(z,t)}{\partial t}\ } \tag{2.2b}
\]

These are the **time-domain** transmission-line equations (also called the telegrapher equations).

**Why this step is valid (concise):** dividing by \(\Delta z\) normalizes series/shunt parameters to per-unit-length values \(R,L,G,C\); the limit converts finite differences to spatial derivatives.

---

## 4. Move to sinusoidal steady state (phasors): assumptions & substitution

Assume all excitations are sinusoidal at angular frequency \(\omega\). Represent instantaneous fields as the real part of complex phasors:

\[
v(z,t) = \Re\{\,V(z)\,e^{j\omega t}\,\},\qquad
i(z,t) = \Re\{\,I(z)\,e^{j\omega t}\,\}.
\]

For algebraic manipulation we use the complex phasor forms directly:
\[
v(z,t) = V(z)\,e^{j\omega t},\qquad i(z,t) = I(z)\,e^{j\omega t}.
\]

Key operator substitution under this assumption:
\[
\frac{\partial}{\partial t} \longrightarrow j\omega \quad\text{(when acting on phasors)}.
\]

---

## 5. Substitute into (2.2a) → derive (2.3a)

Start from (2.2a):
\[
\frac{\partial v(z,t)}{\partial z} = -R\,i(z,t) - L\,\frac{\partial i(z,t)}{\partial t}.
\]

Compute derivatives with phasors:
\[
\frac{\partial v}{\partial z} = \frac{dV(z)}{dz}\,e^{j\omega t},\qquad
\frac{\partial i}{\partial t} = j\omega I(z)\,e^{j\omega t}.
\]

Substitute:
\[
\frac{dV(z)}{dz}\,e^{j\omega t} = -R\,I(z)\,e^{j\omega t} - L\,(j\omega I(z))\,e^{j\omega t}.
\]

Cancel the common factor \(e^{j\omega t}\) and obtain the phasor ODE:

\[
\boxed{\ \frac{dV(z)}{dz} = -\bigl(R + j\omega L\bigr)\,I(z)\ } \tag{2.3a}
\]

---

## 6. Substitute into (2.2b) → derive (2.3b)

Start from (2.2b):
\[
\frac{\partial i(z,t)}{\partial z} = -G\,v(z,t) - C\,\frac{\partial v(z,t)}{\partial t}.
\]

Compute derivatives with phasors:
\[
\frac{\partial i}{\partial z} = \frac{dI(z)}{dz}\,e^{j\omega t},\qquad
\frac{\partial v}{\partial t} = j\omega V(z)\,e^{j\omega t}.
\]

Substitute and cancel \(e^{j\omega t}\):

\[
\boxed{\ \frac{dI(z)}{dz} = -\bigl(G + j\omega C\bigr)\,V(z)\ } \tag{2.3b}
\]

**Interpretation:** time derivatives convert to multiplication by \(j\omega\); the per-unit-length series impedance is \(R+j\omega L\) and the per-unit-length shunt admittance is \(G+j\omega C\).

---

## 7. (Optional next steps — for completeness)
From (2.3a) and (2.3b) you can eliminate \(I\) (or \(V\)) to obtain second-order wave equations.

Eliminate \(I\) by differentiating (2.3a) with respect to \(z\) and substituting (2.3b):

\[
\frac{d^2 V}{dz^2} = (R+j\omega L)(G+j\omega C)\,V(z) = \gamma^2 V(z),
\]
where the **propagation constant** is
\[
\gamma \;=\; \sqrt{(R+j\omega L)(G+j\omega C)}.
\]

Similarly,
\[
\frac{d^2 I}{dz^2} = \gamma^2 I(z).
\]

Characteristic impedance:
\[
Z_0 = \sqrt{\frac{R+j\omega L}{G+j\omega C}}.
\]

General travelling-wave solutions:
\[
V(z) = V^+ e^{-\gamma z} + V^- e^{+\gamma z},\qquad
I(z) = \frac{1}{Z_0}\bigl(V^+ e^{-\gamma z} - V^- e^{+\gamma z}\bigr).
\]

---

## 8. Maxwell curl equations (phasor form) — included as requested

The phasor (time-harmonic) Maxwell curl equations in differential form are:

\[
\boxed{\ \nabla \times \mathbf{E} = -j\omega \mu\,\mathbf{H}\ } \qquad\text{(Faraday's law, phasor form)}
\]

\[
\boxed{\ \nabla \times \mathbf{H} = j\omega \varepsilon\,\mathbf{E} + \mathbf{J}\ } \qquad\text{(Ampère–Maxwell law, phasor form)}
\]

If we assume no impressed conduction current density (\(\mathbf{J}=0\)) and use \(\varepsilon\) instead of a generic phasor \(\mathbf{E}\) coefficient, the simplified source-free pair is commonly written as:

\[
\nabla \times \mathbf{E} = -j\omega\mu\,\mathbf{H},\qquad
\nabla \times \mathbf{H} = j\omega\varepsilon\,\mathbf{E}.
\]

> Note: you supplied the pair \(\nabla\times\mathbf{E}=-j\omega\mu\mathbf{H}\) and \(\nabla\times\mathbf{H}=j\omega\mathbf{E}\). The second equation normally includes the material permittivity \(\varepsilon\) (or total displacement \(\varepsilon\,\mathbf{E}\)); if you deliberately drop \(\varepsilon\) it implies a unit system or normalization where \(\varepsilon=1\). Be explicit which convention you want to use.

---

