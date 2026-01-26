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
