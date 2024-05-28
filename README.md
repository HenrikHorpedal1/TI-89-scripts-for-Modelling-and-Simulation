# TI-89-scripts-for-Modelling-and-Simulation
A handfull of usefull functions for the course TTK4130 - Modelling and Simulation

## Rotation matricies
`rotx(ϕ)`:

$$
\mathbf{R}_x(\phi) =
\begin{pmatrix}
1 & 0 & 0 \\
0 & \cos \phi & -\sin \phi \\
0 & \sin \phi & \cos \phi
\end{pmatrix}
$$



`roty(θ)`:

$$
\mathbf{R}_y(\theta) =
\begin{pmatrix}
\cos \theta & 0 & \sin \theta \\
0 & 1 & 0 \\
-\sin \theta & 0 & \cos \theta
\end{pmatrix}
$$

`rotz(ψ)`:

$$
\mathbf{R}_z(\psi) =
\begin{pmatrix}
\cos \psi & -\sin \psi & 0 \\
\sin \psi & \cos \psi & 0 \\
0 & 0 & 1
\end{pmatrix}
$$


## Skew-symmetric matrix of a vector
`skews(invec)`
Only works for 3-element column-vectors.
If invec is `[a;b;c]`, `skews(invec)` would return:

$$
\begin{pmatrix}
0 & -c & b \\
c & 0 & -a \\
-b & a & 0
\end{pmatrix}
$$

## Lagrangian equations of motion
after calling `lagfunc()`: 
- You are asked to enter number of generalized coordinates, for instance 2.
- You are asked to enter T. use g1, g2, g1dot, g2dot, g3....etc as you generalized coordinates and their derivative
- You are asked to ender V. same procedure.

- The lagrange equation of motion will be displayed on the I/O screen, but because of limited space the equations will be saved as lagr_lst in memory for better viewing on the home screen.

Note: If your T or V equations start with a minus sign you have to use `(-)` istead of `-` on "the first minus"

## Stability function for numeric solver from butcher tableau

## Butcher tableau from Collocation points, Gauss-Legendre
`colloc(tau_lst)`
Input: list of collocation points,
{ $\tau_1$, $\tau_2$, $\tau_3$...}

Calculates a, b and c of corresponding butcher tableau and displays them.
Note: matricies are often too wide for I/O screen, and are therefore saved to storrage under varibale names `a_col`, `b_col` and `c_col`. They can then be easily displayed on the home screen. 

## TODO: Newton-Euler equations of motion
