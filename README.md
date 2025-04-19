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

      
