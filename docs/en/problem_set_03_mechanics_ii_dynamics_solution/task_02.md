# Task 02 – Inclined plane with friction

## Problem Statement

A body of mass $m$ slides down an inclined plane with an angle $\alpha$. The coefficient of kinetic friction is $\mu$. 

1. Determine all forces acting on the body.
2. Derive the acceleration $\vec a$.
3. Calculate the time of descent from height $h$.
4. Determine the final velocity $\vec v$.
5. Check if the result is consistent with the energy balance.

## Theory


The motion of an object on an inclined plane is modeled by establishing a coordinate system tilted along the plane. The $x$-axis aligns parallel to the plane (pointing downwards), and the $y$-axis aligns perpendicular to the plane (pointing outwards).

The work done by non-conservative forces (like kinetic friction) equals the change in the total mechanical energy of the system:

$$
W_{nc} = \Delta E = E_f - E_i
$$

## Step-by-Step Solution

### 1. Forces acting on the body

Three primary forces act on the body during its descent:
1. **Gravity ($\vec F_g$):** Acts strictly downwards toward the center of the Earth. Magnitude $F_g = mg$.
2. **Normal Force ($\vec N$):** Acts strictly perpendicular to the inclined plane, opposing the component of gravity pressing into the surface.
3. **Kinetic Friction ($\vec F_k$):** Acts parallel to the inclined plane, opposing the direction of motion. Magnitude $F_k = \mu N$.

Decomposing gravity into the tilted coordinate system:
- Parallel to the plane: $mg \sin \alpha$
- Perpendicular to the plane: $mg \cos \alpha$

### 2. Derive the acceleration $\vec a$

Applying Newton's Second Law in the perpendicular ($y$) direction:

$$
\begin{align}
\sum F_y &= N - mg \cos \alpha = 0 \\
N &= mg \cos \alpha
\end{align}
$$

Applying Newton's Second Law in the parallel ($x$) direction:

$$
\begin{align}
\sum F_x &= mg \sin \alpha - F_k \\
         &= mg \sin \alpha - \mu N \\
         &= mg \sin \alpha - \mu mg \cos \alpha
\end{align}
$$

Setting this equal to $ma$:

$$
ma = mg (\sin \alpha - \mu \cos \alpha)
$$

Dividing by mass $m$, the acceleration is:

$$
a = g (\sin \alpha - \mu \cos \alpha)
$$

The vector $\vec a$ points down the incline.

### 3. Calculate the time of descent from height $h$

Using geometry, the distance $d$ traveled down the plane from height $h$ is:

$$
d = \frac{h}{\sin \alpha}
$$

Assuming the block starts from rest ($v_0 = 0$), the kinematic equation for displacement is:

$$
d = \frac{1}{2} a t^2
$$

Solving for time $t$:

$$
\begin{align}
t &= \sqrt{\frac{2d}{a}} \\
  &= \sqrt{\frac{2 \left(\frac{h}{\sin \alpha}\right)}{g (\sin \alpha - \mu \cos \alpha)}} \\
  &= \sqrt{\frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}}
\end{align}
$$

### 4. Determine the final velocity $\vec v$

Using the kinematic relationship $v = at$:

$$
\begin{align}
v &= a \sqrt{\frac{2d}{a}} \\
  &= \sqrt{2ad} \\
  &= \sqrt{2 g (\sin \alpha - \mu \cos \alpha) \frac{h}{\sin \alpha}} \\
  &= \sqrt{2gh \left(1 - \mu \cot \alpha \right)}
\end{align}
$$

The vector $\vec v$ points parallel down the incline with this magnitude.

### 5. Check consistency with energy balance

The initial mechanical energy at height $h$ (starting from rest) is purely potential:

$$
E_i = mgh
$$

The final mechanical energy at the bottom ($h=0$) is purely kinetic:

$$
E_f = \frac{1}{2} mv^2
$$

Substitute the derived expression for $v^2$:

$$
\begin{align}
E_f &= \frac{1}{2} m \left[ 2gh \left(1 - \mu \cot \alpha \right) \right] \\
    &= mgh - mgh\mu \cot \alpha
\end{align}
$$

The change in total mechanical energy is:

$$
\begin{align}
\Delta E &= E_f - E_i \\
         &= (mgh - mgh\mu \cot \alpha) - mgh \\
         &= -mgh\mu \cot \alpha
\end{align}
$$

Now calculate the work done by the non-conservative friction force:

$$
\begin{align}
W_{nc} &= \vec F_k \cdot \vec d \\
       &= -(\mu mg \cos \alpha) \left( \frac{h}{\sin \alpha} \right) \\
       &= -\mu mgh \cot \alpha
\end{align}
$$

Since $W_{nc} = \Delta E$, the kinematic derivation is perfectly consistent with the energy balance.

## Final Result

- **Forces:** Gravity, Normal force, Kinetic friction.
- **Acceleration:** $a = g (\sin \alpha - \mu \cos \alpha)$
- **Descent time:** $t = \sqrt{\frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}}$
- **Final speed:** $v = \sqrt{2gh \left(1 - \mu \cot \alpha \right)}$
- **Energy Check:** Confirmed ($W_{nc} = \Delta E$).

## Interpretation

The condition for the block to accelerate downwards is that the bracket term in the acceleration equation must be positive: $\sin \alpha > \mu \cos \alpha$, or equivalently, $\tan \alpha > \mu$. If this condition is not met, static friction will prevent the block from moving in the first place. The energy check demonstrates that a portion of the initial gravitational potential energy is invariably converted into heat by friction during the descent, leaving less available to convert into kinetic energy.