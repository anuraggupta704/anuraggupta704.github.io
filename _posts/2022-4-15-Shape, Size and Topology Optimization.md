---
layout: post
title: "Shape, Size and Topology Optimization"
categories: misc
tag: 
  - misc
---

Structural optimization is the process of determining the best possible material distribution within a physical volume domain, so as to safely transmit the applied load. To achieve this, the constraints imposed by the manufacturer and eventual use must also be taken into consideration. Some of these may include increasing stiffness (increasing strain energy or minimizing compliance), minimizing stress levels, minimizing displacement, altering the fundamental natural frequency, increasing the buckling load.

1**. Size Optimization:**

In Size optimization, the designer knows what the structure will look like, but does not know the size of the components which make up that structure. For example, if a cantilever beam was going to be used, its length and position may be known, but not its cross-sectional dimensions. Another example would be a truss structure where its overall dimensions may be known but not the cross-sectional areas of each truss element (bar). Yet another example would be the thickness distribution of a shell structure. So basically, any feature of a structure where its size is required, but where all other aspects of the structure are known.

2**. Shape Optimization:**

In Shape optimization, the unknown is the form or contour of some part of the boundary of a structural domain. The shape or boundary could either be represented by an unknown equation or by a set of points whose locations are unknown.

**3. Topology Optimization:**

Topology optimization is the most general form of structural optimization. In discrete cases, such as for truss structures, it is achieved by allowing the design variables, such as the cross-sectional areas of the truss members, to have a value of zero or a minimum gage size. For continuum-type structures in two dimensions (2D), topology changes can be achieved by allowing the thickness of a sheet to have values of zero at different locations, thereby determining the number and shape of the cavities (holes). For continuum type structures in three dimensions (3D), the same effect can be achieved by having a density-like variable that can take any value down to zero.
                                

 In size and shape optimization, the size and shape of the components of a structure can be manipulated. They can have any value within their limits, but they must always be present. But if the designer/engineer does not know what the shape or size of the structure should be, then topology optimization needs to be used. The basic flowchart depicts the process of the Topology optimization is shown in the following figure. 

![img](https://computationalmechanics.in/wp-content/uploads/2022/04/Topology-optimization-SIMP-1-447x1024.png)Basic flowchart of Topology Optimization

> 
