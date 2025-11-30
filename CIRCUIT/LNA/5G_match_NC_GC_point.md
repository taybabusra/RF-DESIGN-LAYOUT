<div class="container">
  <header>
    <h1>Low-Noise PA Matching Analysis</h1>
    <p class="meta">Design notes, simulations, and conclusions for input/output matching to optimize noise figure (NF) and gain.</p>
  </header>

  <section>
    <h2>1. Initial Circuit & Baseline Simulation</h2>

    <figure>
      <img src="RAW_IMAGE_URL_1" alt="Schematic and baseline measurement" width="669" height="327" />
      <figcaption>Schematic and baseline measurement used as the starting point for matching work and circle analysis.</figcaption>
    </figure>

    <figure>
      <img src="RAW_IMAGE_URL_2" alt="Baseline circuit image" width="442" />
      <figcaption>Baseline circuit view.</figcaption>
    </figure>
  </section>

  <section>
    <h2>2. Noise Figure Optimization</h2>
    <p>Noise circles (NC) allow tuning the input impedance to approach NF<sub>min</sub>.</p>

    <figure>
      <img src="RAW_IMAGE_URL_3" alt="Noise Circle 1" />
      <figcaption>Noise circle visualization 1.</figcaption>
    </figure>

    <figure>
      <img src="RAW_IMAGE_URL_4" alt="Noise Circle 2" />
      <figcaption>Noise circle visualization 2.</figcaption>
    </figure>

    <figure>
      <img src="RAW_IMAGE_URL_5" alt="Noise Circle 3" />
      <figcaption>Noise circle visualization 3.</figcaption>
    </figure>
  </section>

  <section>
    <h2>3. Gain Optimization</h2>
    <p>Gain circles reveal the impedance for maximum available gain. Full gain requires both input and output matching.</p>

    <figure>
      <img src="RAW_IMAGE_URL_6" alt="Gain Circle 1" />
      <figcaption>Gain circle analysis 1.</figcaption>
    </figure>

    <figure>
      <img src="RAW_IMAGE_URL_7" alt="Gain Circle 2" />
      <figcaption>Gain circle analysis 2.</figcaption>
    </figure>
  </section>

  <section>
    <h2>4. Simultaneous Gain + Noise Optimization</h2>
    <p>Matching at the intersection of noise and gain circles yields both exact gain and exact NF.</p>

    <figure>
      <img src="RAW_IMAGE_URL_8" alt="Intersection 1" />
      <figcaption>Intersection of noise and gain circles 1.</figcaption>
    </figure>

    <figure>
      <img src="RAW_IMAGE_URL_9" alt="Intersection 2" />
      <figcaption>Intersection of noise and gain circles 2.</figcaption>
    </figure>

    <figure>
      <img src="RAW_IMAGE_URL_10" alt="Intersection 3" />
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
