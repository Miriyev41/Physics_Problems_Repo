# Task 02 – Inclined plane with friction

## Problem Statement

A body of mass $m$ slides down an inclined plane with an angle $\alpha$. The coefficient of kinetic friction between the body and the plane is $\mu$.

The required operations are:
1. Determine all forces acting on the body.
2. Derive the acceleration $\vec a$.
3. Calculate the time of descent $t$ from a height $h$.
4. Determine the final velocity $\vec v$ at the bottom of the plane.
5. Check if the result is consistent with the energy balance.

## Theory

To analyze motion on an inclined plane, we define a coordinate system where the $x$-axis is parallel to the plane (pointing downwards) and the $y$-axis is perpendicular to the plane.

The gravitational force $\vec F_g = mg$ must be decomposed into these components:
- $F_{gx} = mg \sin \alpha$ (driving the motion)
- $F_{gy} = -mg \cos \alpha$ (pressing the body against the plane)

The normal force $\vec N$ acts perpendicular to the surface, and the kinetic friction force $\vec F_f$ acts opposite to the direction of motion. The magnitude of friction is proportional to the normal force:

$$
F_f = \mu N
$$

The work-energy theorem states that the change in mechanical energy is equal to the work done by non-conservative forces (friction):

$$
\Delta E = W_{friction}
$$

## Step-by-Step Solution

### 1. Determine all forces acting on the body

There are three primary forces acting on the mass:
1. **Gravity ($m\vec g$):** Points vertically downward.
2. **Normal Force ($\vec N$):** Points perpendicular to the plane.
3. **Friction Force ($\vec F_f$):** Points up the plane (opposite to motion).



### 2. Derive the acceleration $\vec a$

**Step 1: Analyze the y-direction (equilibrium)**

There is no motion perpendicular to the plane, so the net force in $y$ is zero:

$$
\begin{align}
\sum F_y &= N - mg \cos \alpha = 0 \\
N &= mg \cos \alpha
\end{align}
$$

**Step 2: Analyze the x-direction (motion)**

Using Newton's Second Law for the $x$-axis:

$$
\sum F_x = mg \sin \alpha - F_f = ma
$$

Substitute the friction law $F_f = \mu N$:

$$
\begin{align}
ma &= mg \sin \alpha - \mu (mg \cos \alpha) \\
ma &= mg (\sin \alpha - \mu \cos \alpha)
\end{align}
$$

Divide by $m$ to find the acceleration:

$$
a = g (\sin \alpha - \mu \cos \alpha)
$$

### 3. Calculate the time of descent from height $h$

**Step 1: Find the length of the plane $L$**

Using trigonometry, the relation between height $h$ and the length of the incline $L$ is:

$$
\sin \alpha = \frac{h}{L} \implies L = \frac{h}{\sin \alpha}
$$

**Step 2: Solve for time $t$**

Assuming the body starts from rest ($v_0 = 0$), the kinematic equation for position is:

$$
L = \frac{1}{2} a t^2
$$

Substitute $L$ and $a$:

$$
\frac{h}{\sin \alpha} = \frac{1}{2} \bigl[ g (\sin \alpha - \mu \cos \alpha) \bigr] t^2
$$

Solve for $t$:

$$
t^2 = \frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}
$$

$$
t = \sqrt{\frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}}
$$

### 4. Determine the final velocity $v$

Using the kinematic relation $v^2 = v_0^2 + 2aL$:

$$
\begin{align}
v^2 &= 0 + 2 \bigl[ g (\sin \alpha - \mu \cos \alpha) \bigr] \left( \frac{h}{\sin \alpha} \right) \\
v^2 &= \frac{2gh (\sin \alpha - \mu \cos \alpha)}{\sin \alpha} \\
v^2 &= 2gh \left( 1 - \mu \cot \alpha \right)
\end{align}
$$

The final velocity is:

$$
v = \sqrt{2gh (1 - \mu \cot \alpha)}
$$

### 5. Check consistency with energy balance

**Step 1: Energy at the top ($E_1$)**

$$
E_1 = U + K = mgh + 0 = mgh
$$

**Step 2: Energy at the bottom ($E_2$)**

$$
E_2 = \frac{1}{2} mv^2 = \frac{1}{2} m \bigl[ 2gh (1 - \mu \cot \alpha) \bigr] = mgh (1 - \mu \cot \alpha)
$$

**Step 3: Work done by friction ($W_f$)**

$$
\begin{align}
W_f &= -F_f \cdot L \\
    &= -(\mu mg \cos \alpha) \cdot \left( \frac{h}{\sin \alpha} \right) \\
    &= -\mu mgh \cot \alpha
\end{align}
$$

**Step 4: Verify $\Delta E = W_f$**

$$
\begin{align}
E_2 - E_1 &= mgh (1 - \mu \cot \alpha) - mgh \\
          &= mgh - \mu mgh \cot \alpha - mgh \\
          &= -\mu mgh \cot \alpha
\end{align}
$$

The result matches the work done by friction, so the energy balance is consistent.

## Final Result

* Acceleration: $a = g(\sin \alpha - \mu \cos \alpha)$
* Time of descent: $t = \sqrt{\frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}}$
* Final velocity: $v = \sqrt{2gh (1 - \mu \cot \alpha)}$
* Energy balance verified: $E_{bottom} - E_{top} = W_{friction}$

## Interpretation

The motion only occurs if $\sin \alpha > \mu \cos \alpha$ (or $\tan \alpha > \mu$). If the friction is too high, the acceleration becomes zero or negative, meaning the body remains at rest. The final velocity is always less than the vacuum fall velocity ($v < \sqrt{2gh}$) because some of the initial potential energy is dissipated as heat due to the work done by the friction force.