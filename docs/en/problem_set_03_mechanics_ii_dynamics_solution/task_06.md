# Task 06 – Motion with linear drag

## Problem Statement

The drag force is given by the formula:

$$
F = -kv
$$

Initial conditions: $v(0)=v_0$, $x(0)=0$.

1. Write down the equation of motion and solve it.
2. Investigate the limit $\lim_{t\to\infty} v(t)$.
3. Compare with motion without drag.

## Theory

When an object moves through a fluid at relatively low speeds, it experiences a resistive drag force that is linearly proportional to its velocity. This is commonly known as Stokes' drag. The negative sign indicates that the force always acts in the opposite direction to the velocity, thereby decelerating the object.

To solve for the velocity and position as functions of time, we set up Newton's Second Law as a first-order separable differential equation in terms of velocity, solve for $v(t)$, and then integrate the result to find position $x(t)$.

## Step-by-Step Solution

### 1. Equation of motion and solution

Applying Newton's Second Law ($\sum F = ma$):

$$
m \frac{dv}{dt} = -kv
$$

This is a separable ordinary differential equation. We separate the variables $v$ and $t$:

$$
\frac{dv}{v} = -\frac{k}{m} dt
$$

Integrate both sides:

$$
\int \frac{1}{v} \, dv = \int -\frac{k}{m} \, dt
$$

$$
\ln|v| = -\frac{k}{m}t + C
$$

Exponentiate both sides to solve for $v$:

$$
v(t) = e^C e^{-\frac{k}{m}t}
$$

Let $A = e^C$. Apply the initial condition $v(0) = v_0$:

$$
\begin{align}
v(0) &= A e^{0} \\
v_0 &= A
\end{align}
$$

So the velocity function is:

$$
v(t) = v_0 e^{-\frac{k}{m}t}
$$

Now, to find the position $x(t)$, we integrate the velocity function with respect to time:

$$
\begin{align}
x(t) &= \int v(t) \, dt \\
     &= \int v_0 e^{-\frac{k}{m}t} \, dt \\
     &= v_0 \left( -\frac{m}{k} \right) e^{-\frac{k}{m}t} + C'
\end{align}
$$

Apply the initial condition $x(0) = 0$ to find the integration constant $C'$:

$$
\begin{align}
0 &= -\frac{mv_0}{k} e^0 + C' \\
C' &= \frac{mv_0}{k}
\end{align}
$$

Substitute $C'$ back into the position equation:

$$
\begin{align}
x(t) &= -\frac{mv_0}{k} e^{-\frac{k}{m}t} + \frac{mv_0}{k} \\
     &= \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right)
\end{align}
$$

### 2. Investigate the limit $\lim_{t\to\infty} v(t)$

Take the limit of the velocity function as time approaches infinity:

$$
\begin{align}
\lim_{t \to \infty} v(t) &= \lim_{t \to \infty} \left( v_0 e^{-\frac{k}{m}t} \right) \\
                         &= v_0 \cdot 0 \\
                         &= 0
\end{align}
$$

Let us also look at the limit of the position $x(t)$ as $t \to \infty$:

$$
\begin{align}
\lim_{t \to \infty} x(t) &= \lim_{t \to \infty} \left( \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right) \right) \\
                         &= \frac{mv_0}{k} (1 - 0) \\
                         &= \frac{mv_0}{k}
\end{align}
$$

### 3. Compare with motion without drag

Without drag, the net horizontal force on the object is zero ($F = 0$). By Newton's First Law, an object in motion will stay in motion with a constant velocity.

- **Velocity without drag:** $v_{nodrag}(t) = v_0$ (Constant)
- **Position without drag:** $x_{nodrag}(t) = v_0 t$ (Grows infinitely)

With linear drag:
- **Velocity with drag:** Decays exponentially toward zero.
- **Position with drag:** Increases, but asymptotically approaches a finite maximum distance $x_{max} = \frac{mv_0}{k}$. It never goes beyond this distance.

## Final Result

- **Equation of Motion:** $m \frac{dv}{dt} = -kv$
- **Velocity:** $v(t) = v_0 e^{-\frac{k}{m}t}$
- **Position:** $x(t) = \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right)$
- **Limit:** $\lim_{t \to \infty} v(t) = 0$. The object eventually stops.
- **Comparison:** Without drag, velocity is constant and distance is infinite. With drag, velocity decays exponentially, and the object travels only a finite stopping distance $\frac{mv_0}{k}$.

## Interpretation

The parameter $\tau = \frac{m}{k}$ has units of time and serves as the "time constant" of the system. It represents the time it takes for the velocity to drop to roughly $37\%$ ($1/e$) of its initial value. The stopping distance $x_{max} = v_0 \tau$ illustrates a fascinating consequence of fluid resistance: no matter how much time passes, an unpowered object experiencing linear drag will never travel infinitely far. It will smoothly bleed off all its kinetic energy into the surrounding fluid as heat, coming to rest at exactly $\frac{mv_0}{k}$.