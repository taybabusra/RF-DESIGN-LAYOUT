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
<img width="845" height="377" alt="image" src="https://github.com/user-attachments/assets/4d9a19d5-0d39-4f37-8cf9-76627067e1b8" />
Ciccuit of after input matching
<img width="843" height="382" alt="image" src="https://github.com/user-attachments/assets/86e015ba-d8c7-4e62-836f-ad4c54b844cc" />
Result after input matching
