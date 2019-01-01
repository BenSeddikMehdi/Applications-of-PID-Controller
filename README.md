# Applications-of-PID-Controller


## Physical setup

A common actuator in control systems is the DC motor. It directly provides rotary motion and, coupled with wheels or drums and cables, can provide translational motion. The electric equivalent circuit of the armature and the free-body diagram of the rotor are shown in the following figure.


![dc motor](https://user-images.githubusercontent.com/43390471/50570667-635a7a80-0d8b-11e9-835f-a85e0b71e022.png)

For this example, we will assume the following values for the physical parameters. These values were derived by experiment from an actual motor in Carnegie Mellon's undergraduate controls lab.

(J)     moment of inertia of the rotor     3.2284E-6 kg.m^2

(b)     motor viscous friction constant    3.5077E-6 N.m.s

(Kb)    electromotive force constant       0.0274 V/rad/sec

(Kt)    motor torque constant              0.0274 N.m/Amp

(R)     electric resistance                4 Ohm

(L)     electric inductance                2.75E-6H


In this example, we assume that the input of the system is the voltage source ($V$) applied to the motor's armature, while the output is the position of the shaft ($theta$). The rotor and shaft are assumed to be rigid. We further assume a viscous friction model, that is, the friction torque is proportional to shaft angular velocity.


## System equations

In SI units, the motor torque and back emf constants are equal, that is, $K_t = K_e$; therefore, we will use $K$ to represent both the motor torque constant and the back emf constant.

From the figure above, we can derive the following governing equations based on Newton's 2nd law and Kirchhoff's voltage law :









