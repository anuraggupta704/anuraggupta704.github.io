---
layout: post
title: "Numerical Challenges occurs in SIMP based Topology Optimization"
categories: misc
tag: 
  - misc
---

**A)** **Checkerboard Pattern**:
a) Checkerboarding refers to the formation of alternate solid and void elements in the final topologically optimized structure and possesses artificial high stiffness to the numerical model.

b) This issue is primarily due to the discretization error of the numerical FE model.

c) It occurs mainly in those models which have been discretized using 4 noded linear quad elements because in such elements, the elemental force is transferred via corner nodes.

d) Certain methods are used to avoid the checkerboarding like the use of higher-order 8 or 9 noded elements (however some computational efforts increase), patching, perimeter constraint (enforce a constraint on the total perimeter of the material interface), nodal based formulation, filtering techniques, etc.

**B) Mesh dependency:**
a) Mesh dependency means that we will get different optimized designs for the same design domain under different levels of discretization.

b) This issue can be avoided by using perimeter constraints or mesh independent filtering.

**C) Local minima**:
a) The problems of the topology optimization are generally non-convex, meaning there are so many local minima exists for that problem.

b) It refers to the problem of getting different optimized results for the same level of discretized design domain when choosing different parameters of the optimization algorithm.

c) A small change in the move limit, no. of elements used for the discretization, geometry of design domain, values of the perimeter constraint or filter parameter, etc. will result in a major change in the final optimal design.

d) This problem is due to the non-convergence of the optimization algorithm and can be avoided to some extent by employing **continuation methods.** 

e) The penalty parameter in the penalization function also makes the problem non-convex which increases the local optimum solutions in context with topology optimization.

f) In the case of a non-convex problem, it is a usual practice to perform the optimization several times with different starting parameters and at the last, select the best optimum result from the various obtained optimized results. However, adopting this practice in the context of topology optimization is of no importance.

g) If penalty parameter (p) in the SIMP formulation is considered as 1, then the optimization problem becomes convex and has a unique solution. However, in the final design, intermediate densities will appear so that this design can't be manufacturable. If p>1 is used, then the intermediate densities penalize and we will get a crisp black and white solution. However, now the optimization problem becomes non-convex.

h) Some gradient-based optimizers are used to compute a local optimum for this non-convex problem. Different optimizers will give us different optimized results as a local optimum. Also, a minor change in the initial parameters will give us different optimum results. The continuation method is used which will converge results towards the global optimum.

> In the continuation method, initially at the start of the optimization, P=1 is used and it is gradually increased up to p=3 at every optimization iteration. In continuation methods, the optimization problem is gradually changed from convex to a non-convex problem in a no. of steps and in each step, the gradient-based optimization algorithm is employed until convergence.
