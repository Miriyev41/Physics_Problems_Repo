# Task 08 – Motion in different reference frames

## Problem Statement

Two bodies, A and B, move in the $xy$ plane with constant velocities:

$$
\vec v_A = (v_{Ax}, v_{Ay}), \qquad \vec v_B = (v_{Bx}, v_{By})
$$

Their initial positions at $t=0$ are $\vec r_A(0)$ and $\vec r_B(0)$.

The required operations are:
1. Write the equations of motion $\vec r_A(t)$ and $\vec r_B(t)$ in the laboratory reference frame (origin of the coordinate system).
2. Determine the relative position vector of body B with respect to body A: $\vec r_{B/A}(t) = \vec r_B(t) - \vec r_A(t)$.
3. Determine the relative velocity $\vec v_{B/A}$.
4. Visualize the trajectories from three perspectives:
    - The laboratory reference frame.
    - The reference frame attached to body A.
    - The reference frame attached to body B.

## Theory

The position of a particle moving with constant velocity is given by the linear equation:

$$
\vec r(t) = \vec r(0) + \vec v t
$$

In classical mechanics, specifically Galilean relativity, the position of an object B relative to an observer A is found by vector subtraction. If $\vec r_A$ and $\vec r_B$ are positions relative to a fixed laboratory origin $O$, then:

$$
\vec r_{B/A} = \vec r_B - \vec r_A
$$

The velocity of B relative to A is the time derivative of the relative position:

$$
\vec v_{B/A} = \frac{d}{dt} (\vec r_B - \vec r_A) = \vec v_B - \vec v_A
$$

In the reference frame attached to body A, body A is always at the origin $(0,0)$, and all other objects move with their relative velocities.

## Step-by-Step Solution

### 1. Equations of motion in the Lab Frame

For body A:

$$
x_A(t) = x_A(0) + v_{Ax} t
$$

$$
y_A(t) = y_A(0) + v_{Ay} t
$$

For body B:

$$
x_B(t) = x_B(0) + v_{Bx} t
$$

$$
y_B(t) = y_B(0) + v_{By} t
$$

In vector form:

$$
\vec r_A(t) = \vec r_A(0) + \vec v_A t, \qquad \vec r_B(t) = \vec r_B(0) + \vec v_B t
$$

### 2. Determine relative position $\vec r_{B/A}(t)$

Subtract the position vector of A from the position vector of B:

$$
\begin{align}
\vec r_{B/A}(t) &= \vec r_B(t) - \vec r_A(t) \\
                &= [\vec r_B(0) + \vec v_B t] - [\vec r_A(0) + \vec v_A t] \\
                &= [\vec r_B(0) - \vec r_A(0)] + (\vec v_B - \vec v_A)t
\end{align}
$$

Let $\vec r_{rel, 0} = \vec r_B(0) - \vec r_A(0)$ be the initial relative separation.

### 3. Determine relative velocity $\vec v_{B/A}$

The relative velocity is the coefficient of $t$ in the relative position equation:

$$
\vec v_{B/A} = \vec v_B - \vec v_A
$$

Component-wise:

$$
v_{rel, x} = v_{Bx} - v_{Ax}
$$

$$
v_{rel, y} = v_{By} - v_{Ay}
$$

### 4. Interpretation of Frames

- **Lab Frame:** Both A and B are seen moving along straight lines from their respective starting points.
- **Frame A:** Body A sits at $(0,0)$. Body B moves in a straight line starting from $\vec r_{rel, 0}$ with velocity $\vec v_{B/A}$.
- **Frame B:** Body B sits at $(0,0)$. Body A moves in a straight line starting from $-\vec r_{rel, 0}$ with velocity $\vec v_{A/B} = \vec v_A - \vec v_B$.

## Final Result

* Lab positions: $\vec r_A(t) = \vec r_A(0) + \vec v_A t$, $\vec r_B(t) = \vec r_B(0) + \vec v_B t$
* Relative position (B relative to A): $\vec r_{B/A}(t) = (\vec r_B(0) - \vec r_A(0)) + (\vec v_B - \vec v_A)t$
* Relative velocity: $\vec v_{B/A} = \vec v_B - \vec v_A$

## Interpretation

[Image of relative velocity vector addition diagram]

The principle of Galilean relativity shows that the laws of constant velocity motion are preserved across inertial frames. While the individual trajectories look different depending on who is watching (e.g., body A sees body B moving at a different speed than the lab observer does), the relative velocity remains a constant vector. This is a fundamental concept for understanding collisions, navigation, and the transition from geocentric to heliocentric models of the solar system.