<div class="container">
  <header>
    <h1>Low-Noise PA Matching Analysis</h1>
    <p class="meta">Design notes, simulations, and conclusions for input/output matching to optimize noise figure (NF) and gain.</p>
  </header>

  <section>
    <h2>1. Initial Circuit & Baseline Simulation</h2>
    <figure>
      <img src="https://github.com/user-attachments/assets/4279dede-d2d8-413d-9ab7-2fa9d3f838a7" alt="Schematic and baseline measurement" width="669" height="327" />
      <figcaption>Schematic and baseline measurement used as the starting point for matching work and circle analysis.</figcaption>
    </figure>

    <figure>
      <img src="https://github.com/user-attachments/assets/80ad5aab-5277-40cf-a029-49a94e95b675" alt="Baseline circuit image" width="442" />
      <figcaption>Baseline circuit view.</figcaption>
    </figure>
  </section>

  <section>
    <h2>2. Noise Figure Optimization</h2>
    <p>Noise circles (NC) allow tuning the input impedance to approach NF<sub>min</sub>.</p>

    <figure>
      <img src="https://github.com/user-attachments/assets/e7cf49b2-6048-4e67-bf4d-c265a55cc5da" alt="Noise Circle 1" />
      <figcaption>Noise circle visualization 1.</figcaption>
    </figure>

    <figure>
      <img src="https://github.com/user-attachments/assets/39e44abd-e6fc-4e35-a9ca-137ec835fe3f" alt="Noise Circle 2" />
      <figcaption>Noise circle visualization 2.</figcaption>
    </figure>

    <figure>
      <img src="https://github.com/user-attachments/assets/49aff484-fecb-4e98-b28f-e36bb4eb7106" alt="Noise Circle 3" />
      <figcaption>Noise circle visualization 3.</figcaption>
    </figure>
  </section>

  <section>
    <h2>3. Gain Optimization</h2>
    <p>Gain circles reveal the impedance for maximum available gain. Full gain requires both input and output matching.</p>

    <figure>
      <img src="https://github.com/user-attachments/assets/53115fac-9a2d-4c1a-8048-ae2021caafb3" alt="Gain Circle 1" />
      <figcaption>Gain circle analysis 1.</figcaption>
    </figure>

    <figure>
      <img src="https://github.com/user-attachments/assets/9d9a2567-8457-4d4f-b5f0-199d22e1ad06" alt="Gain Circle 2" />
      <figcaption>Gain circle analysis 2.</figcaption>
    </figure>
  </section>

  <section>
    <h2>4. Simultaneous Gain + Noise Optimization</h2>
    <p>Matching at the intersection of noise and gain circles yields both exact gain and exact NF.</p>

    <figure>
      <img src="https://github.com/user-attachments/assets/962afa1b-7183-4ed9-a9e9-981470378a30" alt="Intersection 1" />
      <figcaption>Intersection of noise and gain circles 1.</figcaption>
    </figure>

    <figure>
      <img src="https://github.com/user-attachments/assets/ebfed988-84ff-46f7-bb6c-1029d73d57ae" alt="Intersection 2" />
      <figcaption>Intersection of noise and gain circles 2.</figcaption>
    </figure>

    <figure>
      <img src="https://github.com/user-attachments/assets/bf2e7d92-abbb-4db4-832e-533a910728b4" alt="Intersection 3" />
      <figcaption>Intersection of noise and gain circles 3.</figcaption>
    </figure>
  </section>

  <section>
    <h2>5. Summary</h2>
    <table>
      <thead>
        <tr>
          <th>Goal</th>
          <th>Achievable?</th>
          <th>Condition</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Minimize NF</td>
          <td>Yes</td>
          <td>Input matched to NC Γ<sub>opt</sub></td>
        </tr>
        <tr>
          <td>Maximize Gain</td>
          <td>Yes</td>
          <td>Input + Output matching</td>
        </tr>
        <tr>
          <td>Exact NF & Gain</td>
          <td>Yes</td>
          <td>Match intersection + output conjugate</td>
        </tr>
      </tbody>
    </table>
  </section>
</div>
