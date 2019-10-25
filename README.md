# Failure Mode Management


## Introduction
In this project, we aim to develop strategies to ensure safety for safety-critical systems under failure mode (sensor failure, controller failure, information extraction, etc.)

<!-- ## Papers to read

### Recoverable set 


### Positive invariant set


### Reachability set 
1. Introduction slide https://people.eecs.berkeley.edu/~somil/Papers/Introduction_to_Reachability_to_Share.pdf

2. Safe learning robot  
https://people.eecs.berkeley.edu/~jfisac/papers/General_Safe_Learning.pdf -->


## Faults handling in planning and control
 

### Robots

1. []()

### Autonomous Vehicle


### Platooning 
1. [Fault Tolerance of Cooperative Vehicle Platoons Subject to Communication Delay](https://reader.elsevier.com/reader/sd/pii/S2405896315015062?token=8B538BA79189CB769F2115A7A38F73A9E65D91DA5B18AE38DC104DDC80324CC870C55FAB2FEADAF3776AEF24A6694D16)

    Faults: Actuator(propeller) faults.

    Handling approach: Recoverable set based approach

### UAV
1. [Recoverable set computation for post-fault/failure quadrotors based on sum of squares (SOS)](https://ieeexplore.ieee.org/document/7739731)

    Faults:

    Handling approach:

2. [A General Safety Framework for Learning-Based
Control in Uncertain Robotic Systems](https://people.eecs.berkeley.edu/~jfisac/papers/General_Safe_Learning.pdf)

    Faults: This paper considers learning a controller online for UAV to track reference trajectory. The reachable set based method is used to ensure safety under the condition where the approximated model is correct. The fault in the learning process is defined as the model mismatch between the real system and the approximated model.

    Handling approach: An additional safety controller and Bayesian filter is used to handle the faults. Bayesian filter detects the faults and safety controller is triggered to ensure safety




## Simulation tools we have


### Carla simulator

We can model

* Sensor measurements for AV, including (Lidar, radar, camera)

* Vehicle platooning and muli-vehicle


### Fetch Robot simulator

We can model

* Sensor measurements


### CarSim

We can model

* Vehicle dynamics 

