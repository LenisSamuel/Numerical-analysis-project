﻿# Numerical analysis
Installation guide, user manual and error cases
Instalation guide. How to install the app: https://youtu.be/fJvpFcUOZOo?si=O-g7PON_V34Ncjxq 
User Manual. How to use the app: https://youtu.be/wVmrHQJCXDM 

Bisection
To ensure the accuracy and effectiveness of the secant method in calculating roots of functions, it is essential to meet the following conditions:

"x0 must be less than x1", since the bisection method works on a closed interval.
"The interval must contain a root of the function, i.e., f(x0) * f(x1) < 0"
The function to be evaluated must be continuous on the specified interval and must comply with the following format, i.e. x^3 + 7*x^2 - 60
Tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5

Incorrect Initial Interval:
Does not contain the root: If the interval [x0, x1] does not enclose any root of the function, the method will not be able to find it, as it will always divide an interval that does not contain the solution.
Contains multiple roots: If the interval contains more than one root, the method may converge to any of them, depending on the sequence of divisions.

Discontinuous Function in the Interval:
The bisection method assumes that the function is continuous in the interval. If the function has a discontinuity at any point in the interval, the method may fail or converge to a point of discontinuity instead of a root.

Tolerance Too Small:
If a very small tolerance is set, the method may require an excessive number of iterations to converge, or may not converge at all due to the limited precision of the computer.

Insufficient Maximum Number of Iterations:
If the maximum number of iterations is too low, the method may not have enough time to reach the specified tolerance, especially if the root is near one end of the interval.

False position
To ensure the accuracy and effectiveness of the False Rule method in calculating roots of functions, it is essential to meet the following conditions:

The "Value of a" and "Value of b" must be numeric values that define the initial interval where the root will be searched. The interval [a, b] must contain at least one root of the function.
The function to be evaluated must be continuous on the specified interval and must be entered in the appropriate format. Example: x^3 + 7*x^2 - 60.
The "Tolerance" must be entered in decimal format, such as 0.0001 or 0.5e-5, and represents the desired accuracy for the result.
The "Maximum number of iterations" must be a positive integer, which limits the number of iterations allowed.
Select the "Error Type" between absolute or relative to determine the convergence criterion.

Incorrect Initial Interval:
Does not contain the root: If the interval [a, b] does not enclose any root of the function, the method will not be able to find it, as it will always work within an interval that does not contain the solution.
Contains multiple roots: If the interval contains more than one root, the method may converge to any of them, depending on the sequence of iterations.

Discontinuous Function in the Interval:
The false position method assumes that the function is continuous in the interval. If the function has a discontinuity at any point in the interval, the method may fail or converge to a point of discontinuity instead of a root.

Tolerance Too Small:
If a very small tolerance is set, the method may require an excessive number of iterations to converge, or may not converge at all due to the limited precision of the computer.

Insufficient Maximum Number of Iterations:
If the maximum number of iterations is too low, the method may not have enough time to reach the specified tolerance, especially if the root is near one end of the interval.
Slow Convergence in Convex or Concave Functions:
The false position method may converge slowly if the function is convex or concave near the root, as the new approximation may always remain on the same side of the root.

Fixed point
To ensure the accuracy and effectiveness of the Fixed Point method in calculating roots of functions, it is essential to meet the following conditions:

The "Start Point" must be a numerical value that will serve as a starting point for the method.
The function f(x) must be continuous and must be entered in the appropriate format. Example: x^3 + 7*x^2 - 60.
The function g(x) must be appropriately transformed from f(x) so that x = g(x) corresponds to the desired solution.
The "Tolerance" must be entered in decimal format, such as 0.0001 or 0.5e-5, and represents the desired accuracy for the result.
The "Maximum number of iterations" must be a positive integer, which limits the number of iterations allowed.
Select the "Error Type" between absolute or relative to determine the convergence criterion.

