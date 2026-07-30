# DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J)     moment of inertia of the rotor =    0.02 kg.m^2<br>
(b)     motor viscous friction constant =    0.002 N.m.s<br>
(Ktf)    motor torque constant   =           1.5 N.m/Amp<br>
(Ra)    armature resistance  =              2 Ohm<br>
(La)     armature inductance  =              0.5 H<br>
(Kb)      back emf constant = 0.5 <br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 
<img width="1312" height="1600" alt="image" src="https://github.com/user-attachments/assets/76f11749-c614-417e-9a7e-d0ff9a82276e" />
<img width="1026" height="1467" alt="image" src="https://github.com/user-attachments/assets/449b1cb2-3b6e-420e-bdea-4ba37a5914ff" />
<img width="979" height="1441" alt="image" src="https://github.com/user-attachments/assets/b9bdacca-e065-4176-9f12-8b467dbbfadd" />
<img width="1600" height="1066" alt="image" src="https://github.com/user-attachments/assets/dc6edbbe-bfbf-40b4-9d2c-3203a87f7005" />






## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program:
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
<img width="668" height="521" alt="Screenshot 2026-07-30 223938" src="https://github.com/user-attachments/assets/fa8c7d7b-b7ae-44b2-ac8e-041d0f1c675c" />
<img width="525" height="428" alt="Screenshot 2026-07-30 224326" src="https://github.com/user-attachments/assets/807dffb0-5d17-409a-8943-8b84c120e5a7" />



## Result
Thus, the position of dc motor is controlled using MATLAB. 
