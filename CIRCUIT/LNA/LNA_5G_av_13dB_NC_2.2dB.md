To design a LNA  here is the specificatio
1.operating frequency :5Ghz
2.NF <2.2dB
3.Gain>13dB

## Circuit diagram closer to specification
<img width="685" height="319" alt="image" src="https://github.com/user-attachments/assets/08f00b77-46ff-4856-96e9-a6675d97cd67" />
<img width="845" height="385" alt="image" src="https://github.com/user-attachments/assets/26a59599-25ec-46ad-b49c-e1083d0e678b" />

The circuit is unconditonally stable and NFmin = 2.16 and NF = 2.62 and S21 = 8.59 and Gmax = 15
## Now we need to match so that the gain of the circuit is 13dB and NF = 2.2
<img width="622" height="358" alt="image" src="https://github.com/user-attachments/assets/f4602ad0-b38c-490a-90ed-c811232f2525" />
Figure is defining the intersection between noise circle and gain circle.
<img width="1280" height="582" alt="image" src="https://github.com/user-attachments/assets/793ea0d2-5ebc-4bef-ba43-0edf74d5e097" />

The intersecting point Zd = 108.556+47.603j
<img width="959" height="380" alt="image" src="https://github.com/user-attachments/assets/4828d3b8-1e83-4030-98e3-c35ad0125f11" />
Matching network calculation for input secton
<img width="680" height="309" alt="image" src="https://github.com/user-attachments/assets/a84e43bc-e9a6-4de0-8d89-6e557b2f9d5c" />
Ciccuit of after input matching
<img width="843" height="382" alt="image" src="https://github.com/user-attachments/assets/86e015ba-d8c7-4e62-836f-ad4c54b844cc" />
Result after input matching


# OUTPUT MATCHING
<img width="424" height="368" alt="image" src="https://github.com/user-attachments/assets/d6eb741d-11a2-4e5e-948b-85c1f6b46c3a" />
Z parameters calculation because of unilateral matching.
<img width="946" height="364" alt="image" src="https://github.com/user-attachments/assets/156df2b4-a314-40bc-8079-0cbfc95d213e" />
OUTPUT MATCHING NETWEOK CALCULATION.

# Complete circuit to meet the specification
<img width="691" height="335" alt="image" src="https://github.com/user-attachments/assets/5ff5f002-5f8b-43a6-a422-f606c465998d" />

## fINAL SIMULATION OF THE CIRCUIT
<img width="842" height="377" alt="image" src="https://github.com/user-attachments/assets/3302bee7-07df-474c-b331-f94f24686f31" />
<img width="840" height="374" alt="image" src="https://github.com/user-attachments/assets/b437209d-2c51-4f8e-9e40-7775e2df8f23" />

So the circuit is unconditionally stable but the gain is lower than specification

## KEY observation:
changing the L we can fixes the u in the circuit.