Non-existence of a Fixed Point: If the function g(x) does not have a fixed point in the given interval, the method will not converge.
Convergence to a Different Fixed Point: If there are multiple fixed points, the method might converge to one that is not the desired root.
Divergence: If the absolute value of the derivative of g(x) at the fixed point is greater than 1, the iterations will move farther away from the fixed point, leading to divergence.
Cycling: The iterations might get stuck in a cycle, repeating the same sequence of values without converging.
Poor Choice of Starting Point: An initial guess that is too far from the actual root or in a region where g(x) behaves erratically can lead to slow convergence or divergence.
Improperly Defined g(x): If g(x) is not continuous or not well-defined in the given interval, the method may fail.


Newton
To ensure the accuracy and effectiveness of Newton's method, it is essential to meet the following conditions:

"Start point" must be a numeric value that will serve as the starting point for the method.
The function to be evaluated must be continuous and must comply with the following format. i.e. x^3 + 7*x^2 - 60
The tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5.
The derivative of the function must be entered in the appropriate format. Example: 3x^2 + 14x
The "Maximum number of iterations" must be a positive integer, which limits the number of iterations allowed.
Select the "Error Type" between absolute or relative to determine the convergence criterion.

Poor Initial Guess:
If the starting point is too far from the root, the method might diverge or converge to a different root.
A poorly chosen starting point can lead to oscillations or slow convergence.
Zero Derivative:
If the derivative of the function is zero at any point during the iteration process, the method breaks down as the iteration formula involves dividing by the derivative. This is often referred to as a "division by zero" error.
Multiple Roots:
For functions with multiple roots, the method might converge to a different root, depending on the initial guess.
The convergence rate can be slower near multiple roots.
Discontinuities:
If the function or its derivative is discontinuous near the root, the method might fail to converge.
Slow Convergence or Oscillations:
For certain functions or initial guesses, the method might converge very slowly or oscillate around the root without getting closer.


Secant
To ensure the accuracy and effectiveness of the secant method in calculating roots of functions, it is essential to meet the following conditions:

"XO" must be less than "XI", since the secant method works on a closed interval.
The function to be evaluated must be continuous on the specified interval and must comply with the following format. Exampl: x^3 + 7*x^2 - 60
The tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5.

Poor Initial Guesses:
Too far apart: If the initial guesses, X0 and X1, are too far apart, the method might overshoot the root and converge to a different one or diverge entirely.
Too close together: If the initial guesses are very close, the secant line might be nearly horizontal, leading to slow convergence or even division by zero in the iteration formula.
Function Discontinuities:
The secant method assumes that the function is continuous in the interval [X0, X1]. If there's a discontinuity within this interval, the method might produce meaningless results or fail to converge.
Multiple Roots:
For functions with multiple roots, the method might converge to a different root depending on the initial guesses. Convergence can also be slower near multiple roots.
Flat Regions:
If the function has a flat region near the root, the secant line might be nearly horizontal, leading to slow convergence or even stalling.
Oscillations:
In some cases, the method might oscillate between two points without converging to a root. This can happen if the function has a steep slope near the root.





Multiple roots
To ensure the accuracy and effectiveness of the Multiple Roots method, it is essential to meet the following conditions:

"Start point" must be a numeric value that will serve as the starting point for the method.
The function to be evaluated must be continuous and must comply with the following format. Example: x^3 + 7*x^2 - 60
The tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5.
The "Maximum number of iterations" must be a positive integer, which limits the number of iterations allowed.
Select the "Error Type" between absolute or relative to determine the convergence criterion.

Poor Initial Guess:
Far from the root: If the starting point is too far away from the actual root, the method might converge to a different root or diverge altogether.
At a local minimum or maximum: If the starting point is at a local minimum or maximum of the function, the method may get stuck there and fail to converge.
Incorrect Multiplicity Assumption:
The method often requires an estimate of the multiplicity of the root. If this estimate is inaccurate, the convergence can be slow or the method might fail to converge.
Error in Derivative Estimation:
Some multiple root methods require an estimate of the derivative of the function. If this estimate is inaccurate, it can lead to convergence issues.
Insufficiently Smooth Function:
If the function is not sufficiently smooth (i.e., does not have enough continuous derivatives) near the root, the method may struggle to converge.






