# Task 09 – Change of Reference Frame: Heliocentric to Geocentric

## Problem Statement

Assuming the Copernican model where Earth ($Z$) and Mars ($M$) move in circular orbits around the Sun in the same direction:

The heliocentric positions are given by:

$$
\vec{r}_Z(t) = R_Z \begin{pmatrix} \cos(\omega_Z t) \\ \sin(\omega_Z t) \end{pmatrix}, \qquad \vec{r}_M(t) = R_M \begin{pmatrix} \cos(\omega_M t) \\ \sin(\omega_M t) \end{pmatrix}
$$

1. Describe the motions in the heliocentric system.
2. Determine the position of Mars relative to Earth (geocentric system):
   $$\vec{r}_{M/Z}(t) = \vec{r}_M(t) - \vec{r}_Z(t)$$
   * Explicitly write the components $x_{M/Z}(t)$ and $y_{M/Z}(t)$.
3. Interpret the resulting trajectory (retrograde motion).

## Theory

The **Heliocentric model** (Copernican) places the Sun at the origin, with planets orbiting in circles or ellipses. The **Geocentric description** (Ptolemaic view) observes planetary motion from the perspective of a moving Earth.

To transform from the heliocentric frame to the geocentric frame, we use a translation of the coordinate system:

$$
\vec{r}_{target/observer} = \vec{r}_{target} - \vec{r}_{observer}
$$

This transformation explains why Mars appears to move "backward" in the sky (retrograde motion) when Earth overtakes it in orbit.



## Step-by-Step Solution

### 1. Heliocentric Motion

In the Sun-centered system, both planets undergo uniform circular motion:
* **Earth**: Orbiting at radius $R_Z$ with angular velocity $\omega_Z$.
* **Mars**: Orbiting at radius $R_M$ with angular velocity $\omega_M$.

Since $R_M > R_Z$, Kepler's Third Law implies $\omega_M < \omega_Z$ (Mars moves slower than Earth).

### 2. Geocentric Position Components

The relative position vector is:

$$
\vec{r}_{M/Z}(t) = \begin{pmatrix} R_M \cos(\omega_M t) \\ R_M \sin(\omega_M t) \end{pmatrix} - \begin{pmatrix} R_Z \cos(\omega_Z t) \\ R_Z \sin(\omega_Z t) \end{pmatrix}
$$

The individual components are:

$$
x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)
$$

$$
y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)
$$

### 3. Interpretation of the Trajectory

The resulting path in the $x_{M/Z}y_{M/Z}$ plane is an **epicycloid-like curve**. Because $\omega_Z \neq \omega_M$, the distance between the planets changes periodically. 

When Earth "passes" Mars on the inside track:
1.  The subtraction of the two velocity vectors results in a relative velocity that points in the opposite direction of the orbital motion.
2.  From Earth's perspective, Mars appears to slow down, stop, and move backward against the fixed stars.
3.  This creates the characteristic "loop" known as **retrograde motion**.

## Final Result

* **Geocentric Vector**: $\vec{r}_{M/Z}(t) = (R_M \cos\omega_M t - R_Z \cos\omega_Z t, R_M \sin\omega_M t - R_Z \sin\omega_Z t)$
* **Path Type**: Epitrochoid/Hypotrochoid (depending on constants), resulting in loops.

## Interpretation

The complexity of planetary paths in a geocentric system (epicycles) is a mathematical consequence of observing motion from a non-inertial, moving platform (Earth). The heliocentric model simplifies this by choosing a more stationary reference frame, where the equations of motion become simple circles.