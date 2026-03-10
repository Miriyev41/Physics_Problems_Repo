# Task 08 – Relative motion

## Problem Statement

Body A moves with velocity $\vec v_A=(3,1)$, body B with velocity $\vec v_B=(1,-2)$.

1. Determine the relative velocity $\vec v_{A/B}$.
2. Determine the direction of the relative motion.
3. Visualize the motion of both bodies in:
    - the reference frame attached to the origin of the coordinate system,
    - the reference frame attached to body A,
    - the reference frame attached to body B.

## Theory

Relative motion describes the observation of a body's movement from the perspective of another moving body. In classical mechanics (Galilean relativity), velocities add and subtract vectorially. 

The relative velocity of body A with respect to body B, denoted as $\vec v_{A/B}$, is the velocity of A as measured by an observer situated on B. It is calculated by subtracting the velocity vector of the observer (B) from the velocity vector of the object being observed (A):

$$
\vec v_{A/B} = \vec v_A - \vec v_B
$$

The direction of this relative velocity can be found using the arctangent of the ratio of its $y$ and $x$ components. 

When shifting reference frames:
- In the global frame, both bodies move with their respective absolute velocities.
- In the frame of Body A, Body A is stationary at the origin, and Body B moves with velocity $\vec v_{B/A} = -\vec v_{A/B}$.
- In the frame of Body B, Body B is stationary at the origin, and Body A moves with velocity $\vec v_{A/B}$.

## Step-by-Step Solution

### 1. Determine the relative velocity $\vec{v}_{A/B}$

Given the velocity vectors:

$$
\vec{v}_A = \begin{pmatrix} 3 \\ 1 \end{pmatrix}, \quad \vec{v}_B = \begin{pmatrix} 1 \\ -2 \end{pmatrix}
$$



Calculate the vector difference:

$$
\begin{aligned}
\vec{v}_{A/B} &= \vec{v}_A - \vec{v}_B \\
&= \begin{pmatrix} 3 \\ 1 \end{pmatrix} - \begin{pmatrix} 1 \\ -2 \end{pmatrix} \\
&= \begin{pmatrix} 3 - 1 \\ 1 - (-2) \end{pmatrix} \\
&= \begin{pmatrix} 2 \\ 3 \end{pmatrix}
\end{aligned}
$$

So, the relative velocity is $\vec{v}_{A/B} = (2, 3)$.

### 2. Determine the direction of the relative motion

The direction is the angle $\theta$ the vector $\vec v_{A/B}$ makes with the positive $x$-axis. We can calculate this using the tangent function:

$$
\tan \theta = \frac{v_{y, A/B}}{v_{x, A/B}} = \frac{3}{2} = 1.5
$$

Taking the arctangent:

$$
\theta = \arctan(1.5) \approx 56.31^\circ
$$

Since both components of $\vec v_{A/B}$ are positive, the vector points into the first quadrant, so the angle is exactly $56.31^\circ$ above the positive $x$-axis.

### 3. Velocities in different reference frames

**Frame attached to the origin (Global):**
- $\vec v_A = (3, 1)$
- $\vec v_B = (1, -2)$

**Frame attached to Body A:**
- $\vec v_{A/A} = \vec v_A - \vec v_A = (0, 0)$ (A is stationary)
- $\vec v_{B/A} = \vec v_B - \vec v_A = (1-3, -2-1) = (-2, -3)$

**Frame attached to Body B:**
- $\vec v_{A/B} = \vec v_A - \vec v_B = (2, 3)$
- $\vec v_{B/B} = \vec v_B - \vec v_B = (0, 0)$ (B is stationary)

## Final Result

- **Relative velocity of A wrt B:** $\vec v_{A/B} = (2, 3)$
- **Direction:** $\theta = \arctan(1.5) \approx 56.3^\circ$
- **Relative velocity of B wrt A:** $\vec v_{B/A} = (-2, -3)$

## Interpretation

To an observer standing still at the origin, Body A drifts right and slightly up, while Body B drifts right and down. However, if you are sitting on Body B, you do not feel your own motion; instead, it appears as though the entire universe is moving backwards relative to you. Thus, you observe Body A moving away from you toward the top-right corner with a combined speed governed by the vector $(2, 3)$. The symmetry of Galilean relativity ensures that $\vec v_{A/B} = -\vec v_{B/A}$, meaning an observer on A sees B moving away in the exact opposite direction (bottom-left).