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
If invec is `[[a][b][c]]`, `skews(invec)` would return:

Note: If some of you vector or matrix elements start with a minus sign you have to use `(-)` istead of `-`.
$$
\begin{pmatrix}
0 & -c & b \\
c & 0 & -a \\
-b & a & 0
\end{pmatrix}
$$



## TODO: Angle Axis Parameterization
`Angl_Ax(angle,vec)`
Returns Transformation matrix.

## TODO: Parallel Axis theorem

## TODO: state space formulation of Lagrange equations of motion.

## Lagrangian equations of motion
after calling `lagfunc()`: 
- You are asked to enter number of generalized coordinates, for instance 2.
- You are asked to enter T. use g1, g2, g1dot, g2dot, g3....etc as you generalized coordinates and their derivative
- You are asked to ender V. same procedure.

- The lagrange equation of motion will be displayed on the I/O screen, but because of limited space the equations will be saved as lagr_lst in memory for better viewing on the home screen.

Note: If your T or V equations start with a minus sign you have to use `(-)` istead of `-` on "the first minus"

## Generalized forces from external forces
After calling `genforce()`:
- You are asked to enter number of generalized coordinates, for instance 2.
- You are asked to enter number of external forces, for instance 2.
- For every force you are asked to enter:
  - Attack point, i.e. the position of the force, often a function of gen. coords. (g1,g2..). X,Y,Z coords must be entered as a matrix, for instance
    `[[g1][l*sin(g2)][4]]`.
  - The force vector, as row vector for instance: `[-Fd,0,0]` where each element corespond in X,Y,Z direction.
- A matrix containing the gen. forces are stored in memory as `genf_mat`, where each row-sum is assoiated with each gen. coord.

Note: If some of you vector or matrix elements start with a minus sign you have to use `(-)` istead of `-` on "the first minus".

Note: Doesnt work for torques, but they are often a generalized force out-of-the-box anyways.

## Stability function for numeric solver from butcher tableau
`stabil(a,b,n)` returns the stability function for a given a-matrix, b-vector and dimension n from a butcher tableau. b has to be a column vector.

## Butcher tableau from Collocation points, Gauss-Legendre
`colloc(tau_lst)`
Input: list of collocation points,
{ $\tau_1$, $\tau_2$, $\tau_3$...}

Calculates a, b and c of corresponding butcher tableau and displays them.
Note: matricies are often too wide for I/O screen, and are therefore saved to storrage under varibale names `a_col`, `b_col` and `c_col`. They can then be easily displayed on the home screen. 

## TODO: Newton-Euler equations of motion
