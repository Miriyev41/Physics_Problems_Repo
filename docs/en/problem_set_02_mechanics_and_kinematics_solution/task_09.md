# Task 09 – Change of reference frame (Copernican model → geocentric description)

## Problem Statement

Earth and Mars move in circles around the Sun in the same direction.

Assume the model (heliocentric system): 

$$
\vec r_Z(t) = R_Z\,\bigl(\cos(\omega_Z t),\sin(\omega_Z t)\bigr)
$$

$$
\vec r_M(t) = R_M\,\bigl(\cos(\omega_M t),\sin(\omega_M t)\bigr)
$$

1. Draw both motions in the heliocentric system (Sun in the center).
2. Determine the position of Mars relative to Earth (geocentric system):
   $$
   \vec r_{M/Z}(t)=\vec r_M(t)-\vec r_Z(t)
   $$
   Explicitly write down the components $x_{M/Z}(t)$, $y_{M/Z}(t)$.
3. Create an animation with two panels:
   - panel A: heliocentric motion (Earth and Mars on circles),
   - panel B: trajectory of Mars as seen from Earth (trace of $\vec r_{M/Z}(t)$).

## Theory

[Image of retrograde motion of Mars]

The observation of planets from Earth inherently places the observer in a moving reference frame. In the heliocentric (Copernican) model, both Earth and Mars orbit the Sun in roughly circular paths, but at different distances ($R_M > R_Z$) and different angular velocities ($\omega_M < \omega_Z$, per Kepler's Third Law).

To describe the motion of Mars as seen from Earth (the geocentric perspective), we must shift our origin from the Sun to the Earth. The relative position vector $\vec r_{M/Z}(t)$ points from Earth to Mars and is found by vector subtraction. Because Earth moves faster on its inner orbit, it periodically "overtakes" Mars. During this overtaking phase, Mars appears to move backward against the background stars, a phenomenon known as **apparent retrograde motion**.

## Step-by-Step Solution

### 1. Heliocentric model

In the heliocentric reference frame, the Sun is at the origin $(0,0)$. 
The position vector of Earth is:

$$
\vec r_Z(t) = 
\begin{pmatrix}
R_Z \cos(\omega_Z t) \\
R_Z \sin(\omega_Z t)
\end{pmatrix}
$$

The position vector of Mars is:

$$
\vec r_M(t) = 
\begin{pmatrix}
R_M \cos(\omega_M t) \\
R_M \sin(\omega_M t)
\end{pmatrix}
$$

### 2. Relative position (Geocentric model)

To find the position of Mars relative to Earth, we subtract the position vector of Earth from the position vector of Mars:

$$
\begin{align}
\vec r_{M/Z}(t) &= \vec r_M(t) - \vec r_Z(t) \\
                &= 
\begin{pmatrix}
R_M \cos(\omega_M t) \\
R_M \sin(\omega_M t)
\end{pmatrix}
- 
\begin{pmatrix}
R_Z \cos(\omega_Z t) \\
R_Z \sin(\omega_Z t)
\end{pmatrix} \\
                &= 
\begin{pmatrix}
R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t) \\
R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)
\end{pmatrix}
\end{align}
$$

Explicitly writing down the components:

$$
x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)
$$

$$
y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)
$$

## Final Result

- **Heliocentric equations:** $\vec r_Z(t) = (R_Z \cos(\omega_Z t), R_Z \sin(\omega_Z t))$
  $\vec r_M(t) = (R_M \cos(\omega_M t), R_M \sin(\omega_M t))$
- **Geocentric equations (Mars relative to Earth):**
  $x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)$
  $y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)$

## Interpretation

The resulting parametric equations for $x_{M/Z}(t)$ and $y_{M/Z}(t)$ describe an epitrochoid-like curve. When plotted over time, this trace forms looping patterns. Ancient astronomers, holding to a strictly geocentric model of the universe, observed these loops in the night sky and had to invent complex systems of "epicycles" (circles rolling on circles) to explain them mathematically. 

The Copernican heliocentric model elegantly shows that these complex geocentric trajectories are merely an optical illusion—a mathematical artifact of observing a slower outer planet from a faster inner planet. The relative vector mathematics natively generate the epicycles without needing them to physically exist.