# Task 08 – Two coupled springs (two degrees of freedom)

## Problem Statement

Two masses connected to walls in a series configuration by springs with constants $k_1$, $k_2$, and $k_3$.

1. Write down the equations of motion.
2. Determine the natural frequencies.
3. Find the normal modes.
4. Solve numerically for arbitrary initial conditions.
5. Identify the energy exchange between the masses.

## Theory


A system of two coupled oscillators possesses two degrees of freedom, described by the displacements of the two masses, $x_1$ and $x_2$, from their equilibrium positions. This system exhibits complex motion that can be decomposed into independent "normal modes". 

In a normal mode, all parts of the system oscillate with the same frequency and fixed phase relations. Any arbitrary motion of the coupled system is simply a linear combination (superposition) of its normal modes. If the system is started in a state that is not a pure normal mode, energy will periodically transfer back and forth between the two masses.

## Step-by-Step Solution

### 1. Equations of motion

Let $x_1$ be the displacement of mass $m_1$ and $x_2$ be the displacement of mass $m_2$. The layout is: Wall $\to k_1 \to m_1 \to k_2 \to m_2 \to k_3 \to$ Wall.

The forces acting on $m_1$ are:
- Restoring force from the left spring: $-k_1 x_1$
- Force from the middle coupling spring: $k_2(x_2 - x_1)$

The forces acting on $m_2$ are:
- Force from the middle coupling spring: $-k_2(x_2 - x_1)$
- Restoring force from the right spring: $-k_3 x_2$

Applying Newton's Second Law to both masses gives the coupled equations of motion:

$$
\begin{align}
m_1 \ddot{x}_1 &= -k_1 x_1 + k_2(x_2 - x_1) = -(k_1 + k_2)x_1 + k_2 x_2 \\
m_2 \ddot{x}_2 &= -k_2(x_2 - x_1) - k_3 x_2 = k_2 x_1 - (k_2 + k_3)x_2
\end{align}
$$

### 2. Determine the natural frequencies

To find the natural frequencies, we look for normal mode solutions where both masses oscillate at the same angular frequency $\omega$:
$$
x_1(t) = A_1 \cos(\omega t) \\
x_2(t) = A_2 \cos(\omega t)
$$

Substituting these into the equations of motion (and noting $\ddot{x} = -\omega^2 x$) yields a system of linear algebraic equations for the amplitudes:

$$
\begin{align}
(-m_1 \omega^2 + k_1 + k_2) A_1 - k_2 A_2 &= 0 \\
-k_2 A_1 + (-m_2 \omega^2 + k_2 + k_3) A_2 &= 0
\end{align}
$$

For non-trivial solutions ($A_1, A_2 \neq 0$), the determinant of the coefficient matrix must be zero:

$$
(-m_1 \omega^2 + k_1 + k_2)(-m_2 \omega^2 + k_2 + k_3) - k_2^2 = 0
$$

To simplify and yield clean physical insight, let us assume identical masses and springs: $m_1 = m_2 = m$ and $k_1 = k_2 = k_3 = k$. The determinant equation becomes:

$$
\begin{align}
(-m \omega^2 + 2k)^2 - k^2 &= 0 \\
-m \omega^2 + 2k &= \pm k
\end{align}
$$

This gives two distinct natural frequencies:

$$
\omega_1 = \sqrt{\frac{k}{m}} \qquad \text{and} \qquad \omega_2 = \sqrt{\frac{3k}{m}}
$$

### 3. Find the normal modes

Using the identical parameter assumption ($m$, $k$), we substitute the frequencies back into the amplitude equations to find the mode shapes.

**Mode 1 (Lower frequency: $\omega_1^2 = k/m$):**
$$
\left( -m \left(\frac{k}{m}\right) + 2k \right) A_1 - k A_2 = 0 \implies k A_1 - k A_2 = 0 \implies A_1 = A_2
$$
In this *symmetric mode*, the masses move in exactly the same direction with the same amplitude. The middle spring $k_2$ is neither stretched nor compressed, so it exerts no force.

**Mode 2 (Higher frequency: $\omega_2^2 = 3k/m$):**
$$
\left( -m \left(\frac{3k}{m}\right) + 2k \right) A_1 - k A_2 = 0 \implies -k A_1 - k A_2 = 0 \implies A_1 = -A_2
$$
In this *antisymmetric mode*, the masses move in exactly opposite directions. The middle spring is stretched and compressed twice as much as the outer springs, providing a stronger restoring force and thus a higher oscillation frequency.

### 4. Solve numerically for arbitrary initial conditions

For arbitrary initial conditions, analytical solutions involve a superposition of both modes. Numerically, the second-order system is reduced to four first-order ODEs:
$$
v_1 = \dot{x}_1, \qquad \dot{v}_1 = \frac{-(k_1 + k_2)x_1 + k_2 x_2}{m_1}
$$
$$
v_2 = \dot{x}_2, \qquad \dot{v}_2 = \frac{k_2 x_1 - (k_2 + k_3)x_2}{m_2}
$$
These can be integrated over time using standard techniques like the 4th-order Runge-Kutta (RK4) method (implemented in the accompanying HTML simulation).

### 5. Identify the energy exchange between the masses

If we excite the system by displacing only mass 1 while holding mass 2 at equilibrium ($x_1(0) \neq 0, x_2(0) = 0$), we excite a mixture of both normal modes. Because the modes have different frequencies ($\omega_1$ and $\omega_2$), they drift in and out of phase.

When the modes are in phase, mass 1 has large amplitude and mass 2 is nearly stationary. Over time, as the phase difference shifts, mass 1 comes to a near stop while mass 2 takes over the oscillation with large amplitude. This phenomenon, known as **beats**, visibly manifests as kinetic and potential energy transferring back and forth between the two sub-systems through the coupling spring $k_2$.

## Final Result

- **Equations of Motion:** $m_1 \ddot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 = 0$
  $m_2 \ddot{x}_2 - k_2 x_1 + (k_2 + k_3)x_2 = 0$
- **Natural Frequencies (for identical $m, k$):** $\omega_1 = \sqrt{k/m}$, $\omega_2 = \sqrt{3k/m}$.
- **Normal Modes:** $A_1 = A_2$ (Symmetric, "sloshing") and $A_1 = -A_2$ (Antisymmetric, "breathing").
- **Energy Exchange:** When a mixed state is excited, energy periodically transfers between the two masses due to beating between the two normal mode frequencies.