Iterative methods / Gauss-Seidel
To ensure the accuracy and effectiveness of the iterative method, it is essential to meet the following conditions:

Fill in all fields and selectors. The matrix must be invertible, that there are no 0's on its diagonal
The tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5.

Non-Diagonally Dominant Matrix:
A sufficient (but not necessary) condition for the convergence of the Gauss-Seidel method is that the coefficient matrix of the system is diagonally dominant. This means that in each row, the absolute value of the diagonal element must be greater than the sum of the absolute values of the other elements in that row. If this condition is not met, convergence is not guaranteed.   

System of Equations Without a Unique Solution:
If the system of equations does not have a unique solution (i.e., it has infinitely many solutions or no solution), the Gauss-Seidel method will not converge to a specific solution.

Poor Initial Guess:
While not as critical as in other methods, the choice of the initial guess can influence the rate of convergence. A starting point that is far from the solution can increase the number of iterations required.

Insufficient Maximum Number of Iterations:
If the maximum number of iterations is set too low, the method may stop before reaching convergence, even if convergence is possible.







Iterative methods / Jacobi
To ensure the accuracy and effectiveness of the iterative method, it is essential to meet the following conditions:

Fill in all fields and selectors. The matrix must be invertible, that there are no 0's on its diagonal
The tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5.

Non-Diagonally Dominant Matrix:
A sufficient (but not necessary) condition for the convergence of the Jacobi method is that the coefficient matrix of the system is diagonally dominant. This means that in each row, the absolute value of the diagonal element must be greater than the sum of the absolute values of the other elements in that row. If this condition is not met, convergence is not guaranteed.   

System of Equations Without a Unique Solution:
If the system of equations does not have a unique solution (i.e., it has infinitely many solutions or no solution), the Jacobi method will not converge to a specific solution.

Poor Initial Guess:
The choice of the initial guess can influence the rate of convergence, although not as significantly as in some other methods. A starting point that is far from the solution can increase the number of iterations required.

Insufficient Maximum Number of Iterations:
If the maximum number of iterations is set too low, the method may stop before reaching convergence, even if convergence is possible.







Iterative methods / SOR
To ensure the accuracy and effectiveness of the iterative method, it is essential to meet the following conditions:

Fill in all fields and selectors. The matrix must be invertible, that there are no 0's on its diagonal
The tolerance can be entered in decimal format i.e. 0.0001 or floating point i.e. 0.5e-5.

Inadequate Selection of the Relaxation Parameter ω:
The value of ω plays a crucial role in the convergence of the method. If ω is outside the optimal range (generally between 1 and 2), the method may diverge. A value of ω that is too large can initially accelerate convergence but may lead to oscillations and divergence. A value of ω that is too small can slow down convergence.

Non-Diagonally Dominant Matrix:
While not a strict requirement, diagonal dominance of the matrix can favor convergence. If the matrix is not diagonally dominant, convergence is not guaranteed, even with a well-chosen ω.

System of Equations Without a Unique Solution:
Similar to the Jacobi and Gauss-Seidel methods, if the system of equations does not have a unique solution (i.e., it has infinitely many solutions or no solution), the SOR method will not converge to a specific solution.

Insufficient Maximum Number of Iterations:
If the maximum number of iterations is set too low, the method may stop before reaching convergence, even if convergence is possible.







Interpolation / Vandermonde
"You can add and remove columns as you wish."
"The X's must be arranged from smallest to largest."
"There should not be two X's with the same value."
"Do not leave empty spaces, if you do not use a column, delete it."

Ill-Conditioned Vandermonde Matrix:
The primary reason for the failure of the Vandermonde method is the ill-conditioning of the Vandermonde matrix. This matrix, constructed from the interpolation nodes, tends to be extremely ill-conditioned, especially when the nodes are closely spaced.
An ill-conditioned matrix means that small perturbations in the input data can lead to significant variations in the solution. This makes the method highly sensitive to rounding errors and noise in the data.

Runge's Phenomenon:
Runge's phenomenon is another common issue associated with high-degree polynomial interpolation. This phenomenon manifests as wild oscillations of the interpolating polynomial near the ends of the interpolation interval, even when the function being interpolated is smooth.
This occurs because high-degree polynomials tend to have high curvature, which can lead to undesirable results.

