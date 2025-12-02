<img width="241" height="260" alt="image" src="https://github.com/user-attachments/assets/cd9b190e-a3f6-4a46-824d-62c84635313f" />

# Quick review -- LNA Theory & Fundamentals
Q: what is a low noise amplifier?
electronic amplifier that amplifiers a very low power signal without significaltly degrading 
its signal to noise ratio.amplifier increase te power of both the signal and noise presnet at its input but 
the amplifier will also introduce som additional noise. 
LNA is designed to minimize that addtional noise.

Imp: Designer can minimize additional noise by choosing low noise amponents, operating point and circuit topologies.
Q: Does higher node device is less prone to noise addition? and which component like BJT and mosfet which one has the higher noise adding 
does NMOS is higher noise additive of PMOS.
Q: In high frequency what's happend to the noise? do they are more additive? 

LNA is a key component at the front end of the radio receiver circuit to help reduce unwanted noise in particular. 
the overal NF is dominanted by the first frew stages of the RF front end.
Q: why the first few stages are very important? for each stages how the output NF is dominated?
--> the effect of noise from subsequent stages of the reciever chain in the circuit is reduced bu thje signal gain created by the LNA.
while the noise crated by the LNA  itself is injected directly into received signal.

through as the LNA it amplify the desired signal power hile adding as little noise and distortion as possible.The work doen by the LNA enables 
optimum retrieval of the desired signal in the later stages of the system.
Receiver block of the communication system.
<img width="188" height="88" alt="image" src="https://github.com/user-attachments/assets/337b6afe-b27b-4c7e-98f2-e358fb45b3d7" />
Q: what's the friis formula? from where it is calculated.
<img width="960" height="216" alt="image" src="https://github.com/user-attachments/assets/2fb351be-ddda-4c9c-a29f-aa08556841d6" />
<img width="481" height="43" alt="image" src="https://github.com/user-attachments/assets/02db23ba-090b-48d3-a359-536e43d5e97e" />
Friis's formula is used to clculated the total noise factor of a cascade of stages. each with its own noises facto and power gain 
where the impedances are matched at each stage. Total noise factor ca nthen be used to calculate the total noise figure.
<img width="198" height="41" alt="image" src="https://github.com/user-attachments/assets/863d36e4-d642-42d0-b79e-4bceae5dd34a" />
<img width="460" height="49" alt="image" src="https://github.com/user-attachments/assets/7e233b96-1270-47de-baff-76bd81f83b02" />
<img width="268" height="39" alt="image" src="https://github.com/user-attachments/assets/f6916117-f588-41e4-9f43-4918f75a547b" />
Q: when I am designing the LNA then it's S11 is not closer to -10dB. it's in the range of -5dB why is that so? does this has the impact on my system?
<img width="443" height="257" alt="image" src="https://github.com/user-attachments/assets/0a52ec4a-8b3a-47f5-9628-ba67ab66b382" />
Based on technoloy the props and cons are the device size, availibility etc.

When desining the circuit the rule of thum to remember that 
pick a device whose optimum NF = 1/2 of the desired NF from the LNA circuit
Q: what i gamma optimum values or magnitude? why it is important to design a circuit.
Q: why does the linearity and non-lineartity of the device is important when designing a circuit.


#LNA impedance matching consideration:
1.gamma opt is the reflection co-efficient of the source impedance presented to the device that allows the device to produce it's NFmin.
2.matching circuit losses of oftne limit the ability of the amplifier to achieve a noise figure equivalesn to device NFmin.
Q: what is the Rn after matching it should be equal to source resistnace why it's lower than that. what's the relation between Rn and Z11.
3.gamma opt not necessarity equal to S11* which means noise match is not equicalent to a gain match.
4.Noise resistance is used to calculate the device's sensitivity in noise figure to changes in source impedance.Rn is normalized to 50 ohm.
<img width="208" height="149" alt="image" src="https://github.com/user-attachments/assets/c7dc9ed6-cbb5-4e00-a531-3574d87d4272" />




<h1>LNA Theory & Fundamentals — Quick Review</h1>

