Q: What is an oscillator? Why do we need the oscillator? What's the fundamental building block of an oscillator?<br>

Solution:<br>
An oscillator is an electronic circuit that generates a periodic signal (AC)—usually a sine wave, square wave, or clock—without requiring an external input signal.<br>
It basically converts the DC power into a periodic AC signal at a specific frequency.<br>
An oscillator is a circuit that produces a continuous, self-sustained oscillation at a specific frequency.<br>
<br>
Need for the oscillator:<br>
An oscillator is required to generate the carrier signal at the transceiver or receiver sector in a transceiver architecture.<br>
<br>
Fundamental block of an oscillator:<br>
The fundamental building block of an oscillator is the frequency-selective network, which are basically a tank network building with the LC network.<br>
The basic fundamental tank circuit is the series network or the parallel network. link (another GitHub)<br>
<br>
The fundamental rules to follow to design the oscillator are the Barkhausen criterion:<br>
**which defines that for the sustained oscillator, the loop gain of an oscillator needs to be 1**<br>
Total phase shift = 0 or 360<br>

## Tuned Oscillator Circuit<br> 
<img width="512" height="375" alt="image" src="https://github.com/user-attachments/assets/d80f3002-3ee2-41e2-9f16-8767428a37e4" />

### AC Analysis Simulation result:
<img width="467" height="317" alt="image" src="https://github.com/user-attachments/assets/4a57566d-7411-4772-be6f-99fed44e7f30" />

### Transient Analysis result of the 50ns time period:
<img width="469" height="304" alt="image" src="https://github.com/user-attachments/assets/336621f7-66d9-4b0a-8666-a6e38847f383" />

Summary of the design and the challenges:
Here, the tuned oscillator is based on the parallel LC network circuit, where the fundamental frequency of the circuit is defined by the value of the L and C network.
The equation of the fundamental frequency is defined by the values of the 
   f= 1/2piroot (LC)
Circuit working principle:
1. Due to the DC voltage, the MOSFET is in the saturation region, and it will amplify the voltage without any AC input. There is a voltage in the drain node due to the Vds = Vgs = Vth, and due to this voltage, the charge accumulates in the capacitor plant and there is an electric field between plate of the capacitor. Due to this, there is a energy stored by the electric field.
2. Due to the drain current flows through the inductor, a magnetic field is created around the coil, and energyis  stored due to the magnetic field.
3. The importance of the resistor in the circuit: Because the resisotor control how much energy is lost per cycle in the tank.
    Less loss - energy build up more- larger voltage swing -- higher gain.

   NMOS used as a current source, id = gm vgs
   tank converts the current into a voltage, vout = id Ztank.
   The phase of the inductor and the capacitor current  are in opposite phase.

4. The value of R is small, which means high loss because it allows more current to flow for the same voltage, and that current dissipates more energy as heat every cycle.
5.  The value of the Q = woRC 


## Cascade of two Tuned Oscillator Circuit<br> 
<img width="736" height="361" alt="image" src="https://github.com/user-attachments/assets/6c258856-12c8-44c4-afb5-771ab7252df2" /> <br>
### AC analysis simulation result:
<img width="461" height="297" alt="image" src="https://github.com/user-attachments/assets/918cdcc0-714f-4b27-a3a8-ff319fed94d6" /> <br>
At first, with the same value of the DC in the gate of the mosfet which was 340mV then there was a phase shift of around -30 so after that I changed the Dc voltage of the input to change the phase shift improvement of -24degree. <br>
Q: why this happening? As far as my understanding the both mosfet doesn't have the same Cgs or Cgd and coupling capacitor.<br>
<img width="464" height="299" alt="image" src="https://github.com/user-attachments/assets/e56dd9c1-37d9-439a-b4a7-822f4d495789" /><br> 
Figure: the result of the first stage.<br>
<img width="464" height="310" alt="image" src="https://github.com/user-attachments/assets/ce76e5fb-bfe0-4b1b-aeff-e9fb7ea97818" /> <br>
Figure: result of the 2nd stage.<br>

### Transient analysis simulation result:
<img width="467" height="310" alt="image" src="https://github.com/user-attachments/assets/4fde77ac-3353-4a7c-bdf7-c812487003c2" /> <br>
The intermediate note has a more than 180 phase shift, and last has also the 180 phase shift to get the output, which  has more than -24 phase shift.
## Cross-Coupled Tuned Oscillator Circuit
<img width="698" height="373" alt="image" src="https://github.com/user-attachments/assets/aec7a2de-92a9-42de-81a1-591b5ab2e7e7" />

## Transient Analysis Simulation result:
<img width="465" height="306" alt="image" src="https://github.com/user-attachments/assets/f4d5882d-3630-48aa-bb4d-0c2cb604c106" /> <br>

Particularly in this circuit, there are two things I need to consider: one is staring circuit how the circuit will be one and get's started. <br>
To start the circuit, we can do two things: one is add an initial condition from the simulation window.<br>
<img width="304" height="278" alt="image" src="https://github.com/user-attachments/assets/b18ea8f2-ab53-4871-85f3-babda4522097" />
<img width="236" height="185" alt="image" src="https://github.com/user-attachments/assets/e6c67550-e57d-48d0-b2a1-9de1820c8e48" /><br>
Click on the node or net where We want to add the values of the initial set and give the value. After that, it will start to work.<br>
<br>
Another way to work on the circuit starting point is to add the transient noise in the simulation.<br>
<img width="240" height="418" alt="image" src="https://github.com/user-attachments/assets/289b8809-3fdd-4e23-b56a-cd36a25748de" /> <br>
Here is the maximum noise frequency definition of the circuit.<br>

# Summary: 
It's showing the output, which should be shown in the circuit behaviour, but I need to analyze the HB and other simulations for this circuit from YT.