Sensitivity to Data Errors:
As mentioned earlier, the Vandermonde method is very sensitive to errors in the input data. Small perturbations in the y-values can cause large changes in the interpolating polynomial.

Computational Cost:
Constructing and solving the linear system of equations associated with the Vandermonde matrix can be computationally expensive, especially for a large number of data points.




Interpolation / Lagrange
"You can add and remove columns as you wish."
"The X's must be arranged from smallest to largest."
"There should not be two X's with the same value."
"Do not leave empty spaces, if you do not use a column, delete it."

Runge's Phenomenon:
Similar to the Vandermonde method, Lagrange interpolation can exhibit Runge's phenomenon, especially when using high-degree polynomials. This manifests as unwanted oscillations of the interpolating polynomial near the ends of the interpolation interval, even if the function being interpolated is smooth.

Sensitivity to Node Distribution:
The accuracy of Lagrange interpolation is highly dependent on the distribution of the interpolation nodes. If the nodes are clustered together in some regions and widely spaced in others, the interpolating polynomial may behave erratically in regions with widely spaced nodes.

Computational Cost:
While more efficient than the Vandermonde method, calculating Lagrange polynomials can still be computationally expensive, especially for a large number of data points.

Not Optimal for All Functions:
Lagrange interpolation is not optimal for all functions. For example, if the function being interpolated has discontinuities or high-order derivatives, the Lagrange polynomial may not be a good approximation.







Interpolation / Newton
"You can add and remove columns as you wish."
"The X's must be arranged from smallest to largest."
"There should not be two X's with the same value."
"Do not leave empty spaces, if you do not use a column, delete it."

Runge's Phenomenon:
Similar to Lagrange and Vandermonde methods, Newton's interpolation can exhibit Runge's phenomenon, especially when using high-degree polynomials. This manifests as unwanted oscillations of the interpolating polynomial near the ends of the interpolation interval, even if the function being interpolated is smooth.

Sensitivity to Node Distribution:
The accuracy of Newton's interpolation heavily depends on the distribution of the interpolation nodes. If the nodes are clustered together in some regions and widely spaced in others, the interpolating polynomial may behave erratically in regions with widely spaced nodes.

Computational Cost:
While Newton's method can be more efficient than Lagrange in some cases, calculating the divided differences can be computationally expensive, especially for a large number of data points.

Not Optimal for All Functions:
Like other polynomial interpolation methods, Newton's method is not optimal for all functions. For example, if the function being interpolated has discontinuities or high-order derivatives, the Newton polynomial may not be a good approximation.







Interpolation / Linear Spline
"You can add and remove columns as you wish."
"The X's must be arranged from smallest to largest."
"There should not be two X's with the same value."
"Do not leave empty spaces, if you do not use a column, delete it."

Lack of Smoothness:
The primary drawback of linear splines is that the resulting function is not smooth at the interpolation nodes. This means the first derivative of the function is not continuous at these points, which can lead to corners or abrupt changes in the slope of the curve. In applications where a smooth curve is required, such as in computer-aided design (CAD), this can be a problem.

Inflexibility to Capture Local Features:
Linear splines may not be able to capture local features of the function being interpolated, especially if the function has significant curvature between the nodes. This is because linear segments are relatively rigid and cannot easily adapt to abrupt changes in the function.

Sensitivity to Node Distribution:
Like other interpolation methods, the accuracy of linear spline interpolation is highly dependent on the distribution of the interpolation nodes. If the nodes are widely spaced, the interpolating polynomial may not be a good approximation of the function in that region.










Interpolation / Cubic Spline
"You can add and remove columns as you wish."
"The X's must be arranged from smallest to largest."
"There should not be two X's with the same value."
"Do not leave empty spaces, if you do not use a column, delete it."

