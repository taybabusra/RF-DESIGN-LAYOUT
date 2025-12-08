<h1>Why Noise Figure (NF) Improves at First but Gets Worse Again When Increasing Transistor Width (W)</h1>

<p>
This section explains the behavior from first-principles device physics and RF trade-off logic.  
The phenomenon is real and fundamental to MOS/BJT RF design — not a simulator artifact.
</p>

<details>
  <summary><h3>1. Core Effects When You Increase Transistor Width</h3></summary>

  <p>Increasing width <strong>(W)</strong> simultaneously changes three primary device parameters:</p>

  <ul>
    <li><strong>Transconductance (gm)</strong> ↑ — more carriers → stronger gm</li>
    <li><strong>Gate/base capacitances (Cgs, Cgd, Cbe, Cbc)</strong> ↑ — larger area → higher C</li>
    <li><strong>Transit frequency</strong> (f<sub>T</sub> = gm / 2πC<sub>total</sub>) ↓ — capacitances eventually dominate</li>
  </ul>

  <p>This sets up the trade-off behind the NF U-shaped curve.</p>
</details>

<details>
  <summary><h3>2. Phase 1 — NF Improves When Width Increases</h3></summary>

  <h4>Why NF Goes Down Initially</h4>

  <ol>
    <li><strong>gm increases almost linearly</strong><br>
        More width → more parallel channels → higher gm.<br>
        Since noise figure behaves approximately as:<br>
        <code>NFmin ∝ (γ/α) × (ω / fT)</code><br>
        And early on, gm grows faster than C, so f<sub>T</sub> does not degrade.
    </li>

    <li><strong>Input-referred thermal noise decreases</strong><br>
        Noise ∝ 1/gm → higher gm directly reduces input noise.
    </li>
  </ol>

  <p><strong>Result:</strong> NF drops — the classic region where increasing width helps noise performance.</p>
</details>

<details>
  <summary><h3>3. Phase 2 — NF Gets Worse as Width/Current Keep Increasing</h3></summary>

  <h4>The Turning Point: gm Scaling Stops, Parasitics Dominate</h4>

  <p>
    When width becomes large enough, the device behavior shifts from 
    <strong>gm-dominated</strong> to <strong>RC-dominated</strong>.  
    This reverses the NF improvement.
  </p>

  <h4>Key Degradation Mechanisms</h4>

  <ol>
    <li>
      <strong>Capacitances (Cgs, Cgd, Cfringing) grow linearly or super-linearly</strong><br>
      Large W → very large input capacitance.<br>
      This leads to:
      <ul>
        <li>input impedance collapse</li>
        <li>lossy or impossible matching</li>
        <li>noise from matching network increasing</li>
      </ul>
    </li>

    <li>
      <strong>gm saturates due to physical limits</strong><br>
      Including:
      <ul>
        <li>velocity saturation</li>
        <li>vertical-field mobility degradation</li>
        <li>series resistance (R<sub>g</sub>, R<sub>d</sub>, R<sub>s</sub>) increases</li>
      </ul>
      At this point:<br>
      gm ≈ constant but C<sub>total</sub> keeps rising.
    </li>

    <li>
      <strong>Transit frequency collapses</strong><br>
      <code>fT = gm / (2π Ctotal)</code><br>
      gm flattens + C keeps increasing → f<sub>T</sub> drops hard.<br>
      Since NFmin ∝ (ω / f<sub>T</sub>) → <strong>NF rises again</strong>.
    </li>

    <li>
      <strong>Gate resistance (Rg) becomes a major noise source</strong><br>
      Larger W → longer, wider gate → huge Rg.<br>
      Rg thermal noise is directly added to input noise at high frequency.
    </li>

    <li>
      <strong>Noise matching breaks</strong><br>
      When Cgs becomes too large, you can’t match to 50Ω (or source impedance) efficiently.<br>
      Matching degradation hurts NF even if the device is unchanged.
    </li>
  </ol>

  <h4>Core Insight</h4>
  <p>
    Increasing width helps noise <strong>only while gm dominates</strong>.  
    Once parasitics dominate, the device turns into a <strong>slow, noisy capacitor</strong>.
  </p>

  <p><strong>The NF vs Width curve is inherently U-shaped:</strong></p>

  <ul>
    <li>Small W → low gm → high NF</li>
    <li>Moderate W → optimal gm vs parasitics → best NF</li>
    <li>Large W → parasitic C, Rg, ft collapse → NF increases again</li>
  </ul>

  <p>Applies to CMOS, SiGe HBT, GaAs — the physics is universal.</p>
</details>

<details>
  <summary><h3>4. Practical Fixes and Optimization Strategies</h3></summary>

  <h4>1. Use Multi-Finger Layout</h4>
  <ul>
    <li>reduces gate resistance</li>
    <li>reduces effective capacitance per finger</li>
    <li>keeps gm high without collapsing f<sub>T</sub></li>
  </ul>

  <h4>2. Increase Current Density Instead of Width</h4>
  <p>
    Raising I<sub>D</sub>/W (moderately) increases gm without exploding capacitance.
  </p>

  <h4>3. Add Inductive Source Degeneration</h4>
  <ul>
    <li>improves noise matching</li>
    <li>stabilizes NF across width changes</li>
    <li>reduces sensitivity to large capacitances</li>
  </ul>

  <h4>4. Use a Cascode Topology</h4>
  <p>
    Cascode suppresses C<sub>gd</sub> feedback → higher effective f<sub>T</sub> → better noise at large W.
  </p>
</details>
