# ISRO

m I_{3 \times 3} & 0 \\
0 & I
\end{bmatrix}
\begin{bmatrix}
\dot{V} \\
\dot{\omega}
\end{bmatrix}
+ \begin{bmatrix}
\omega \times m V \\
\omega \times I \omega
\end{bmatrix}
= \begin{bmatrix}
F \\
\tau
\end{bmatrix} \]
#### Components of the Equation
1. **Mass-Inertia Matrix**:
\[ \begin{bmatrix}
m I_{3 \times 3} & 0 \\
0 & I
\end{bmatrix} \]
- \(m\) is the mass of the quadrotor.
- \(I_{3 \times 3}\) is the 3x3 identity matrix.
- \(I\) is the inertia tensor, a 3x3 matrix describing the rotational inertia of the quadrotor around its center of mass.
2. **State Vector**:
\[ \begin{bmatrix}
\dot{V} \\
\dot{\omega}
\end{bmatrix} \]
- \(\dot{V}\) is the linear acceleration of the quadrotor's center of mass.
- \(\dot{\omega}\) is the angular acceleration of the quadrotor.
3. **Centripetal and Gyroscopic Forces**:
\[ \begin{bmatrix}
\omega \times m V \\
\omega \times I \omega
\end{bmatrix} \]
- \(\omega\) is the angular velocity of the quadrotor.
- \(V\) is the linear velocity of the quadrotor's center of mass.
- \(m V\) is the linear momentum.
- \(I \omega\) is the angular momentum.
- \(\omega \times\) represents the cross product, which introduces the centripetal and gyroscopic effects due to the rotation.
4. **External Forces and Torques**:
\[ \begin{bmatrix}
F \\
\tau
\end{bmatrix} \]
- \(F\) is the total external force acting on the quadrotor.
- \(\tau\) is the total external torque acting on the quadrotor.
### Derivation
#### Translational Dynamics
From Newton's second law for translational motion:
\[ m \dot{V} = F - \omega \times (m V) \]
- \( m \dot{V} \) is the mass times linear acceleration.
- \( F \) is the total external force.
- \( - \omega \times (m V) \) is the fictitious force (Coriolis and centripetal) due to the rotational motion.
#### Rotational Dynamics
From Euler's equations for rotational motion:
\[ I \dot{\omega} + \omega \times (I \omega) = \tau \]
- \( I \dot{\omega} \) is the moment of inertia times angular acceleration.
- \( \omega \times (I \omega) \) is the gyroscopic torque due to angular velocity.
- \( \tau \) is the total external torque.
#### Combining Both Dynamics
We can combine both sets of equations into a single matrix form to describe the coupled translational and rotational dynamics:
1. **Constructing the Mass-Inertia Matrix**:
The mass-inertia matrix combines the mass and inertia tensor into a block diagonal matrix:
\[ \begin{bmatrix}
m I_{3 \times 3} & 0 \\
0 & I
\end{bmatrix} \]
2. **Constructing the State Vector**:
The state vector includes both linear and angular accelerations:
\[ \begin{bmatrix}
\dot{V} \\
\dot{\omega}
\end{bmatrix} \]
3. **Constructing the Coriolis and Gyroscopic Forces**:
The Coriolis and gyroscopic forces due to rotation are combined into another vector:
\[ \begin{bmatrix}
\omega \times m V \\
\omega \times I \omega
\end{bmatrix} \]
4. **Combining Forces and Torques**:
Finally, the external forces and torques are combined:
\[ \begin{bmatrix}
F \\
\tau
\end{bmatrix} \]
Combining these components, we get:
\[ \begin{bmatrix}
m I_{3 \times 3} & 0 \\
0 & I
\end{bmatrix}
\begin{bmatrix}
\dot{V} \\
\dot{\omega}
\end{bmatrix}
+ \begin{bmatrix}
\omega \times m V \\
\omega \times I \omega
\end{bmatrix}
= \begin{bmatrix}
F \\
\tau
\end{bmatrix} \]
This equation succinctly captures the coupled translational and rotational dynamics of the quadrotor in matrix form, making it easier to analyze and control.