Boundary Conditions:
The choice of boundary conditions can significantly influence the behavior of the cubic spline, especially at the endpoints of the interpolation interval. Inappropriate boundary conditions can lead to unwanted oscillations or inflexions in the spline.
Natural boundary conditions: While popular due to their simplicity, they may not be suitable for all problems, particularly if additional information about the derivatives at the endpoints is available.
Clamped boundary conditions: These impose specific values for the first derivatives at the endpoints but can be difficult to estimate if exact information is not known.

Number of Nodes:
An insufficient number of nodes can lead to an inaccurate representation of the function, especially in regions where the function varies rapidly. Conversely, an excessive number of nodes can increase computational complexity without significantly improving accuracy.

Node Distribution:
Non-uniform distribution of nodes can affect the quality of the interpolation. If nodes are highly concentrated in one region, the spline may be more accurate in that area but less accurate in others.

Round-off Error:
In numerical calculations, round-off errors can accumulate and affect the accuracy of the cubic spline, especially when using many nodes or working with limited precision.




Incremental Search
The Incremental Search method works by evaluating a function iteratively over small intervals to locate a root. The following conditions must be met:
           
"x0" is the starting point of the search.
"Delta" is the step size used for incrementing x0.
The function must be continuous in the search interval.
Tolerance is not directly used but iterations are limited by the "Maximum number of iterations."

Step Size:
Too large: If the step size is too large, it may skip over roots of the function, especially if they are closely spaced.
Too small: A very small step size can lead to a large number of iterations and increased computation time without a significant improvement in accuracy.

Nature of the Function:
Functions with many close roots: For functions with multiple roots that are very close together, the method may have difficulty identifying all roots or may converge to a false root.
Functions with discontinuities: If the function has discontinuities in the search interval, the method may fail to find all roots or may converge to a point of discontinuity.
Functions with very small derivatives: In regions where the derivative of the function is very small, the method may converge very slowly or may not converge at all.

Search Interval:
Too wide: A search interval that is too wide can increase computation time and make it difficult to identify roots.
Too narrow: A search interval that is too narrow may cause the method to miss any roots that lie outside the interval.


Computer Precision:
Round-off errors can accumulate and affect the accuracy of the results, especially if many iterations are performed.

LU Decomposition:
1.	Square matrix:
LU decomposition is typically performed on square matrices (n x n).
Possible error: "Matrix is not square. LU decomposition requires a square matrix."
2.	Non-singular matrix (no zero pivots):
The matrix must not be singular, meaning it should not have a determinant of zero. If any diagonal element of the matrix is zero during the decomposition process, the method cannot proceed without row swapping.
Possible error: "Singular matrix detected. LU decomposition cannot be performed."
3.	Valid matrix format:
The matrix A must be in a valid numerical format, such as a list of lists, a NumPy array, or a similar structured format.
Possible error: "Invalid input format. The matrix must be numerical and properly structured."
4.	Correctly defined independent vector (if solving systems):
When solving systems using LU decomposition, the right-hand side vector b should be defined and match the dimensions of A.
Possible error: "The vector b does not match the dimensions of matrix A."
5.	Floating-point precision:
LU decomposition is sensitive to floating-point errors, especially with ill-conditioned matrices.
Possible error: "Floating-point precision error detected. The results may not be accurate."
6.	Zero pivot elements:
If a pivot element during the decomposition is zero, the method will fail unless row interchanges are performed.
Possible error: "Zero pivot encountered. The matrix may need row swapping."
7.	Ill-conditioned matrices:
LU decomposition may still work on ill-conditioned matrices, but the result may not be numerically accurate. Ill-conditioned matrices have very small or large eigenvalues, which can lead to instability.
Possible error: "The matrix is ill-conditioned. Results may be unreliable."
8.	Overflows or underflows during calculations:
If the matrix elements are very large or very small, numerical overflows or underflows might occur during the LU decomposition process.
Possible error: "Numerical overflow or underflow detected during LU decomposition."
9.	Row interchanges or permutations (for numerical stability):
If pivoting is used to swap rows, and no valid pivot can be found, the decomposition will fail.
Possible error: "Row interchange failed. The matrix may be singular or have no solution."

