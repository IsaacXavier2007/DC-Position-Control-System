# DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J)     moment of inertia of the rotor =    0.02 kg.m^2<br>
(b)     motor viscous friction constant =    0.002 N.m.s<br>
(Ktf)    motor torque constant   =           1.5 N.m/Amp<br>
(Ra)    armature resistance  =              2 Ohm<br>
(La)     armature inductance  =              0.5 H<br>
(Kb)      back emf constant = 0.5<br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 
<img width="1312" height="1600" alt="image" src="https://github.com/user-attachments/assets/0b811c8e-2ec2-4699-b9bc-7137ceeee7b5" />
<img width="1026" height="1467" alt="image" src="https://github.com/user-attachments/assets/cdc3e5a5-3065-45e5-b1f2-8894ff4f8117" />
<img width="979" height="1441" alt="image" src="https://github.com/user-attachments/assets/306028b0-4c72-4b4c-82d0-60404cead35f" />
<img width="1600" height="1066" alt="image" src="https://github.com/user-attachments/assets/14916ea4-427a-406a-a2ba-838af5a2112d" />






## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program
```
Kt = 1.5;
J = 0.02;
B = 0.002;
Ra = 2;
La = 0.5;
Kb = 0.5;
S = tf('s');
ol_sys = Kt / ((J*S*S+B*S)*(Ra+La*S)+Kt*Kb*S);
subplot(2,1,1)
step(ol_sys)
title('Open-Loop Step Response');
Cl_sys = feedback(1*ol_sys,1);
subplot(2,1,2)
step(Cl_sys)
title('Closed-Loop Step Response');
```


## Output:
<img width="668" height="521" alt="Screenshot 2026-07-30 223938" src="https://github.com/user-attachments/assets/df4cb782-4552-40f3-a7ea-d5b6f9b75df3" />

<img width="525" height="428" alt="Screenshot 2026-07-30 224326" src="https://github.com/user-attachments/assets/d459b45d-583a-4859-96d3-41b8a3325345" />



## Result
Thus, the position of dc motor is controlled using MATLAB. 
