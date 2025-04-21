# Verification-of-Convex-Function

# Overview

This assignment analyzes the convexity properties of three mathematical functions by simulating their behaviour and visualizing them with 3D plots. These functions come from convex optimization and matrix analysis and are often encountered in optimization and data science problems.

# Problem Statement

We are given the following functions and asked to determine whether each is convex:

(a) $f(x) = max_{i=1,..,m}||A^{(i)}x - b^{(i)}||_p$

(b) $f(X) = \sum^{n}_{i=1}\lambda_i(X)$, where $\lambda_i(X)$ are the eigenvalues of the symmetric matrix X.

(c) $f(X) = \lambda_{min}(X)$, the smallest eigenvalue of symmetric matrix X.

# Tools and Libraries

The following tools must be used in order to execute the above program

(1) Python 3.

(2) NumPy

(3) Matplolib

# Function Simulation

<ins> Part (a): Maximum of Norms</ins>

Function :

  $f(x) = max_i||A^{(i)}x - b^{(i)}||_p$

Approach :

-> Simulate this function over a 2D grid of input values x $\epsilon R^2$.

-> Use two sample affine transformations $A^{(i)}$ and offset vectors $b^{(i)}$.

-> Visualize with a 3D surface plot.

Conclusion :

-> The function is convex for p >= 1.

-> This is supported by the convexity of norms and the max operator over convex functions.

<ins> Part (b): Trace of a Symmetric Matrix </ins>

Function :

  $f(X) = \sum^{n}_{i=1} \lambda{i}(X) = trace(X)$

Approach :

-> Simulate 2x2 symmetric matrices of the form:

  $$
X = \begin{pmatrix}
a & b\\
b & c \\
\end{pmatrix}
  $$

-> Fix b = 1 and vary a,c

-> Use np.linalg.eigvalsh to compute the eigenvalues

Conclusion :

-> Trace is a linear function, hence both convex and concave.

-> 3D surface appears as a plane.

<ins> Part (c): Minimum Eigenvalue</ins>

Function :

$$
f(X) = \lambda_{min}(X)
$$

Approach :

-> Same symmetric matrix simulation as part (b).

-> Extract the minimum eigenvalue for each matrix.

-> Visualize over varying a and c.

Conclusion :

-> The function is concave, not convex.

-> This is evident from the downward curvature of the plot.

# How to Run

1. Install the dependencies

          pip install numpy matplotlib

2. Run the script or notebook to view the 3D plots and validate the convexity properties.

# Notes

1. For more rigorous verification of convexity, symbolic tools like cvxpy can be used.

2. Eigenvalue-based functions are common in SDP (semidefinite programming) and optimization over matrix variables.