LU with Pivoting:
1.	Square matrix:
The matrix must be square (i.e., the number of rows and columns must be equal).
Possible error: "The matrix is not square. LU decomposition with pivoting cannot be performed."
2.	Correct matrix format:
The matrix must be provided in a valid numerical format, such as a list of lists or a NumPy array.
Possible error: "Invalid input format. The matrix must be numerical and properly structured."
3.	Pivot not found (no non-zero values in the current column):
When pivoting, there might be no non-zero values in the current column to swap with the pivot, which typically happens if the matrix is singular.
Possible error: "No valid pivot found in column X. The matrix might be singular."
4.	Dimension compatibility of the independent vector (in linear systems):
When solving A * x = b, the vector b must have the same number of rows as the matrix A.
Possible error: "Dimension mismatch between matrix A and vector b."
5.	Non-singular matrix:
Even with partial pivoting, the method cannot proceed if the matrix is singular (i.e., determinant is zero).
Possible error: "The matrix is singular. LU decomposition cannot be performed."
6.	Valid format of the independent vector:
When solving A * x = b, the vector b must contain numerical values only, without invalid entries (e.g., strings or NaN).
Possible error: "Vector b contains invalid or non-numerical values."
7.	Small pivot leading to instability:
Even with partial pivoting, if the largest absolute value in the current column (pivot) is very small, numerical rounding errors can cause significant inaccuracies.
Possible error: "The pivot is too small. The decomposition may be unstable."
8.	Row swap index out of bounds:
During row swaps for pivoting, ensure that the indices do not exceed the matrix dimensions.
Possible error: "Row index out of bounds during row swapping. Check the matrix dimensions."
9.	Tolerance for approximations (optional):
If using a convergence criterion based on tolerance, it must be a small positive value.
Possible error: "Invalid tolerance. It must be a small positive number."
10.	Maximum number of iterations (optional):
When solving triangular systems, a maximum iteration limit must be set to prevent infinite loops.
Possible error: "Maximum number of iterations exceeded while solving the triangular system."

Simple Gaussian Elimination:
1.	Square or consistent rectangular matrix:
For solving A * x = b, A must have dimensions compatible with b (number of rows in A equals the number of elements in b).
Possible error: "Dimension mismatch between matrix A and vector b."
2.	Non-singular matrix (no zero rows in a fully reduced row echelon form):
If the matrix is singular (determinant is zero), Gaussian elimination cannot provide a unique solution.
Possible error: "The matrix is singular. Gaussian elimination cannot be performed."
3.	No division by zero during elimination:
If a pivot element is zero, division will result in an error unless row swapping is performed.
Possible error: "Division by zero encountered during elimination. Consider row swapping or pivoting."
4.	Valid matrix format:
The matrix A must be provided in a valid numerical format, such as a list of lists or a NumPy array.
Possible error: "Invalid input format. The matrix must be numerical and properly structured."
5.	Numerical stability (optional):
Simple Gaussian elimination can suffer from numerical instability in ill-conditioned matrices, leading to large rounding errors.
Possible error: "The matrix is ill-conditioned. Results may be inaccurate."
6.	Correctly defined independent vector:
The vector b in A * x = b must be numeric and free of invalid entries (e.g., NaN, strings, or null values).
Possible error: "The vector b contains invalid or non-numerical values."
7.	Floating-point precision:
Errors may accumulate due to the limitations of floating-point arithmetic, especially for very large or very small values.
Possible error: "Floating-point precision errors detected. Results may not be accurate."
8.	Zero rows or zero solutions:
If the elimination results in one or more rows of zeros but with inconsistent right-hand side values, the system has no solution.
Possible error: "The system has no solution (inconsistent equations)."
9.	Overflow or underflow:
For very large or very small numerical entries, numerical overflow or underflow can occur during computations.
Possible error: "Numerical overflow or underflow detected during computation."
10.	Row interchange limitations:
Simple Gaussian elimination does not inherently include pivoting. If a zero is encountered as a pivot, the method may fail unless manual row interchange is implemented.
Possible error: "Zero pivot detected. Consider using Gaussian elimination with pivoting."


