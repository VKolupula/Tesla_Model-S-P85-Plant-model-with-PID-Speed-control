# Model and simulate an electric car (Tesla Model S) in MATLAB & SIMULINK with PID speed controller.

### vehicle parameters
![Screenshot (480)](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/8fe02d07-f236-48c0-be93-1d56b5f2ccba)

![car_dynamics](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/b465784f-447e-443a-9794-fe0d53eac7e7)

## Newton's laws of motion 
### Σ F = Ma.
#### Tractive Force(Ff) + Rolling Resistance(Fr) + Aerodynamic drag(D) = Mass * Acceleration

##### Tractive Force(Ff)

![tractive force](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/31c04632-a3f3-47b5-bdea-4ec13bf8a5f8)

where,
T = torque(Nm),
L = Radius of Wheel(m),
Gr = Gear ratio.

##### Aerodynamic Drag(D)

![areodynamic drag](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/ba92b89e-0813-4993-860a-4c76cf8cca79)

where,
ρ = roh air density(Kg/m^3),
V = Velocity(m/s),
S = forntal area of the car(m^2),
Cd = Coefficient of Drag.

##### Rolling Resistance(Fr)

![rolling resistance](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/10082851-31d1-464c-be4b-37d09c8588cb)

where,
Cr = rolling resistance Coeffcient,
mT = Total mass of the car,
g = Acceleration due to gravity.

assuming the overall plant efficiency to be around 60-70 percent

##### The tesla model s P 85 uses a three phase AC four pole induction Motor.

for simplicity a Brushed Dc motor is used.

#### Brushed DC Motor

![brushed dc motor](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/512c0ac8-33e2-4e71-9d08-9907473b3e62)

according to Kirchhoff's the sum of all Voltages across a closed path in a circut equals zero.

![Kirchhoff's law](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/1ea1ca0c-ef26-4511-a8cc-81e40fdd581e)

where, 
v = voltage,
I = current,
R = resistance,
L = inductance
E = EMf

##### The torque in a DC motor can be written as,
#### T(t) = Kt*I(t)
where, Kt is the motor torque constant and I is the current. 

##### similarly, the Back EMF can be written as,
#### E(t) = Ke*w(t)
where, Ke is the Back EMF constant and w is the rotaional speed of the motor in (rad/s).

##### by combining the above equations and transforming into laplace domain, we get.

###### Torque as a function of voltage and rotational velocity

![dcmotormain equation](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/7d446ede-095a-4491-9c19-d68459a330a8)

## Simulink Model Implementation

![Screenshot (479)](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/9fb74311-8550-45e3-979a-c6069cc7af2a)

#### Results



