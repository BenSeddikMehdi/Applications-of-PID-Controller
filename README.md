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


![01](https://user-images.githubusercontent.com/43390471/50570709-4757d880-0d8d-11e9-90f0-a0a7865565e2.png)

![02](https://user-images.githubusercontent.com/43390471/50570717-7d955800-0d8d-11e9-95ff-6dc1629f5262.png)

## Second Model / S Domain

In this Model we decided to start converting the first Model Of DC Motor which means find the dual of the model so.

However, during this example we will be looking at the position as the output. We can obtain the position by integrating the speed, therefore, we just need to divide the above transfer function by s.

![03](https://user-images.githubusercontent.com/43390471/50570925-b71d9180-0d94-11e9-9e7c-77b68aac6d9f.png)


We replaced the Developed Model of DC Motor with its correponding transfer function. The figure below shows us the change :


![transferfunction](https://user-images.githubusercontent.com/43390471/50570956-60648780-0d95-11e9-8d43-a86ec04b8442.png)




















