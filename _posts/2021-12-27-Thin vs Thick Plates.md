---
layout: post
title: "Thin vs Thick Plates"
categories: misc
tag: 
  - misc
---

Thin plates are flat structural members with two parallel planes called **faces** and a cylindrical surface called an **edge or boundary**. The plate’s thickness ” *h”* is defined as the distance between the plane faces. The plates can withstand static or dynamic loads that are mostly perpendicular to their faces. Thin plates have several advantages, including their light weight and high load-carrying capacity. As a result, they are used in many fields of technology, including civil, mechanical, and aeronautical.

​               Consider a plate whose thickness ” *h”* is divided into equal halves by a plane that is parallel to its faces. This plane is called as the **middle plane** of the plate. When the plate is subjected to transverse loads, the plate initially flat deforms and the middle plane changes into some curvilinear surface known as the **middle surface**.

![img](https://i1.wp.com/computationalmechanics.in/wp-content/uploads/2021/12/plate_midplane.jpg?resize=300%2C205&ssl=1)

The plates resist transverse loads primarily through bending action, and the flexure properties of the plate are determined by its thickness parameter. Plates can be divided into several groups based on their ***a/h*** ratio, where ” *h”* is the thickness of the plate and ” *a”* is its dimension.

1. **Thick Plates:** Plates can be categorised as thick plates when the ratio *a/h* < 8….10. The analysis of such plates involves the use of governing equation for the three dimensional elastic solid bodies. They follows **Reissner-Mindlin formulation** that accounts for transverse shear deformations.

2. **Membranes:** Plates can be categorised as membranes when the ratio *a/h* > 80….100.

3. **Thin Plates:** Plates can be categorised as thin plates when 8…10 < *a/h* < 80….100. They follows **Kirchoff formulation** that neglects the transverse shear deformations. The Kirchhoff–Love theory which is a two-dimensional mathematical model is used to determine the stresses and deformations in thin plates subjected to forces and moments. Depending on the value of the ratio *w/h*, i.e the ratio of maximum deflection of plate to its thickness, the part of flexural and membrane forces here may be different. As a result, this group can be further classified as follows:

   **a) Stiff Plates:** When the *w/h* ratio is less than and equal to 0.2, a plate is classified as stiff. They are flexurally rigid thin plates that support loads in two dimensions, primarily through internal bending and twisting moments and transverse shear forces. The deformation of the middle plane and the membrane forces are negligible in this case.

   **b) Flexible Plates:** When the *w/h* ratio of a plate is greater than and equal to 0.3, it is classified as a flexible plate. These plates are a hybrid of stiff plates and membranes that carry external loads through the combined action of internal moments, shear forces, and membrane (axial) forces.
