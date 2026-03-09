# Task 05 – Power and efficiency

## Problem Statement

A body of mass $m = 10\ \text{kg}$ is pulled up an inclined plane with an angle $\alpha = 30^\circ$ at a constant velocity $v = 2\ \text{m/s}$. The coefficient of kinetic friction is $\mu = 0.2$.

The required operations are:
1. Determine the pulling force $F$ required to maintain constant velocity.
2. Calculate the power $P$ developed by the pulling force.
3. Calculate the rate of energy dissipation due to friction ($P_{friction}$).
4. Determine the efficiency $\eta$ of the process.
5. Analyze how the efficiency changes with the angle $\alpha$.

## Theory

Power $P$ is the rate at which work is done or energy is transferred. For a constant force $\vec F$ acting on an object moving with velocity $\vec v$, the instantaneous power is given by the dot product:

$$
P = \vec F \cdot \vec v
$$

If the force and velocity are parallel, this simplifies to $P = Fv$.

Efficiency $\eta$ is the ratio of useful power output ($P_{out}$) to the total power input ($P_{in}$):

$$
\eta = \frac{P_{out}}{P_{in}}
$$

In this context, the "useful" work is the increase in gravitational potential energy, while the "input" is the work done by the pulling force. The difference between the two is the power dissipated as heat due to friction.

Newton's First Law states that for an object moving at a constant velocity, the net force acting on it must be zero ($\sum \vec F = 0$).

## Step-by-Step Solution

### 1. Determine the pulling force $F$

We define a coordinate system where the $x$-axis points up the incline. Since the velocity is constant, the acceleration is zero ($a = 0$).

**Step 1: Identify forces in the y-direction (perpendicular to the plane)**

$$
\begin{align}
\sum F_y &= N - mg \cos \alpha = 0 \\
N &= mg \cos \alpha
\end{align}
$$

**Step 2: Identify forces in the x-direction (parallel to the plane)**

The forces acting along the incline are the pulling force $F$ (up), the component of gravity $mg \sin \alpha$ (down), and the friction force $F_f = \mu N$ (down).

$$
\begin{align}
\sum F_x &= F - mg \sin \alpha - F_f = 0 \\
F &= mg \sin \alpha + \mu (mg \cos \alpha) \\
F &= mg (\sin \alpha + \mu \cos \alpha)
\end{align}
$$

**Step 3: Calculate the numerical value**
Using $g \approx 9.81\ \text{m/s}^2$:

$$
\begin{align}
F &= 10 \cdot 9.81 \cdot (\sin 30^\circ + 0.2 \cdot \cos 30^\circ) \\
  &= 98.1 \cdot (0.5 + 0.2 \cdot 0.866) \\
  &= 98.1 \cdot (0.5 + 0.1732) \\
  &= 98.1 \cdot 0.6732 \\
  &\approx 66.04\ \text{N}
\end{align}
$$

### 2. Calculate the input power $P_{in}$

The power developed by the pulling force $F$ moving at velocity $v$:

$$
\begin{align}
P_{in} &= F \cdot v \\
       &= 66.04 \cdot 2 \\
       &= 132.08\ \text{W}
\end{align}
$$

### 3. Calculate the power dissipated by friction $P_{friction}$

The friction force is $F_f = \mu mg \cos \alpha$:

$$
\begin{align}
F_f &= 0.2 \cdot 10 \cdot 9.81 \cdot \cos 30^\circ \\
    &= 19.62 \cdot 0.866 \\
    &\approx 16.99\ \text{N}
\end{align}
$$

The power dissipated as heat:

$$
\begin{align}
P_{friction} &= F_f \cdot v \\
             &= 16.99 \cdot 2 \\
             &= 33.98\ \text{W}
\end{align}
$$

### 4. Determine the efficiency $\eta$

Useful power ($P_{out}$) is the rate of change of potential energy:

$$
\begin{align}
P_{out} &= \frac{d}{dt}(mgh) = mg \frac{dh}{dt} \\
        &= mg (v \sin \alpha) \\
        &= 10 \cdot 9.81 \cdot (2 \cdot 0.5) \\
        &= 98.1\ \text{W}
\end{align}
$$

Calculate efficiency:

$$
\begin{align}
\eta &= \frac{P_{out}}{P_{in}} \\
     &= \frac{98.1}{132.08} \\
     &\approx 0.7427 \text{ or } 74.3\%
\end{align}
$$

### 5. Efficiency as a function of $\alpha$

Express efficiency using the formulas derived:

$$
\begin{align}
\eta &= \frac{mgv \sin \alpha}{mg(\sin \alpha + \mu \cos \alpha)v} \\
     &= \frac{\sin \alpha}{\sin \alpha + \mu \cos \alpha}
\end{align}
$$

Divide numerator and denominator by $\cos \alpha$:

$$
\eta(\alpha) = \frac{\tan \alpha}{\tan \alpha + \mu}
$$

## Final Result

* Pulling force: $F \approx 66.04\ \text{N}$
* Input Power: $P_{in} \approx 132.08\ \text{W}$
* Dissipated Power: $P_{friction} \approx 33.98\ \text{W}$
* Efficiency: $\eta \approx 74.3\%$
* Efficiency Formula: $\eta = \frac{\tan \alpha}{\tan \alpha + \mu}$

## Interpretation



The efficiency of pulling an object up an incline depends heavily on the steepness. As the angle $\alpha$ increases, the term $\tan \alpha$ grows, causing the efficiency to approach $1$ (100%). This is because at steeper angles, the normal force (and thus friction) decreases while the useful work (lifting against gravity) increases. Conversely, at very shallow angles, most of the input work is wasted overcoming friction rather than gaining height, leading to low efficiency.