Gaussian Elimination with Partial Pivoting:
1.	Square or consistent rectangular matrix:
For solving A * x = b, the matrix A must have the same number of rows as the number of elements in vector b.
Possible error: "Dimension mismatch between matrix A and vector b."
2.	Non-singular matrix (pivot elements cannot be zero):
If a pivot element is zero, partial pivoting must be applied to swap rows. If no non-zero pivot can be found, the matrix is singular and no solution exists.
Possible error: "Singular matrix detected. Pivot element is zero and no row swaps can resolve it."
3.	Valid matrix format:
The matrix A must be provided in a valid numerical format, such as a list of lists or a NumPy array.
Possible error: "Invalid input format. The matrix must be numerical and properly structured."
4.	Numerical stability:
Gaussian elimination with partial pivoting helps improve stability, but if the matrix is ill-conditioned, the method may still produce inaccurate results due to floating-point errors.
Possible error: "The matrix is ill-conditioned. Results may be unreliable."
5.	Correctly defined independent vector:
The vector b must be a numeric array or list with the same number of rows as matrix A.
Possible error: "The vector b contains invalid or non-numerical values."
6.	Floating-point precision:
Due to the limitations of floating-point arithmetic, numerical errors can accumulate, especially when the matrix values are very large or very small.
Possible error: "Floating-point precision errors detected. Results may not be accurate."
7.	Row interchange limitations:
If partial pivoting requires swapping rows and the algorithm cannot find a valid row to swap, the system may be inconsistent or singular.
Possible error: "No valid row to swap. The matrix may be singular or inconsistent."
8.	Zero rows or zero solutions:
If elimination results in rows of zeros, but the corresponding element in the vector b is non-zero, the system has no solution.
Possible error: "The system has no solution (inconsistent equations)."
9.	Overflow or underflow:
For very large or very small numerical entries, overflow or underflow may occur during computations.
Possible error: "Numerical overflow or underflow detected during computation."
10.	Pivoting index out of bounds:
During partial pivoting, row swaps must not go out of bounds.
Possible error: "Row index out of bounds during row swapping."

Gaussian Elimination with Full Pivoting:
1.	Square or consistent rectangular matrix:
For solving A * x = b, the matrix A must have the same number of rows as the number of elements in vector b.
Possible error: "Dimension mismatch between matrix A and vector b."
2.	Non-singular matrix (pivot elements cannot be zero):
If a pivot element is zero, full pivoting will attempt to swap both rows and columns. However, if no non-zero pivot can be found, the matrix is singular, and no solution exists.
Possible error: "Singular matrix detected. Pivot element is zero, and no row or column swaps can resolve it."
3.	Valid matrix format:
The matrix A must be provided in a valid numerical format, such as a list of lists or a NumPy array.
Possible error: "Invalid input format. The matrix must be numerical and properly structured."
4.	Numerical stability:
Full pivoting improves numerical stability, but the method can still produce inaccurate results for ill-conditioned matrices.
Possible error: "The matrix is ill-conditioned. Results may be unreliable."
5.	Correctly defined independent vector:
The vector b must be a numeric array or list with the same number of rows as matrix A.
Possible error: "The vector b contains invalid or non-numerical values."
6.	Floating-point precision:
Floating-point arithmetic limitations may lead to numerical errors, especially when matrix values are very large or very small.
Possible error: "Floating-point precision errors detected. Results may not be accurate."
7.	Row and column interchange limitations:
Full pivoting involves both row and column swaps. If the algorithm cannot find a valid row or column to swap, the system may be inconsistent or singular.
Possible error: "No valid row or column to swap. The matrix may be singular or inconsistent."
8.	Zero rows or zero solutions:
If elimination results in rows of zeros, but the corresponding element in the vector b is non-zero, the system has no solution.
Possible error: "The system has no solution (inconsistent equations)."
9.	Overflow or underflow:
Very large or very small numerical entries may cause overflow or underflow during computations.
Possible error: "Numerical overflow or underflow detected during computation."
10.	Pivoting index out of bounds:
During full pivoting, row and column swaps must not go out of bounds.
Possible error: "Row or column index out of bounds during row or column swapping."
