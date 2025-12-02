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
matching circuit losses of oftne limit the ability of the amplifier to achieve a noise figure equivalesn to device NFmin.
Q: what is the Rn after matching it should be equal to source resistnace why it's lower than that. what's the relation between Rn and Z11.
