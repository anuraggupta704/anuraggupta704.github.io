---
layout: post
title: "Uncertainities in Topology Optimization"
categories: misc
tag: 
  - misc
---

Various types of uncertainties are considered in the topology optimization, like uncertainty in loading, geometry and material properties, etc. Two methods account for the uncertainties in the topology optimization framework. They are-

**1. Probabilistic based methods (Statistical or reliability-based methods)**

**2. Non-probabilistic based methods**

The traditional approach to account for the uncertainties in the structure is the "Safety factor" approach. After that, the probabilistic methods have been adopted.

In the reliability-based methods, the reliability constraints are introduced based on the probability of failure. In such methods, the weight is minimized, and the failure probability is less than the prescribed value (Failure probability constraint). Since reliability constraints or probabilistic constraints are difficult to handle in the optimization process, several techniques have been used like FORM (first-order reliability method), SORM(second-order reliability method), etc. In the non-probabilistic based methods, the convex, interval, and fuzzy set models have been included. In the FORM approach, the probabilistic constraints have been evaluated by linearly approximating the limit state function.

The objective function in the deterministic optimization is the same as that of the reliability-based design optimization and the difference is only in their constraints.

The reliability index is used as a constraint in reliability-based optimization and the corresponding approach refers as the **"reliability index approach"**. Sometimes performance measure approach is also used to compute the reliability constraints.
