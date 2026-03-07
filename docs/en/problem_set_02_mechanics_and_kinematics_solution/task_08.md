# Task 08 – Relative Motion

## Problem Statement

Two bodies move in a two-dimensional plane. Body A moves with velocity $\vec{v}_A = (3, 1)$, and body B moves with velocity $\vec{v}_B = (1, -2)$.

1. Determine the relative velocity $\vec{v}_{A/B}$ (velocity of A as seen by B).
2. Determine the direction of the relative motion.
3. Describe the visualization of the motion in:
    - The laboratory reference frame (fixed origin).
    - The reference frame attached to body A.
    - The reference frame attached to body B.

## Theory

Relative velocity is the velocity of an object as observed from a particular reference frame. If two objects $A$ and $B$ have velocities $\vec{v}_A$ and $\vec{v}_B$ relative to a common stationary origin (the laboratory frame), the velocity of $A$ relative to $B$ is given by the vector difference:

$$
\vec{v}_{A/B} = \vec{v}_A - \vec{v}_B
$$

Similarly, the velocity of $B$ relative to $A$ is:

$$
\vec{v}_{B/A} = \vec{v}_B - \vec{v}_A = -\vec{v}_{A/B}
$$

The direction of the relative motion is the angle $\theta$ that the relative velocity vector makes with the positive x-axis.



## Step-by-Step Solution

### 1. Calculation of Relative Velocity

Given:
$\vec{v}_A = \begin{pmatrix} 3 \\ 1 \end{pmatrix}$
$\vec{v}_B = \begin{pmatrix} 1 \\ -2 \end{pmatrix}$

The relative velocity $\vec{v}_{A/B}$ is:

$$
\vec{v}_{A/B} = \vec{v}_A - \vec{v}_B = \begin{pmatrix} 3 \\ 1 \end{pmatrix} - \begin{pmatrix} 1 \\ -2 \end{pmatrix}
$$

$$
\vec{v}_{A/B} = \begin{pmatrix} 3 - 1 \\ 1 - (-2) \end{pmatrix} = \begin{pmatrix} 2 \\ 3 \end{pmatrix}
$$

### 2. Direction of Relative Motion

The direction $\theta$ is found using the arctangent of the vector components:

$$
\theta = \arctan\left( \frac{v_{y, A/B}}{v_{x, A/B}} \right) = \arctan\left( \frac{3}{2} \right)
$$

$$
\theta \approx 56.31^\circ
$$

The motion of A as seen by B is directed toward the first quadrant.

### 3. Comparison of Reference Frames

* **Laboratory Frame**: Both bodies are seen moving from the origin. A moves "right and slightly up," while B moves "right and down."
* **Frame of Body A**: In this frame, A is stationary at the origin. Body B appears to move with velocity $\vec{v}_{B/A} = (-2, -3)$, which is "left and down."
* **Frame of Body B**: In this frame, B is stationary at the origin. Body A appears to move with velocity $\vec{v}_{A/B} = (2, 3)$, which is "right and up."

## Final Result

* **Relative Velocity $\vec{v}_{A/B}$**: $(2, 3)$
* **Relative Velocity $\vec{v}_{B/A}$**: $(-2, -3)$
* **Direction of $\vec{v}_{A/B}$**: $56.31^\circ$ relative to the x-axis.

## Interpretation

Relative motion allows us to simplify complex systems by "fixing" one object at the origin. While both bodies are moving relative to the ground, an observer on body B would perceive themselves as stationary while body A recedes away at a speed of $|\vec{v}_{A/B}| = \sqrt{2^2 + 3^2} = \sqrt{13} \approx 3.61$.