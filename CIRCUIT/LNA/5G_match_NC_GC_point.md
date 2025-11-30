<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Low-Noise PA Matching Analysis</title>
  <style>
    :root{--max-width:980px;--accent:#0b63ce;--muted:#6b7280}
    body{font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;line-height:1.5;color:#111827;background:#f8fafc;padding:24px}
    .container{max-width:var(--max-width);margin:0 auto;background:#fff;border-radius:12px;box-shadow:0 6px 24px rgba(15,23,42,0.06);padding:28px}
    h1{font-size:1.6rem;margin:0 0 8px}
    .meta{color:var(--muted);margin-bottom:18px}
    section{margin:20px 0}
    .figure{display:block;margin:12px 0;border-radius:6px;overflow:hidden}
    img{max-width:100%;height:auto;display:block}
    .lead{color:#0f172a}
    table{width:100%;border-collapse:collapse;margin-top:14px}
    th,td{padding:10px 12px;text-align:left;border-bottom:1px solid #eef2f7}
    th{background:#f1f5f9;color:#0f172a}
    .note{background:#f1f5f9;padding:12px;border-radius:8px;color:#0f172a}
    .kbd{background:#111827;color:#fff;padding:6px 8px;border-radius:6px;font-size:0.85rem}
    .btn{display:inline-block;background:var(--accent);color:#fff;padding:8px 12px;border-radius:8px;text-decoration:none}
    .cols{display:grid;grid-template-columns:1fr 1fr;gap:18px}
    @media (max-width:720px){.cols{grid-template-columns:1fr}}
    .summary-table td{vertical-align:top}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Low-Noise PA Matching Analysis</h1>
      <p class="meta">Design notes, simulations, and conclusions for input/output matching to optimize noise figure (NF) and gain.</p>
    </header>

    <section>
      <h2>1. Initial Circuit &amp; Baseline Simulation</h2>
      <p class="lead">Schematic and baseline measurement used as the starting point for matching work and circle analysis.</p>
      <figure class="figure">
        <img src="https://github.com/user-attachments/assets/4279dede-d2d8-413d-9ab7-2fa9d3f838a7" alt="Initial circuit schematic"/>
        <figcaption class="meta">Figure: Initial PA schematic.</figcaption>
      </figure>
      <figure class="figure">
        <img src="https://github.com/user-attachments/assets/80ad5aab-5277-40cf-a029-49a94e95b675" alt="Baseline simulation"/>
        <figcaption class="meta">Figure: Baseline simulation plot.</figcaption>
      </figure>
    </section>

    <section>
      <h2>2. Can we reduce the Noise Figure toward <span class="kbd">NF<sub>min</sub></span>?</h2>
      <p class="lead"><strong>Short answer:</strong> Yes — by using noise circles (NC) and matching the input to an appropriate Zd point you can approach NF<sub>min</sub>.</p>

      <div class="cols">
        <div>
          <figure class="figure">
            <img src="https://github.com/user-attachments/assets/e7cf49b2-6048-4e67-bf4d-c265a55cc5da" alt="Noise circle NC=2.2"/>
            <figcaption class="meta">Noise circle (example): NC = 2.2</figcaption>
          </figure>
        </div>
        <div>
          <figure class="figure">
            <img src="https://github.com/user-attachments/assets/39e44abd-e6fc-4e35-a9ca-137ec835fe3f" alt="Zd matching for NC 2.2"/>
            <figcaption class="meta">Target Zd and matching network for NC = 2.2</figcaption>
          </figure>
        </div>
      </div>

      <figure class="figure">
        <img src="https://github.com/user-attachments/assets/49aff484-fecb-4e98-b28f-e36bb4eb7106" alt="Simulation after input matching"/>
        <figcaption class="meta">Simulation result after applying input matching.</figcaption>
      </figure>

      <div class="note">
        <strong>Observation:</strong> Input matching reduces NF but does not guarantee reaching NF<sub>min</sub> unless the selected impedance is the optimal simultaneous noise–gain point.
      </div>
    </section>

    <section>
      <h2>3. Can we achieve maximum gain?</h2>
      <p class="lead">Yes — gain circles reveal impedance regions that maximize available gain. However, to reach the numeric target you must match both input and output.</p>

      <figure class="figure">
        <img src="https://github.com/user-attachments/assets/53115fac-9a2d-4c1a-8048-ae2021caafb3" alt="Gain circle plot"/>
        <figcaption class="meta">Gain circle analysis.</figcaption>
      </figure>

      <figure class="figure">
        <img src="https://github.com/user-attachments/assets/9d9a2567-8457-4d4f-b5f0-199d22e1ad06" alt="Post-matching gain result"/>
        <figcaption class="meta">Gain after input-only matching.</figcaption>
      </figure>

      <div class="note">
        <strong>Why the gain is not 15.2 dB?</strong>
        <p>Only the input was matched. Maximum realized gain requires conjugate matching at both input and output to the correspondingΓ<sub>opt</sub> points.</p>
      </div>
    </section>

    <section>
      <h2>4. Output Matching &amp; Simultaneous Optimization</h2>
      <p class="lead">To get both exact gain and exact NF, identify the intersection between noise and gain circles and match both ports to that point (input) and its conjugate (output).</p>

      <div class="cols">
        <div>
          <figure class="figure">
            <img src="https://github.com/user-attachments/assets/962afa1b-7183-4ed9-a9e9-981470378a30" alt="Intersection of noise and gain circles"/>
            <figcaption class="meta">Intersection of noise and gain circles — candidate Zd.</figcaption>
          </figure>
        </div>
        <div>
          <figure class="figure">
            <img src="https://github.com/user-attachments/assets/ebfed988-84ff-46f7-bb6c-1029d73d57ae" alt="Output matching network"/>
            <figcaption class="meta">Example output matching network used to conjugately match the output.</figcaption>
          </figure>
        </div>
      </div>

      <figure class="figure">
        <img src="https://github.com/user-attachments/assets/bf2e7d92-abbb-4db4-832e-533a910728b4" alt="Input-only matching simulation"/>
        <figcaption class="meta">Simulation result when only input matching is applied (for comparison).</figcaption>
      </figure>

      <div class="note">
        <strong>Conclusion:</strong> With matching at the intersection point (input) and conjugate output matching, you can achieve both the target NF and the target gain (≈15.2 dB) simultaneously.
      </div>
    </section>

    <section>
      <h2>5. Summary</h2>

      <table class="summary-table">
        <thead>
          <tr><th>Goal</th><th>Achievable?</th><th>Condition</th></tr>
        </thead>
        <tbody>
          <tr><td>Minimize NF (→ NF<sub>min</sub>)</td><td>✔️ Yes</td><td>Match input to noise-circle Γ<sub>opt</sub></td></tr>
          <tr><td>Achieve maximum gain</td><td>✔️ Yes</td><td>Conjugate input + output matching</td></tr>
          <tr><td>Exact NF and exact gain</td><td>✔️ Yes</td><td>Match at noise/gain circle intersection + output conjugate match</td></tr>
        </tbody>
      </table>
    </section>

    <section>
      <h2>6. Next steps</h2>
      <ul>
        <li>Apply the output matching network and re-run the full two-port simulations (S-parameters, NF, and gain plots).</li>
        <li>Add tolerance analysis for component Q and parasitics.</li>
        <li>Create a consolidated before/after comparison figure and a short method section with component values.</li>
      </ul>

      <p>If you want I can:</p>
      <ol>
        <li>Export this as a single HTML file ready to commit to GitHub.</li>
        <li>Generate a printable PDF version.</li>
        <li>Polish styling (dark mode, brand colors) or add interactive overlay annotations for the figures.</li>
      </ol>

      <p style="margin-top:12px">Tell me which of the three actions above you want and I’ll prepare it.</p>
    </section>

    <footer style="margin-top:18px;color:var(--muted);font-size:0.9rem">Created for PA matching documentation — concise, testable, and implementation-ready.</footer>
  </div>
</body>
</html>
