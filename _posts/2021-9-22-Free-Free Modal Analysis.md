---
layout: post
title: "Free-Free Modal Analysis"
categories: misc
tag: 
  - misc
---

**Modal analysis is called the mother of all dynamic analysis** because modal analysis is a prerequisite before performing any dynamic analysis. The modal analysis captures the dynamic characteristics of the vibrating system like natural frequency and mode shapes. The natural frequency is the inherent frequency of the vibrating system at which the system tends to vibrate without the action of any externally applied forces and the mode shape represents the corresponding vibrating pattern of the system at a specified natural frequency.

If the modal analysis is carried out for a system without any boundary condition or for an unconstrained system, then that type of analysis is referred to as free-free modal analysis. That means modal analysis is to be performed for a system without any specified boundary condition. In free-free modal analysis, the first six natural frequencies come to be zero or close to zero that signifies the six **rigid body modes** (three translational and three rotational). The seventh natural frequency is the first natural frequency for a constrained system.

Free-free modal analysis is to be carried out in the design phase when we are interested to find out the behavior of a system when it is under constrained. Also, this type of analysis is used to determine the dynamic characteristics of an unconstrained system like aircraft, missiles, ships, etc. There is no deformation observed in the system under rigid body modes. This can be illustrated using the following case study. In the case study, the modal analysis of the cantilever beam is to be performed both for the case when it is constrained and unconstrained.

### Case 1: When the system is unconstrained (no boundary condition is applied)

After doing modal analysis, the first six natural frequencies for a system are:

| Mode | Frequency [Hz] |
| :--- | :------------- |
| 1    | 0              |
| 2    | 0              |
| 3    | 9.274e-005     |
| 4    | 2.4602e-004    |
| 5    | 2.6525e-004    |
| 6    | 4.1306e-004    |

The corresponding mode shapes are:

![img](https://i0.wp.com/computationalmechanics.in/wp-content/uploads/2021/09/mode3_rigid.jpg?resize=398%2C252&ssl=1)Mode 3

![img](https://i1.wp.com/computationalmechanics.in/wp-content/uploads/2021/09/mode4_rigid.jpg?resize=389%2C268&ssl=1)Mode 4

### Case 2: When the system is constrained (suitable boundary condition is specified)

After doing modal analysis, the first six natural frequencies for a system are:

| Mode | Frequency [Hz] |
| :--- | :------------- |
| 1    | 9.7846         |
| 2    | 19.569         |
| 3    | 61.321         |
| 4    | 116.08         |
| 5    | 122.64         |
| 6    | 171.74         |

The corresponding mode shapes are:

![img](https://i2.wp.com/computationalmechanics.in/wp-content/uploads/2021/09/mode3_deformable.jpg?resize=392%2C296&ssl=1)Mode 3

![img](https://i2.wp.com/computationalmechanics.in/wp-content/uploads/2021/09/mode4_deformable.jpg?resize=380%2C242&ssl=1)Mode 4

So, it is clearly shown from the figures that when the system is unconstrained, there is no internal deformation observed in the system (rigid body modes), and when appropriate boundary conditions are imposed on that system, there is some internal deformation observed in the system.
