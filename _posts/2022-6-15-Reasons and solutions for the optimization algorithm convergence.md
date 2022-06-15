---
layout: post
title: "Reasons and solutions for the optimization algorithm convergence"
categories: misc
tag: 
  - misc
---

Various reasons are responsible when the optimization algorithm's convergence is not ensured. Some of the following steps are beneficial in fixing this issue:

1.  Ensure that the objective function and the constraints are appropriately formulated.

    

2. Ensure that the objective and constraint functions are continuous and differentiable at least up to the second order.

    

3. If the objective function and the constraints have different orders of magnitude, normalization is to be carried out before the optimization algorithm.

    

4. To run the optimization algorithm with different starting points. Sometimes algorithm diverges instead of convergence with some initial starting points.

    

5. Ensures the precision of the calculations performed.

    

6. Ensures that the gradients of the objective function and constraints are evaluated correctly.

    

7. The algorithm's termination or stopping criterion is not too tight, so it becomes difficult for the algorithm to compute the final solution accurately. Try to relax the stopping criterion.

    

8. Ignore some of the constraint functions and then try to solve the optimization problem. If the problem converges, add some more ignored constraints and solve the problem again. Repeat this process until the complete optimization algorithm converges.

    

9. Sometimes convergence issue is due to the unbounded nature of the problem. Try to add more constraints so that the optimization problem becomes bounded.

    

10. Keep a smaller limit on the number of iterations. Restart the algorithm with the starting solution kept as the final point of the previous run.

     

11. If the design variables have different orders of magnitude, scaling of the design variables has been performed. However, this scaling influences the gradient calculations.

     

12. Ensures that the optimization algorithm always converges to the local optimum with any assumed initial starting point. The authenticity of the algorithm can be checked by solving different problems with the known solutions available.
