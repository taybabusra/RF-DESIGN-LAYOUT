<h1>RF: Why Noise Figure (NF) improves then worsens when increasing transistor Width (W)</h1>

<p>Short answer: <strong>W helps at first because gm rises faster than capacitances — but beyond an optimum, parasitics (C, R) and mobility/series-resistance effects outgrow gm, ft collapses, and NF increases.</strong></p>

<details>
  <summary><strong>Q: Why does NF decrease with width initially but then rise after more width/current?</strong></summary>

  <h4>First-principles snapshot</h4>
  <ul>
    <li><strong>gm</strong> (transconductance) ~ increases with W → reduces input-referred thermal noise (good).</li>
    <li><strong>C<sub>total</sub></strong> (C<sub>gs</sub>, C<sub>gd</sub>, fringing) ↑ with W → tends to reduce f<sub>T</sub> = gm / (2π C<sub>total</sub>).</li>
    <li><strong>Series resistances</strong> (R<sub>g</sub>, R<sub>s</sub>, R<sub>d</sub>) and mobility degradation limit gm scaling at large W or high current density.</li>
  </ul>

  <h4>Key relations (intuitive)</h4>
  <p>
    f<sub>T</sub> ≈ gm / (2π C<sub>total</sub>)<br>
    NF<sub>min</sub> ∝ (ω / f<sub>T</sub>) × (device noise factors) — so if f<sub>T</sub> falls, NF gets worse.
  </p>

  <h4>Why the U-shaped NF vs W</h4>
  <ol>
    <li><strong>Small W:</strong> low gm → high NF.</li>
    <li><strong>Moderate W:</strong> gm dominates → NF improves (minimum).</li>
    <li><strong>Large W / high current:</strong> parasitic C and R dominate, gm saturates, f<sub>T</sub> drops → NF rises again.</li>
  </ol>
</details>

<details>
  <summary><strong>Q: How to find the optimum and fix it — practical, prioritized actions</strong></summary>

  <h4>Immediate checklist (ranked)</h4>
  <ol>
    <li><strong>Multi-finger layout</strong> — split W across N fingers to reduce gate resistance and local C per finger while keeping total gm.</li>
    <li><strong>Increase current density before width</strong> — raise I<sub>D</sub>/W moderately to push gm without exploding C (watch thermal limits).</li>
    <li><strong>Use cascode stage</strong> — isolates C<sub>gd</sub> feedback and preserves gain/ft at high W.</li>
    <li><strong>Inductive source degeneration</strong> — improves noise match and reduces sensitivity to parasitics; also widens noise-optimal matching range.</li>
    <li><strong>Optimize device finger length</strong> — avoid overly long gates (higher Rg) even if width is large; keep unit finger width reasonable for process node.</li>
    <li><strong>Layout: minimize routing series R</strong> — short source/drain runs, wide metal for large devices, symmetrical fingers.</li>
  </ol>

  <h4>Design rules & heuristics</h4>
  <ul>
    <li>Target the NF minimum by sweeping W in simulation while logging gm, C<sub>gs</sub>, C<sub>gd</sub>, R<sub>g</sub>, and f<sub>T</sub>.</li>
    <li>If R<sub>g</sub> becomes significant, split gates and add low-resistance routing or multiple gate fingers.</li>
    <li>If C dominates, prefer raising bias (moderately) or change topology (cascode or shunt-feedback).</li>
  </ul>

  <h4>Tools to use</h4>
  <p>S-parameter driven noise analysis, Y-factor or cold-source measurements for bench validation, and EM-aware layout extraction (post-layout) for accurate parasitics.</p>
</details>

<details>
  <summary><strong>Q: Quick worked example (how to run a sweep)</strong></summary>

  <p>Use this simple table or automate it in your simulator. Sweep W and log: I<sub>D</sub>, gm, C<sub>gs</sub>, C<sub>gd</sub>, R<sub>g</sub>, f<sub>T</sub>, NF.</p>

  <pre>
| W (µm) | ID (mA) | gm (mS) | Cgs (fF) | Cgd (fF) | Rg (Ω) | fT (GHz) | NF (dB) |
|--------|---------|---------|----------|----------|--------|----------|---------|
| 10     | 0.5     | 5.0     | 45       | 10       | 2.5    | 18       | 1.8     |
| 20     | 1.0     | 9.5     | 85       | 20       | 3.5    | 17       | 1.2     |
| 40     | 2.0     | 16.0    | 160      | 38       | 6.0    | 13       | 1.9     |
  </pre>

  <p><em>Interpretation:</em> NF hits a minimum near the point where gm growth slows vs parasitic growth; the table above is illustrative — use your specific PDK numbers.</p>
</details>

<hr>

<h3>Concise engineer-to-engineer playbook (3 moves)</h3>
<ol>
  <li><strong>Measure & extract:</strong> do post-layout extraction and sweep W with constant total current and constant current density variants. Plot NF vs W and f<sub>T</sub> vs W.</li>
  <li><strong>Fix topology:</strong> if NF rises at large W, switch to cascode or add inductive degeneration and multi-finger the device.</li>
  <li><strong>Layout & routing:</strong> reduce R<sub>g</sub> and series R by fingering + wide metal and symmetric routing. Re-extract and re-sim.</li>
</ol>

<hr>

### SIMULATION
<img width="517" height="425" alt="image" src="https://github.com/user-attachments/assets/b49163ed-fab7-4636-87a3-f5c946bc15ad" />

<img width="541" height="440" alt="image" src="https://github.com/user-attachments/assets/48fba68b-4c53-4a86-bd81-a8afd1dcf50f" />


output noise with frequency
<img width="518" height="430" alt="image" src="https://github.com/user-attachments/assets/bcab92d1-6e67-40a7-9336-4e46d2629ff3" />

🎯 Optimum noise impedance (Zopt) shifts with Vbias
As bias increases:
gm increases → Zopt decreases
If your source impedance is fixed (e.g., 50 Ω),
mismatch between Zs and Zopt increases at some bias points
