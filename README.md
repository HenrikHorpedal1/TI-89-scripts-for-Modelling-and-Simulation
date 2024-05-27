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


## Scew-symmetric matrix of a vector

## Lagrangian equtions of motion

## Stability function for numeric solver from butcher tableau

## Butcher tableau from Collocation points, Gauss-Legendre
`colloc(tau_lst)`
Input: list of collocation points,
{ $\tau_1$, $\tau_2$, $\tau_3$...}

Calculates a, b and c of corresponding butcher tableau and displays them.
Note: matricies are often too wide for I/O screen, and are therefore saved to storrage under varibale names `a_col`, `b_col` and `c_col`. They can then be easily displayed on the home screen. 

## TODO: Newton-Euler equations of motion
