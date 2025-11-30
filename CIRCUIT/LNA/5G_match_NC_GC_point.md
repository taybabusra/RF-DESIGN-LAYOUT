<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>PA — Noise & Gain Matching (README)</title>
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--muted:#94a3b8;--accent:#60a5fa;--ok:#34d399}
    body{font-family:Inter,Segoe UI,Arial,Helvetica,sans-serif;margin:0;background:linear-gradient(180deg,#071029 0%, #071521 100%);color:#e6eef8}
    .wrap{max-width:980px;margin:36px auto;padding:28px}
    header{display:flex;align-items:center;gap:18px}
    h1{margin:0;font-size:22px}
    .meta{color:var(--muted);font-size:13px}
    .card{background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);padding:18px;border-radius:12px;margin-top:18px}
    .row{display:flex;gap:12px;flex-wrap:wrap}
    figure{margin:8px 0}
    figcaption{color:var(--muted);font-size:13px;margin-top:6px}
    pre{background:#021021;padding:12px;border-radius:8px;overflow:auto;border:1px solid rgba(255,255,255,0.02)}
    .kpi{display:inline-block;padding:8px 10px;border-radius:8px;background:rgba(255,255,255,0.02);margin-right:8px}
    .callout{border-left:4px solid var(--accent);padding:8px 12px;background:rgba(96,165,250,0.03);border-radius:8px;margin:12px 0}
    table{width:100%;border-collapse:collapse;margin-top:8px}
    th,td{padding:8px 10px;border-bottom:1px dashed rgba(255,255,255,0.03);text-align:left}
    .actions{display:flex;gap:8px;margin-top:14px}
    .btn{padding:8px 12px;border-radius:8px;text-decoration:none;color:inherit;border:1px solid rgba(255,255,255,0.03);background:rgba(255,255,255,0.01)}
    footer{color:var(--muted);font-size:13px;margin-top:18px}
    @media (max-width:720px){.row{flex-direction:column}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div>
        <h1>PA — Noise & Gain Matching: How noise & gain circles map to practical matching</h1>
        <div class="meta">Concise explanation and annotated figures — input files provided by author</div>
      </div>
    </header>

    <section class="card">
      <h2>Overview</h2>
      <p class="meta">Objective: show how noise (NF) and gain circles are used to pick an input match that trades off noise figure and gain, and how close a practical matching network can get to NF<sub>min</sub> and target gain.</p>

      <div class="callout">
        Key takeaways:
        <ul>
          <li><strong>Yes</strong> — by choosing Z<sub>d</sub> at the noise circle intersection you can approach NF<sub>min</sub> (Q1).</li>
          <li><strong>Yes</strong> — maximum small-signal gain is found on the gain circle; input-only matching limits achieved gain unless output is also matched (Q2).</li>
          <li><strong>Yes</strong> — exact gain and NF are achievable if both input and output are matched to the calculated intersection impedances (Q3).</li>
        </ul>
      </div>

      <h3>Files / Figures (as provided)</h3>
      <div class="row">
        <figure style="flex:1 1 300px">
          <img src="https://github.com/user-attachments/assets/4279dede-d2d8-413d-9ab7-2fa9d3f838a7" alt="PA circuit" style="width:100%;border-radius:8px">
          <figcaption>Figure 1 — PA circuit schematic (initial).</figcaption>
        </figure>

        <figure style="flex:1 1 300px">
          <img src="https://github.com/user-attachments/assets/80ad5aab-5277-40cf-a029-49a94e95b675" alt="initial simulation" style="width:100%;border-radius:8px">
          <figcaption>Figure 2 — Initial simulation results (before matching).</figcaption>
        </figure>
      </div>
    </section>

    <section class="card">
      <h2>Question 1 — Can we minimise noise to reach NF<sub>min</sub>?</h2>
      <p>Answer: <strong>Yes</strong>. From the noise circle (NC) you can identify an optimal load impedance Z<sub>d</sub> that places the amplifier operating point on or very near the NF<sub>min</sub> locus. In your case you report Z<sub>d</sub> ≈ <strong>2.2 (normalized)</strong> gave the expected improvement — see matching figures below.</p>

      <div class="row">
        <figure style="flex:1 1 420px">
          <img src="https://github.com/user-attachments/assets/e7cf49b2-6048-4e67-bf4d-c265a55cc5da" alt="noise circle explanation" style="width:100%;border-radius:8px">
          <figcaption>Noise circle with the selected Z<sub>d</sub> indicated.</figcaption>
        </figure>

        <figure style="flex:1 1 420px">
          <img src="https://github.com/user-attachments/assets/39e44abd-e6fc-4e35-a9ca-137ec835fe3f" alt="matching zd 2.2" style="width:100%;border-radius:8px">
          <figcaption>Matched input network using Z<sub>d</sub>=2.2 (normalized).</figcaption>
        </figure>
      </div>

      <h4>After matching (sim)</h4>
      <figure>
        <img src="https://github.com/user-attachments/assets/49aff484-fecb-4e98-b28f-e36bb4eb7106" alt="after sim" style="width:420px;border-radius:8px">
        <figcaption>Measured NF improvement after input matching.</figcaption>
      </figure>

      <pre>// Practical note
// 1) Loss and Q of real matching components increase NF. Use low-loss lines/inductors and high-Q caps.
// 2) If NF still above NFmin, inspect stability network and bias (which can change S-parameters and noise parameters).
</pre>
    </section>

    <section class="card">
      <h2>Question 2 — Can we get maximum gain from the circuit?</h2>
      <p>Answer: <strong>Yes — on paper.</strong> The gain circle shows where maximum available gain exists. However, matching only the input (S<sub>11</sub>) restricts the realized ›small-signal‹ gain because the load presented to the device (S<sub>22</sub> side) is not optimized.</p>

      <figure>
        <img src="https://github.com/user-attachments/assets/53115fac-9a2d-4c1a-8048-ae2021caafb3" alt="gain circle" style="width:100%;border-radius:8px">
        <figcaption>Gain circle: the point on the circle gives maximum theoretical gain.</figcaption>
      </figure>

      <p class="meta">You reported that after input matching, NC<sub>min</sub> didn't change significantly — expected if only input was matched. The simulated gain did not reach the theoretical 15.2 dB because the output was left unmatched.</p>

      <h4>Output matching</h4>
      <p>To approach the 15.2 dB target, perform a conjugate-style or power-optimal match at the output: this will present the device with the desired load impedance, moving the realized gain toward the theoretical maximum. Watch for stability and output network loss.</p>
    </section>

    <section class="card">
      <h2>Question 3 — Can we get exact gain with exact NC?</h2>
      <p>Answer: <strong>Yes.</strong> If you identify the intersection of the noise circle and gain circle and synthesize matching networks that present those complex impedances to the device (both input and output), you can realize the predicted NF and gain simultaneously.</p>

      <div class="row">
        <figure style="flex:1 1 420px">
          <img src="https://github.com/user-attachments/assets/962afa1b-7183-4ed9-a9e9-981470378a30" alt="intersection" style="width:100%;border-radius:8px">
          <figcaption>Intersection point(s) of noise & gain circles — candidates for Z<sub>d</sub>.</figcaption>
        </figure>

        <figure style="flex:1 1 420px">
          <img src="https://github.com/user-attachments/assets/ebfed988-84ff-46f7-bb6c-1029d73d57ae" alt="matching zd intersection" style="width:100%;border-radius:8px">
          <figcaption>Matching network targeting the intersection impedance.</figcaption>
        </figure>
      </div>

      <h4>Sim results (input-only matched)</h4>
      <figure>
        <img src="https://github.com/user-attachments/assets/bf2e7d92-abbb-4db4-832e-533a910728b4" alt="after input matching sim" style="width:420px;border-radius:8px">
        <figcaption>Simulation after input matching only — gain and NF improved, but full theoretical values require output matching as well.</figcaption>
      </figure>
    </section>

    <section class="card">
      <h2>Recommended next steps (practical, prioritized)</h2>
      <ol>
        <li><strong>Design and implement the output match</strong> to present the amplifier with the calculated load impedance for maximum gain (watch for oscillations — add damping resistors if necessary).</li>
        <li><strong>Use EM or distributed models</strong> for microstrip matching sections if operating at GHz — lumped approximations can hide stray reactances.</li>
        <li><strong>Measure S-parameters and noise parameters on the assembled PCB</strong> under bias (bench verification) — adjust matching to account for packaging and layout effects.</li>
      </ol>

      <h4>Short checklist before final claim</h4>
      <table>
        <tr><th>Item</th><th>Why</th></tr>
        <tr><td>Input & output matched</td><td>Realize predicted gain & NF simultaneously</td></tr>
        <tr><td>Low-loss components</td><td>Minimise dissipative NF contributions</td></tr>
        <tr><td>Stability check</td><td>Ensure matches don't create oscillation</td></tr>
        <tr><td>Bias optimization</td><td>S-params/noise params are bias-dependent</td></tr>
      </table>
    </section>

    <footer>
      <div class="meta">If you want, I can generate a printable README.md (markdown) or provide the minimal matching component values and schematic export. Tell me which format you prefer.</div>
    </footer>
  </div>
</body>
</html>
