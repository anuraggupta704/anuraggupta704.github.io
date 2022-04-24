---
layout: post
title: "Mesh refinement in Topology Optimization"
categories: misc
tag: 
  - misc
---

1. Mesh refinement or discretization is a fundamental step in finite element analysis. In finite element analysis, the refinement of mesh is done only in those areas that are of interest (eg: the region of high stress in the stress analysis) so that to obtain good accuracy with minimum computational efforts. However, in the context of topology optimization, the purpose of mesh refinement is somewhat different. 

2. In topology optimization, mesh refinement is generally used to generate smooth boundaries. 

3. The final topology obtained in the topology optimization is unknown before doing the optimization, so most optimization algorithms begin with a uniform coarse mesh. But it results in the jagged boundaries or material of intermediate density around the members. These jagged or rough boundaries are not desirable in the final obtained topology optimized structure. 

4. To remove such jagged or irregular boundaries, it is desirable to use a more uniform fine mesh initially, but it is not computationally efficient. 

5. Also, using very fine mesh in the initial will result in very thin members due to mesh dependency. These thin members are not desirable due to the manufacturable issue. However, the problem of thin members can be removed by adopting suitable filtering techniques. The filtering causes an additional issue i.e to produce fuzzy or blurred boundaries of intermediate density around the member or at material interface. To lessen the blurred boundary effect, threshold function is used.

> In typical topology optimization problems, one can use fine mesh to obtain high-resolution topology. But the major drawback to this approach is that the fine mesh gives topology with very thin members and increases the computational cost. These thin members are not easily manufacturable and prone to failure. In the adaptive mesh refinement (AMR) technique, one can start with a coarse mesh and then refine it in those areas where it is needed. The AMR technique is also computationally efficient and produces members of desired thickness and smooth surfaces. So, suppose we use adaptive mesh refinement in topology optimization. In that case, we can avoid the jagged boundaries obtained due to the uniform coarse mesh and prevent the occurrence of very thin members produced due to fine uniform mesh.
