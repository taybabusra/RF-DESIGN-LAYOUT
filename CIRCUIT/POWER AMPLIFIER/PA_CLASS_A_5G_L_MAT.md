Power amplifier Design specification:
1.Current less not more than 10mA



Circuit before matching:
<img width="537" height="262" alt="image" src="https://github.com/user-attachments/assets/27297d19-31c7-4e5c-ab74-140598e4c589" />

## Simulation result before matching
<img width="1930" height="856" alt="image" src="https://github.com/user-attachments/assets/1f58641a-2d94-4c44-8de2-d7db7bf1ef1f" />
## before matching the circuit is unconditionally stable due to it's different parameters

## AFTER doing the complex conjugate matching  
<img width="943" height="332" alt="image" src="https://github.com/user-attachments/assets/2a9811c5-500f-4fb7-a54c-f790c12d930f" />
This is the calculation for the complex conjugate matching.
## Matching network:
-- to do the perfect matching in the smith chart we decide to go with the T network:
### Input matching network
<img width="949" height="479" alt="image" src="https://github.com/user-attachments/assets/dba9d82c-3a9d-4ff9-9105-521d2d91e639" />
## Output matching network
<img width="959" height="436" alt="image" src="https://github.com/user-attachments/assets/6da56475-eb55-43af-bd1b-d4004ce0e3a7" />
## Both network is designed in consideration of having the Q=5 in consideration.


## Final circuit of the PA for a 5GHz network
<img width="783" height="377" alt="image" src="https://github.com/user-attachments/assets/57db9f80-2b69-4aca-bfa2-ecaa228a2a41" />

## Final simulation after design as a small signal analysis
<img width="926" height="417" alt="image" src="https://github.com/user-attachments/assets/a7a9771e-412b-42f8-be7b-a73e58abc694" />
