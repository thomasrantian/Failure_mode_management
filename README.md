# Failure Mode Management


# Introduction

In this project, we aim to develop strategies to ensure safety for safety-critical systems under failure mode (sensor failure, controller failure, information extraction, etc.)

<!-- ## Papers to read

### Recoverable set 


### Positive invariant set


### Reachability set 
1. Introduction slide https://people.eecs.berkeley.edu/~somil/Papers/Introduction_to_Reachability_to_Share.pdf

2. Safe learning robot  
https://people.eecs.berkeley.edu/~jfisac/papers/General_Safe_Learning.pdf -->


# Faults handling in planning and control
 

## Vehicle steering system faults


+ [Steering Redundancy for Self-Driving Vehicles using Differential Braking](https://www.tandfonline.com/doi/abs/10.1080/00423114.2017.1356929)

    - Vehicle steering system fails, differential braking is used as a secondary actuator to control the vehicle to track a curvature, the control strategy is PID, speed control is not considered; no fault detection, assuming fault is known.


+ [Passive fault-tolerant path following control of autonomous distributed drive electric vehicle considering steering system fault](https://www.sciencedirect.com/science/article/pii/S0888327019300196)

    - Vehicle steering system (partial) fails; Kalman filter is applied to estimate the vehicle steering system fault; sliding mode control method is proposed to facilitate path following controller; tire force allocation method is used to execute the control efforts of upper layer controller.

## Tire system faults

+ [A Fault Tolerant Vehicle Stability Control Using Adaptive Control Allocation](https://asmedigitalcollection.asme.org/DSCC/proceedings-abstract/DSCC2018/51890/V001T09A002/455564)

    - Brakes, motors and steering are controlled simultaneously using an adaptive control allocation strategy; the strategy shows safe performance under tire traction force faults.

+ [Vibration-Based Propeller Fault Diagnosis for Multicopters](https://ieeexplore.ieee.org/document/8453400)

    - Only faults detection; detecting faults (physical damage to a propeller) in a multicopter’s motor/propeller by analysis of the vibration spectrum measured by accelerometer (under pre-defined flight trajectories).


## UAV propeller faults

+ [A Model-based Active Fault Tolerant Control Scheme for a Remotely Operated Vehicle](https://www.sciencedirect.com/science/article/pii/S240589631832384X)

    - Underwater vehicle thruster faults; sliding mode observer to estimate the faults, control allocation algorithm to redistributes the control effort.



## AV perception faults

+ [Kinematics-based Fault-tolerant Techniques: Lane Prediction for an Autonomous Lane Keeping System](https://link.springer.com/article/10.1007/s12555-017-0449-8)

    - The vision system fails to identify the (partial or complete) road lanes. kinematic motion model-based lane estimation scheme covers possible camera vision sensor.

## AV sensor measurement faults
+ [Effective fault-tolerant control paradigm for path tracking in autonomous vehicles](https://www.tandfonline.com/doi/full/10.1080/21642583.2014.1002138)

    - Two sets of sensors to measure lateral displacement of a vehicle; observer-based method to detect failure of the sensors; the measurements from the two sets of sensors are fused (weighted) based on fault detection; LQR is used to control vehicle stability.


## Model mismatch faults in safety-critical systems  

+ [A General Safety Framework for Learning-Based Control in Uncertain Robotic Systems](https://people.eecs.berkeley.edu/~jfisac/papers/General_Safe_Learning.pdf)

    - This paper considers learning a controller online for UAV to track reference trajectory. The reachable set based method is used to ensure safety under the condition where the approximated model is correct. The fault in the learning process is defined as the model mismatch between the real system and the approximated model. An additional safety controller and Bayesian filter is used to handle the faults. Bayesian filter detects the faults and safety controller is triggered to ensure safety.


+ [Robust Tracking with Model Mismatch for Fast and Safe Planning: an SOS Optimization Approach](https://arxiv.org/abs/1808.00649)
    
    - Fault is modeled as model mismatch between the model (reduced-order) used to generate the motion plan and the system’s model; trajectory-independent tracking error bound is computed based on the sum of squares programming and is accounted in the path planning to ensure safety.

+ [On Infusing Reachability-Based Safety Assurance within Probabilistic Planning Frameworks for Human-Robot Vehicle Interactions](http://asl.stanford.edu/wp-content/papercite-data/pdf/Leung.Schmerling.Chen.ea.ISER18.pdf)

    - Fault is modeled as the wrongly predicted or unexpected behaviors of a human-driven vehicle interacting with an AV. A set of unsafe states is computed by assuming fully adversarial human driver and Reachability Analysis, and is imposed as constraints of the MPC controller.

+ [Safe Platooning of Unmanned Aerial Vehicles via Reachability](https://arxiv.org/abs/1503.07253)
    - One of the UAV in a platoon may behave unexpectedly due to faults, which may lead to an unsafe configuration; HJR is used to ensure safety.



# Simulation tools we have


## [Carla simulator](https://github.com/carla-simulator/carla)

We can model

* AV interacts with human-driven vehicles

* Vehicle platooning 

* Full sensor readings (Lidar, radar, IMU, etc.)


## [Fetch Robot simulator](https://docs.fetchrobotics.com/manipulation.html)

We can model

* Robot navigation

* Robot manipulation

* Full sensor readings (Lidar, radar, IMU, etc.)

## [CarSim](https://www.carsim.com/products/carsim/index.php)

We can model

* Vehicle dynamics

