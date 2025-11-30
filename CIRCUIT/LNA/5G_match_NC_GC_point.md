<div class="container">
  <header>
    <h1>Low-Noise PA Matching Analysis</h1>
    <p class="meta">Design notes, simulations, and conclusions for input/output matching to optimize noise figure (NF) and gain.</p>
  </header>

  <section>
    <h2>1. Initial Circuit &amp; Baseline Simulation</h2>
    <img width="669" height="327" alt="image" src="https://github.com/user-attachments/assets/4279dede-d2d8-413d-9ab7-2fa9d3f838a7" /
    <p class="lead">Schematic and baseline measurement used as the starting point for matching work and circle analysis.</p>
   <img width="442" alt="img" src="https://github.com/user-attachments/assets/80ad5aab-5277-40cf-a029-49a94e95b675" /
  </section>

  <section>
    <h2>2. Noise Figure Optimization</h2>
    <p class="lead">Noise circles (NC) allow tuning the input impedance to approach NFmin.</p>

    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/e7cf49b2-6048-4e67-bf4d-c265a55cc5da" />
    </figure>
    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/39e44abd-e6fc-4e35-a9ca-137ec835fe3f" />
    </figure>

    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/49aff484-fecb-4e98-b28f-e36bb4eb7106" />
    </figure>
  </section>

  <section>
    <h2>3. Gain Optimization</h2>
    <p class="lead">Gain circles reveal the impedance for maximum available gain. Full gain requires both input and output matching.</p>

    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/53115fac-9a2d-4c1a-8048-ae2021caafb3" />
    </figure>
    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/9d9a2567-8457-4d4f-b5f0-199d22e1ad06" />
    </figure>
  </section>

  <section>
    <h2>4. Simultaneous Gain + Noise Optimization</h2>
    <p class="lead">Matching at the intersection of noise and gain circles yields both exact gain and exact NF.</p>

    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/962afa1b-7183-4ed9-a9e9-981470378a30" />
    </figure>
    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/ebfed988-84ff-46f7-bb6c-1029d73d57ae" />
    </figure>

    <figure class="figure">
      <img src="https://github.com/user-attachments/assets/bf2e7d92-abbb-4db4-832e-533a910728b4" />
    </figure>
  </section>

  <section>
    <h2>5. Summary</h2>
    <table>
      <tr><th>Goal</th><th>Achievable?</th><th>Condition</th></tr>
      <tr><td>Minimize NF</td><td>Yes</td><td>Input matched to NC Γopt</td></tr>
      <tr><td>Maximize Gain</td><td>Yes</td><td>Input + Output matching</td></tr>
      <tr><td>Exact NF & Gain</td><td>Yes</td><td>Match intersection + output conjugate</td></tr>
    </table>
  </section>
</div>
