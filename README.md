# A matlab implementation of the Newton correction methods described in

A. Jaffe, R. Weiss and Boaz Nadler
Newton correction methods for computing real eigenpairs of symmetric tensors (2017)
The package includes a main script and tensor examples to generate Figure 6 (right).

To run the newton correction method:
[x,lambda,ctr,run_time,converge] = ...
    newton_correction_method(T,max_itr,delta,x_init)

To run the orthogonal newton correction method:
[x,lambda,ctr,run_time,converge] = ...
    orthogonal_newton_correction_method(T,max_itr,delta,x_init)

where 

Input:    T - A cubic real and symmetric tensor
          max_itr - maximum number of iterations until termination
          delta - convergence threshold
          x_init(opt) - initial point

DEFAULT:
	   if nargin<4 x_init is chosen randomly over the unit sphere

Output:   x - output eigenvector
          ctr - number of iterations till convergence
          run_time - time till convergence
          convergence (1- converged)
