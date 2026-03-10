# Task 06 – Damped oscillator

## Problem Statement

The equation of a damped oscillator is given by:

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0
$$

1. Derive the general solution for each case.
2. Present the classification of cases: underdamped, critically damped, overdamped.
3. Solve the equation numerically (RK4).
4. Investigate the effect of parameter $b$.
5. Generate the graph of $x(t)$.
6. Generate the phase portrait.

## Theory


A damped harmonic oscillator experiences a restoring force proportional to displacement ($-kx$) and a resistive damping force proportional to velocity ($-bv$). This resistive force, often due to fluid friction or air resistance, removes mechanical energy from the system over time.

By dividing the equation of motion by the mass $m$, we can rewrite it in a standard form:

$$
\frac{d^2 x}{dt^2} + 2\gamma \frac{dx}{dt} + \omega_0^2 x = 0
$$

where:
* $\gamma = \frac{b}{2m}$ is the damping coefficient.
* $\omega_0 = \sqrt{\frac{k}{m}}$ is the undamped natural angular frequency.

To solve this linear homogeneous second-order differential equation, we assume a solution of the form $x(t) = e^{rt}$. Substituting this into the equation yields the characteristic quadratic equation:

$$
r^2 + 2\gamma r + \omega_0^2 = 0
$$

The roots of this equation dictate the nature of the solution:

$$
r_{1,2} = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}
$$

The behavior of the system fundamentally changes depending on the sign of the discriminant $\Delta = \gamma^2 - \omega_0^2$, leading to three distinct cases: underdamped, critically damped, and overdamped.

## Step-by-Step Solution

### 1. Classification and general solutions

**Case 1: Underdamped ($\gamma < \omega_0$ or $b < 2\sqrt{mk}$)**

When the damping is weak, the term under the square root is negative, resulting in complex conjugate roots. Let us define the damped angular frequency $\omega_d = \sqrt{\omega_0^2 - \gamma^2}$. The roots are:

$$
r_{1,2} = -\gamma \pm i\omega_d
$$

The general solution is a combination of these complex exponentials, which can be rewritten using Euler's formula as an exponentially decaying sine wave:

$$
x(t) = e^{-\gamma t} \left( A \cos(\omega_d t) + B \sin(\omega_d t) \right)
$$

where $A$ and $B$ are constants determined by initial conditions.

**Case 2: Critically Damped ($\gamma = \omega_0$ or $b = 2\sqrt{mk}$)**

When the damping perfectly balances the restoring force's ability to oscillate, the term under the square root is zero. This results in a single, repeated real root:

$$
r_1 = r_2 = -\gamma
$$

Because the root is repeated, we must multiply the second term by $t$ to form a fundamental set of solutions. The general solution is:

$$
x(t) = (A + B t) e^{-\gamma t}
$$

**Case 3: Overdamped ($\gamma > \omega_0$ or $b > 2\sqrt{mk}$)**

When the damping is strong, the term under the square root is positive, giving two distinct real roots:

$$
r_{1,2} = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}
$$

Both roots are negative real numbers. The general solution is a sum of two decaying exponentials:

$$
x(t) = A e^{r_1 t} + B e^{r_2 t}
$$

### 2. Numerical Solution via RK4

To solve the system numerically using the 4th-order Runge-Kutta (RK4) method, we must reduce the second-order differential equation into a system of two first-order differential equations. 

Let $v = \frac{dx}{dt}$. The system becomes:

$$
\begin{align}
\frac{dx}{dt} &= v \\
\frac{dv}{dt} &= -\frac{b}{m}v - \frac{k}{m}x
\end{align}
$$

Given a state vector $\vec{Y} = \begin{pmatrix} x \\ v \end{pmatrix}$, the derivative function is:

$$
\vec{f}(t, \vec{Y}) = 
\begin{pmatrix}
v \\
-\frac{b}{m}v - \frac{k}{m}x
\end{pmatrix}
$$

The RK4 method iteratively updates the state using a weighted average of four calculated slopes ($k_1, k_2, k_3, k_4$) over a small time step $\Delta t$:

$$
\begin{align}
\vec{k}_1 &= \vec{f}(t, \vec{Y}_n) \\
\vec{k}_2 &= \vec{f}\left(t + \frac{\Delta t}{2}, \vec{Y}_n + \frac{\Delta t}{2}\vec{k}_1\right) \\
\vec{k}_3 &= \vec{f}\left(t + \frac{\Delta t}{2}, \vec{Y}_n + \frac{\Delta t}{2}\vec{k}_2\right) \\
\vec{k}_4 &= \vec{f}(t + \Delta t, \vec{Y}_n + \Delta t \vec{k}_3)
\end{align}
$$

$$
\vec{Y}_{n+1} = \vec{Y}_n + \frac{\Delta t}{6} (\vec{k}_1 + 2\vec{k}_2 + 2\vec{k}_3 + \vec{k}_4)
$$

## Final Result

- **Underdamped ($b < 2\sqrt{mk}$):** Oscillates with decaying amplitude. $x(t) = e^{-\gamma t}(A\cos\omega_d t + B\sin\omega_d t)$.
- **Critically Damped ($b = 2\sqrt{mk}$):** Returns to equilibrium rapidly without oscillation. $x(t) = (A + Bt)e^{-\gamma t}$.
- **Overdamped ($b > 2\sqrt{mk}$):** Returns to equilibrium slowly without oscillation. $x(t) = A e^{r_1 t} + B e^{r_2 t}$.
- **Numerical setup:** System defined as $\dot{x} = v$ and $\dot{v} = -(b/m)v - (k/m)x$.

## Interpretation

The parameter $b$ controls the rate at which energy is dissipated. In the underdamped regime, the system possesses enough energy to pass through the equilibrium point multiple times, creating oscillations whose envelope decays exponentially. In the critically damped regime, the system returns to rest in the shortest possible time without overshooting; this is exactly how car shock absorbers and automatic door closers are tuned. In the overdamped regime, the friction is so immense that it acts like "molasses", actively fighting the spring's attempt to bring the mass back to equilibrium, resulting in a sluggish return. In phase space, underdamped systems show inward spirals, whereas critically damped and overdamped systems show paths that sweep directly into the origin.