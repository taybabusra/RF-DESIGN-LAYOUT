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
where 
F
r
e
s
t
{\displaystyle F_{\mathrm {rest} }} is the overall noise factor of the subsequent stages. According to the equation, the overall noise factor, 
F
r
e
c
e
i
v
e
r
{\displaystyle F_{\mathrm {receiver} }}, is dominated by the noise factor of the LNA, 
F
L
N
A
{\displaystyle F_{\mathrm {LNA} }}, if the gain is sufficiently high. The resultant Noise Figure expressed in dB is:
