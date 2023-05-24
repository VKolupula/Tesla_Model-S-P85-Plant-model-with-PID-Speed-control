# Model and simulate an electric car (Tesla Model S) in MATLAB & SIMULINK with PID speed controller.

### vehicle parameters

![Screenshot (480)](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/652d6fdf-ad83-40ae-8631-b8d2ebbed8a4)

![car_dynamics](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/07a4e91b-7536-4372-8da6-23b0609ca93d)

## Newton's laws of motion 
### Σ F = Ma.
#### Tractive Force(Ff) + Rolling Resistance(Fr) + Aerodynamic drag(D) = Mass * Acceleration

##### Tractive Force(Ff)

![tractive force](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/afb39d04-280b-44cf-b2ec-47573a77c1d2)


where,
T = torque(Nm),
L = Radius of Wheel(m),
Gr = Gear ratio.

##### Aerodynamic Drag(D)

![areodynamic drag](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/8790004a-712d-47c6-9428-614a38ba68a1)

where,
ρ = roh air density(Kg/m^3),
V = Velocity(m/s),
S = forntal area of the car(m^2),
Cd = Coefficient of Drag.

##### Rolling Resistance(Fr)

![rolling resistance](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/df68e433-9fe5-41db-b5d5-37e7afe1cf00)

where,
Cr = rolling resistance Coeffcient,
mT = Total mass of the car,
g = Acceleration due to gravity.

assuming the overall plant efficiency to be around 60-70 percent

##### The tesla model s P 85 uses a three phase AC four pole induction Motor.

for simplicity a Brushed Dc motor is used.

#### Brushed DC Motor

![brushed dc motor](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/b0d55cc2-f482-4647-aa1f-c2880bcc1200)

according to Kirchhoff's the sum of all Voltages across a closed path in a circut equals zero.

![Kirchhoff's law](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/6dfa4735-5a60-4fea-a589-148b18983673)

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

![dcmotormain equation](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/1bc2cfd9-c2a5-49d3-8b68-1bb1a97e687b)

## Simulink Model Implementation

![Screenshot (479)](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/d5a4f248-7ac6-4e26-b573-3409f4de5860)

#### Results

![velocity](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/7f5d8aad-ef01-4424-b647-e2dda652aef5)

![torque](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/3309cd90-2fd8-4d82-90ee-b30005b3c911)

![acceleration](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/7d002bc5-262b-44cc-a243-a1e5903acdc5)

![TsvNv](https://github.com/VKolupula/Tesla_Model-S-P85-Plant-model-with-PID-Speed-control/assets/120835150/709acf82-cb4b-4981-adee-50b40ef95e63)


