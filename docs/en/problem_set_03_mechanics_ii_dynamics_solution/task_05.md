# Task 05 – Momentum and one-dimensional head-on collision

## Problem Statement

Two bodies with masses $m_1, m_2$ move along a single straight line. The collision is elastic. 

1. Write down the principles of conservation of momentum and energy.
2. Determine the velocities after the collision.
3. Consider the case $m_1 = m_2$.
4. Consider the limit $m_2 \gg m_1$.
5. Interpret the results physically.

## Theory

[Image of elastic collision of two spheres]

An elastic collision is an encounter between two bodies in which the total kinetic energy of the two bodies remains the same. In an ideal, perfectly elastic collision, there is no net conversion of kinetic energy into other forms such as heat, noise, or potential energy.

For an isolated system (no external forces), the total momentum is always conserved regardless of the collision type. Since the motion is restricted to a single straight line (1D), we can drop vector notation and simply use positive and negative signs to indicate direction.

- **Conservation of Momentum:** The total initial momentum equals the total final momentum.
- **Conservation of Kinetic Energy:** The total initial kinetic energy equals the total final kinetic energy.

## Step-by-Step Solution

### 1. Conservation principles

Let $u_1$ and $u_2$ be the initial velocities, and $v_1$ and $v_2$ be the final velocities after the collision.

The conservation of momentum equation is:

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2
$$

The conservation of kinetic energy equation is:

$$
\frac{1}{2}m_1 u_1^2 + \frac{1}{2}m_2 u_2^2 = \frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2
$$

### 2. Determine the velocities after the collision

To solve for $v_1$ and $v_2$, we first rearrange both equations to group the masses together. 

From momentum:

$$
m_1(u_1 - v_1) = m_2(v_2 - u_2)
$$

From kinetic energy (multiplying by 2 to remove the fractions):

$$
m_1(u_1^2 - v_1^2) = m_2(v_2^2 - u_2^2)
$$

Using the difference of squares factorization on the kinetic energy equation:

$$
m_1(u_1 - v_1)(u_1 + v_1) = m_2(v_2 - u_2)(v_2 + u_2)
$$

We can divide the factored energy equation by the rearranged momentum equation (assuming a non-trivial collision where $u_1 \neq v_1$):

$$
\frac{m_1(u_1 - v_1)(u_1 + v_1)}{m_1(u_1 - v_1)} = \frac{m_2(v_2 - u_2)(v_2 + u_2)}{m_2(v_2 - u_2)}
$$

This simplifies dramatically to the relative velocity equation:

$$
u_1 + v_1 = v_2 + u_2
$$

Rearranging this gives:

$$
u_1 - u_2 = -(v_1 - v_2)
$$

This states that the relative velocity of approach equals the relative velocity of separation. Now we can express $v_2$ in terms of $v_1$:

$$
v_2 = u_1 + v_1 - u_2
$$

Substitute this back into the original momentum equation:

$$
\begin{align}
m_1 u_1 + m_2 u_2 &= m_1 v_1 + m_2 (u_1 + v_1 - u_2) \\
m_1 u_1 + m_2 u_2 &= m_1 v_1 + m_2 u_1 + m_2 v_1 - m_2 u_2 \\
m_1 u_1 - m_2 u_1 + 2m_2 u_2 &= (m_1 + m_2) v_1
\end{align}
$$

Solving for $v_1$:

$$
v_1 = \frac{m_1 - m_2}{m_1 + m_2} u_1 + \frac{2m_2}{m_1 + m_2} u_2
$$

By symmetry (swapping subscripts 1 and 2), the final velocity for the second body is:

$$
v_2 = \frac{2m_1}{m_1 + m_2} u_1 + \frac{m_2 - m_1}{m_1 + m_2} u_2
$$

### 3. Case: Equal masses ($m_1 = m_2$)

If the masses are equal, let $m_1 = m_2 = m$. Substitute this into the final velocity equations:

$$
\begin{align}
v_1 &= \frac{m - m}{m + m} u_1 + \frac{2m}{m + m} u_2 \\
    &= 0 + \frac{2m}{2m} u_2 \\
    &= u_2
\end{align}
$$

$$
\begin{align}
v_2 &= \frac{2m}{m + m} u_1 + \frac{m - m}{m + m} u_2 \\
    &= \frac{2m}{2m} u_1 + 0 \\
    &= u_1
\end{align}
$$

When the masses are equal, the bodies exactly exchange their velocities.

### 4. Limit: Massive target ($m_2 \gg m_1$)

Consider the limit where $m_2$ is much larger than $m_1$. We can divide the numerator and denominator of the coefficients by $m_2$:

$$
v_1 = \frac{\frac{m_1}{m_2} - 1}{\frac{m_1}{m_2} + 1} u_1 + \frac{2}{\frac{m_1}{m_2} + 1} u_2
$$

As $m_2 \to \infty$, the fraction $\frac{m_1}{m_2} \to 0$:

$$
\begin{align}
v_1 &\approx \frac{0 - 1}{0 + 1} u_1 + \frac{2}{0 + 1} u_2 \\
v_1 &\approx -u_1 + 2u_2
\end{align}
$$

For $v_2$, dividing by $m_2$ gives:

$$
\begin{align}
v_2 &= \frac{2\frac{m_1}{m_2}}{\frac{m_1}{m_2} + 1} u_1 + \frac{1 - \frac{m_1}{m_2}}{\frac{m_1}{m_2} + 1} u_2 \\
v_2 &\approx \frac{0}{1} u_1 + \frac{1}{1} u_2 \\
v_2 &\approx u_2
\end{align}
$$

## Final Result

- **Conservation laws:** $m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2$ and $\frac{1}{2}m_1 u_1^2 + \frac{1}{2}m_2 u_2^2 = \frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2$.
- **Final velocities:** $v_1 = \frac{m_1 - m_2}{m_1 + m_2} u_1 + \frac{2m_2}{m_1 + m_2} u_2$
  $v_2 = \frac{2m_1}{m_1 + m_2} u_1 + \frac{m_2 - m_1}{m_1 + m_2} u_2$
- **Equal masses:** $v_1 = u_2$ and $v_2 = u_1$.
- **Massive target ($m_2 \gg m_1$):** $v_1 \approx -u_1 + 2u_2$ and $v_2 \approx u_2$.

## Interpretation

The exact exchange of velocities when $m_1 = m_2$ is a well-known phenomenon observable in Newton's Cradle. When a moving ball strikes a stationary identical ball, the first stops completely while the second moves off with the original velocity.

The $m_2 \gg m_1$ limit effectively describes a light object hitting a massive "wall". If the wall is stationary ($u_2 = 0$), the light object simply bounces back with exactly reversed velocity ($v_1 \approx -u_1$), while the massive wall barely moves ($v_2 \approx 0$). If the massive wall is moving toward the object, the object bounces back with significantly increased speed (e.g., a tennis ball hit by a heavy racket).