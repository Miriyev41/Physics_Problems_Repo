# Task 09 – Change of reference frame (Copernican model → geocentric description)

## Problem Statement

Earth (Z) and Mars (M) move in circular orbits around the Sun (S) in the same direction. The heliocentric positions are given by:

$$
\vec r_Z(t) = R_Z \bigl( \cos(\omega_Z t), \sin(\omega_Z t) \bigr)
$$

$$
\vec r_M(t) = R_M \bigl( \cos(\omega_M t), \sin(\omega_M t) \bigr)
$$

The required operations are:
1. Draw both motions in the heliocentric system (Sun at the center).
2. Determine the position of Mars relative to Earth (geocentric system): $\vec r_{M/Z}(t) = \vec r_M(t) - \vec r_Z(t)$.
3. Explicitly write down the components $x_{M/Z}(t)$ and $y_{M/Z}(t)$.
4. Create an interactive animation with two panels showing heliocentric vs. geocentric motion.

## Theory

The **Heliocentric model** (Copernican) places the Sun at the origin of the coordinate system. In this frame, planets move in nearly circular paths (approximated here as perfect circles).

The **Geocentric description** shifts the origin to the Earth. This is a non-inertial reference frame. To find the position of a celestial body (Mars) as seen from Earth, we use the vector subtraction of their heliocentric positions:

$$
\vec r_{M/Z} = \vec r_M - \vec r_Z
$$

Because Earth moves faster than Mars ($\omega_Z > \omega_M$), Earth periodically "overtakes" Mars. From the perspective of an observer on Earth, Mars appears to slow down, stop, and move backward against the background of fixed stars. This phenomenon is known as **retrograde motion**.

## Step-by-Step Solution

### 1. Heliocentric positions

The positions of Earth and Mars relative to the Sun are:

$$
\vec r_Z(t) = 
\begin{pmatrix}
R_Z \cos(\omega_Z t) \\
R_Z \sin(\omega_Z t)
\end{pmatrix}, \qquad
\vec r_M(t) = 
\begin{pmatrix}
R_M \cos(\omega_M t) \\
R_M \sin(\omega_M t)
\end{pmatrix}
$$

### 2. Determine the relative position $\vec r_{M/Z}(t)$

Subtract the Earth's position vector from Mars's position vector:

$$
\begin{align}
\vec r_{M/Z}(t) &= \vec r_M(t) - \vec r_Z(t) \\
                &= \begin{pmatrix} R_M \cos(\omega_M t) \\ R_M \sin(\omega_M t) \end{pmatrix} - \begin{pmatrix} R_Z \cos(\omega_Z t) \\ R_Z \sin(\omega_Z t) \end{pmatrix}
\end{align}
$$

### 3. Explicit components $x_{M/Z}(t)$ and $y_{M/Z}(t)$

By performing the subtraction component-wise, we obtain the coordinates of Mars in the geocentric frame:

First component ($x$):

$$
x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)
$$

Second component ($y$):

$$
y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)
$$

## Final Result

* Heliocentric positions are simple circles of radii $R_Z$ and $R_M$.
* Geocentric position: $\vec r_{M/Z}(t) = \bigl( R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t), R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t) \bigr)$.
* The resulting path in the geocentric frame exhibits loops (epicycles) caused by the relative difference in orbital speeds.

## Interpretation

[Image of retrograde motion of Mars from Earth's perspective]

In the heliocentric system, the motion is geometrically simple: two concentric circles. However, when we transform this to the geocentric system, the trajectory of Mars becomes complex. Because $R_M > R_Z$ and $\omega_Z > \omega_M$, Earth completes its orbit faster than Mars. When Earth passes between the Sun and Mars (opposition), Mars appears to move in the opposite direction relative to the stars. This "looping" trajectory was the primary observation that ancient astronomers tried to explain using complex systems of epicycles and deferents in the Ptolemaic model, whereas the Copernican model explains it naturally as a simple change of reference frame.