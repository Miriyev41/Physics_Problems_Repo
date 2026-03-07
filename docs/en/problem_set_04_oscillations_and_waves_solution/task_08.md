# Task 08 – Two Coupled Springs (Two Degrees of Freedom)

## Problem Statement

Two masses $m_1, m_2$ are connected to walls in a series configuration by three springs with constants $k_1$, $k_2$, and $k_3$.

1. Write down the equations of motion.
2. Determine the natural frequencies.
3. Find the normal modes.
4. Solve numerically for arbitrary initial conditions.
5. Identify the energy exchange between the masses.

## Theory

A system with two degrees of freedom consists of two independent coordinates required to describe its configuration. When these masses are coupled by a middle spring, the motion of one mass directly affects the other. 

The system can be described by a set of coupled second-order linear differential equations. The "Normal Modes" are specific patterns of motion where all parts of the system oscillate at the same frequency and stay in phase or out of phase with each other.



## Step-by-Step Solution

### 1. Equations of Motion

Let $x_1$ and $x_2$ be the displacements of $m_1$ and $m_2$ from their equilibrium positions. The forces acting on the masses are:
* **Mass 1**: $F_1 = -k_1 x_1 + k_2 (x_2 - x_1)$
* **Mass 2**: $F_2 = -k_3 x_2 - k_2 (x_2 - x_1)$

Applying Newton's Second Law:

$$
m_1 \ddot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 = 0
$$

$$
m_2 \ddot{x}_2 + (k_2 + k_3)x_2 - k_2 x_1 = 0
$$

### 2. Natural Frequencies

We assume solutions of the form $x_1 = A_1 e^{i\omega t}$ and $x_2 = A_2 e^{i\omega t}$. Substituting these into the equations leads to the characteristic equation:

$$
\det \begin{pmatrix} k_1 + k_2 - m_1\omega^2 & -k_2 \\ -k_2 & k_2 + k_3 - m_2\omega^2 \end{pmatrix} = 0
$$

For the symmetric case ($m_1=m_2=m$ and $k_1=k_3=k$):

$$
(k + k_2 - m\omega^2)^2 - k_2^2 = 0
$$

Solving for $\omega$:
* **Mode 1 (Symmetric)**: $\omega_1 = \sqrt{\frac{k}{m}}$
* **Mode 2 (Anti-symmetric)**: $\omega_2 = \sqrt{\frac{k + 2k_2}{m}}$

### 3. Normal Modes

* **Symmetric Mode ($\omega_1$)**: The masses move in the same direction ($x_1 = x_2$). The coupling spring $k_2$ is neither compressed nor stretched.
* **Anti-symmetric Mode ($\omega_2$)**: The masses move in opposite directions ($x_1 = -x_2$). The coupling spring is significantly deformed.

### 4. Energy Exchange

When the system is started with only one mass displaced, the motion is a superposition of both normal modes. This results in **beats**, where energy is periodically transferred from the first mass to the second and back again. The rate of exchange depends on the coupling strength $k_2$.

## Final Result

* **Equations**: Coupled linear second-order ODEs.
* **Frequencies**: $\omega_1 = \sqrt{k/m}$ and $\omega_2 = \sqrt{(k+2k_2)/m}$ (for symmetric systems).
* **Normal Modes**: In-phase and out-of-phase oscillations.

## Interpretation

Coupled oscillators explain how energy propagates through complex structures. The existence of normal modes allows us to decompose any complex vibration into a set of simple, independent harmonic oscillations. This principle is the foundation for understanding phonons in crystals and the behavior of multi-story buildings during earthquakes.