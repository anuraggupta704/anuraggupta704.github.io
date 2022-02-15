---
layout: post
title: "Different Topology optimization solvers used in Ansys"
categories: misc
tag: 
  - misc
---

In Ansys commercial FE package, two topology optimization solvers are present based on the SIMP (Solid isotropic material with penalization) method. These solvers include Optimality Criteria (OC) and Sequential Convex Programming (SCP).

1. **Sequential Convex Programming:** This method is an extension of the Method of Moving Asymptotes (MMA) solver. The MMA solver is a non-linear programming-based solver that approximates the optimized solution by solving separable convex subproblems. This solver extends MMA in such a way that it rejects steps that do not contribute with an optimized design. This solver requires derivative of all the functions in the topology optimization problem.
2. **Optimality Criteria:** This optimization solver is used when the objective function is compliance, and the constraint is either mass/volume or minimum member size. This solver is limited to use for simpler topology optimization problems. The OC solver suffers from slow convergence thereby requiring more number of iterations.
