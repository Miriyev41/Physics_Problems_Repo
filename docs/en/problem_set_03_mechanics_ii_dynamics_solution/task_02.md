# Task 02 – Inclined Plane with Friction

## Problem Statement

A body of mass $m$ slides down an inclined plane with an angle $\alpha$. The coefficient of kinetic friction is $\mu$.

* Determine all forces acting on the body.
* Derive the acceleration $\vec{a}$.
* Calculate the time of descent from height $h$.
* Determine the final velocity $\vec{v}$.
* Check if the result is consistent with the energy balance.

## Theory

The motion of an object on an inclined plane is governed by the decomposition of gravitational force into components relative to the plane's surface. According to Newton's Second Law, the net force in any direction is equal to the mass times the acceleration in that direction.

The forces involved are:
1.  **Gravity ($F_g = mg$):** Directed vertically downward.
2.  **Normal Force ($N$):** Exerted by the surface perpendicular to the plane.
3.  **Kinetic Friction ($f_k = \mu N$):** Opposes the direction of motion along the plane.



## Step-by-Step Solution

### 1. Force Decomposition

We establish a coordinate system where the $x$-axis is parallel to the inclined plane (pointing downwards) and the $y$-axis is perpendicular to it.

**Gravity components:**
* $F_{gx} = mg \sin(\alpha)$
* $F_{gy} = mg \cos(\alpha)$

**Equations of Equilibrium and Motion:**
* **Vertical ($y$):** Since there is no motion perpendicular to the plane, $N - mg \cos(\alpha) = 0 \implies N = mg \cos(\alpha)$.
* **Horizontal ($x$):** The net force is the difference between the driving gravitational component and friction.

$$
F_{net} = mg \sin(\alpha) - f_k
$$

### 2. Deriving Acceleration

Substituting $f_k = \mu N = \mu mg \cos(\alpha)$ into the net force equation:

$$
ma = mg \sin(\alpha) - \mu mg \cos(\alpha)
$$

Dividing by $m$:

$$
a = g(\sin(\alpha) - \mu \cos(\alpha))
$$

### 3. Time of Descent

The distance $L$ along the plane corresponding to height $h$ is:

$$
L = \frac{h}{\sin(\alpha)}
$$

Using the kinematic equation for constant acceleration starting from rest ($x = \frac{1}{2}at^2$):

$$
\frac{h}{\sin(\alpha)} = \frac{1}{2} g(\sin(\alpha) - \mu \cos(\alpha)) t^2
$$

$$
t = \sqrt{\frac{2h}{g \sin(\alpha)(\sin(\alpha) - \mu \cos(\alpha))}}
$$

### 4. Final Velocity

Using the relation $v^2 = 2aL$:

$$
v = \sqrt{2 g(\sin(\alpha) - \mu \cos(\alpha)) \frac{h}{\sin(\alpha)}}
$$

$$
v = \sqrt{2gh \left( 1 - \mu \cot(\alpha) \right)}
$$

### 5. Energy Balance Verification

The work-energy theorem states that the change in mechanical energy equals the work done by non-conservative forces (friction).

**Initial Energy:** $E_i = mgh$ (Potential Energy)
**Final Energy:** $E_f = \frac{1}{2}mv^2$ (Kinetic Energy)
**Work of Friction:** $W_f = -f_k \cdot L = -(\mu mg \cos\alpha) \cdot \frac{h}{\sin\alpha} = -\mu mgh \cot\alpha$

**Verification:**

$$
E_f - E_i = W_f
$$

$$
\frac{1}{2}m [2gh(1 - \mu \cot\alpha)] - mgh = -\mu mgh \cot\alpha
$$

$$
mgh - \mu mgh \cot\alpha - mgh = -\mu mgh \cot\alpha
$$

The energy balance is consistent.

## Final Result

* **Acceleration**: $a = g(\sin\alpha - \mu \cos\alpha)$
* **Final Velocity**: $v = \sqrt{2gh(1 - \mu \cot\alpha)}$
* **Time of Descent**: $t = \sqrt{\frac{2h}{g(\sin^2\alpha - \mu \sin\alpha \cos\alpha)}}$

## Interpretation

Motion only occurs if $\tan(\alpha) > \mu$; otherwise, the static friction would prevent the body from sliding. The final velocity is always less than $\sqrt{2gh}$ (the speed of a free-falling body) because a portion of the initial potential energy is dissipated as heat due to the work of friction.