<h2>🔍 What is a Low Noise Amplifier (LNA)?</h2>
<p>
A Low Noise Amplifier boosts very low-power signals while minimizing additional noise.  
Although amplification increases both signal and noise present at the input, the LNA's goal is
to add as little noise as possible through careful device choice, biasing, and topology selection.
</p>

<hr>

<h2>📌 Key Questions</h2>

<h3>1. Are higher-node devices less prone to noise?</h3>
<p>Noise performance depends on device physics rather than process node alone. Smaller geometries do not inherently guarantee lower noise.</p>

<h3>2. Which adds more noise — BJT vs MOSFET? NMOS vs PMOS?</h3>
<ul>
  <li>BJTs generally offer lower noise for RF due to higher transconductance.</li>
  <li>NMOS typically exhibits lower noise than PMOS (higher mobility → higher gm → reduced noise contribution).</li>
</ul>

<h3>3. What happens to noise at high frequency?</h3>
<p>Noise typically increases with frequency due to device parasitics and reduced gain.</p>

<hr>

<h2>🎯 Importance of LNA in Receiver Front-Ends</h2>
<p>
The LNA sits at the front of the RF chain. Because of its position, its noise dominates the total receiver noise figure.
Gain from the LNA suppresses the noise contribution of later stages, while the noise generated by the LNA itself directly appears in the signal path.
</p>

<hr>

<h2>📘 Friis Formula</h2>

<p><strong>Purpose:</strong> Calculates total noise factor of cascaded stages (with impedance matching).</p>

<div align="center">
  <img src="https://github.com/user-attachments/assets/2fb351be-ddda-4c9c-a29f-aa08556841d6" width="90%">
  <br><br>
  <img src="https://github.com/user-attachments/assets/02db23ba-090b-48d3-a359-536e43d5e97e">
</div>

<p>
Total noise factor becomes:
</p>

<div align="center">
  <img src="https://github.com/user-attachments/assets/863d36e4-d642-42d0-b79e-4bceae5dd34a">
  <br><br>
  <img src="https://github.com/user-attachments/assets/7e233b96-1270-47de-baff-76bd81f83b02">
  <br><br>
  <img src="https://github.com/user-attachments/assets/f6916117-f588-41e4-9f43-4918f75a547b">
</div>

<hr>

<h2>📡 Design Issue: Why is S11 only –5 dB instead of –10 dB?</h2>

<p>
Poor S11 indicates imperfect input matching. This affects system performance through:
</p>

<ul>
  <li>Reduced available gain</li>
  <li>Potential stability issues</li>
  <li>Higher reflection → lower effective SNR</li>
</ul>

<div align="center">
  <img src="https://github.com/user-attachments/assets/0a52ec4a-8b3a-47f5-9628-ba67ab66b382" width="50%">
</div>

<hr>

<h2>📐 Rule of Thumb for Device Selection</h2>
<p>
Choose a device with optimum NF roughly half of the desired LNA NF target.
</p>

<hr>

<h2>⚡ Gamma<sub>opt</sub> & Noise Matching Concepts</h2>

<ul>
  <li><strong>Gamma<sub>opt</sub>:</strong> Source reflection coefficient that achieves NF<sub>min</sub>.</li>
  <li>Matching circuit losses prevent achieving the true NF<sub>min</sub>.</li>
  <li>Gamma<sub>opt</sub> is generally <em>not</em> equal to S11*, meaning noise matching ≠ gain matching.</li>
</ul>

<h3>Noise Resistance (R<sub>n</sub>)</h3>
<ul>
  <li>Indicates how sensitive NF is to impedance mismatch.</li>
  <li>Normalized to 50 Ω.</li>
  <li>After matching, R<sub>n</sub> may appear lower than expected depending on Z<sub>11</sub> and device parameters.</li>
</ul>

<div align="center">
  <img src="https://github.com/user-attachments/assets/c7dc9ed6-cbb5-4e00-a531-3574d87d4272" width="25%">
</div>

<hr>

<h2>📉 Linearity Considerations</h2>
<p>
Linearity & nonlinearity play a critical role in preventing distortion and intermodulation products that degrade system performance.
</p>
