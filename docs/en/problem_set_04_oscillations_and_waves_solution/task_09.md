# Task 09 – Chain of $N$ springs (discrete wave model)

## Problem Statement

System: $N$ masses connected by springs.

1. Write down the equations of motion.
2. Solve numerically for $N = 20, 50, 100$.
3. Introduce a local initial disturbance.
4. Observe the propagation of the pulse.
5. Investigate the effect of the values of $k$ and $m$ on the propagation speed.

## Theory

[Image of a chain of masses and springs modeling a discrete wave]

A 1D chain of masses and springs is a fundamental model in solid-state physics for understanding the propagation of sound waves in a crystal lattice (phonons). By taking the continuum limit (where the number of masses $N \to \infty$ and the spacing between them approaches zero), this discrete model smoothly transitions into the continuous 1D wave equation (like a guitar string).

Let $u_i$ represent the longitudinal or transverse displacement of the $i$-th mass from its equilibrium position. Assuming all masses $m$ and spring constants $k$ are identical, the restoring force on the $i$-th mass depends on its relative distance to its immediate left and right neighbors.

## Step-by-Step Solution

### 1. Equations of motion

Consider the $i$-th mass in the interior of the chain. 
- The spring connecting to the $(i+1)$-th mass exerts a force $F_{right} = k(u_{i+1} - u_i)$.
- The spring connecting to the $(i-1)$-th mass exerts a force $F_{left} = -k(u_i - u_{i-1})$.

Applying Newton's Second Law ($m\ddot{u}_i = \sum F$):

$$
m \frac{d^2 u_i}{dt^2} = k(u_{i+1} - u_i) - k(u_i - u_{i-1})
$$

Simplifying this yields a system of coupled differential equations for $i = 1, 2, \dots, N$:

$$
\frac{d^2 u_i}{dt^2} = \frac{k}{m} (u_{i+1} - 2u_i + u_{i-1})
$$

To properly close the system, we apply fixed boundary conditions at the ends of the chain:
$$
u_0(t) = 0 \quad \text{and} \quad u_{N+1}(t) = 0
$$

### 2. Numerical Solution 

For numerical simulation, we discretize time into small steps $\Delta t$ and apply the semi-implicit Euler method for stability in conservative systems. For each mass $i$, the updates per time step are:

$$
a_i = \frac{k}{m} (u_{i+1} - 2u_i + u_{i-1})
$$
$$
v_i(t + \Delta t) = v_i(t) + a_i \Delta t
$$
$$
u_i(t + \Delta t) = u_i(t) + v_i(t + \Delta t) \Delta t
$$

This allows us to scale the system easily to $N = 20, 50,$ or $100$ masses using arrays in JavaScript.

### 3 & 4. Local initial disturbance and pulse propagation

If we introduce a localized initial disturbance—for instance, by pulling the first mass slightly and releasing it, or by giving it a sudden velocity "kick"—the coupling causes this displacement to be sequentially transferred down the chain. 

When observed, this creates a propagating pulse. Because this is a discrete medium, it exhibits **dispersion**: high-frequency components of the pulse travel slightly slower than low-frequency components, causing a sharp pulse to spread out and leave a "wake" of high-frequency ripples as it travels. When the pulse hits the fixed boundary at $N+1$, it reflects and inverts its phase, traveling back in the opposite direction.

### 5. Effect of $k$ and $m$ on propagation speed

In the continuum limit (where the spacing between masses is $a$), the wave equation gives a theoretical propagation speed (phase velocity) of:

$$
v = a \sqrt{\frac{k}{m}}
$$

From this mathematical relationship, we can conclude:
- **Increasing the spring constant $k$:** Makes the inter-atomic bonds "stiffer", which means forces are transmitted more rapidly to adjacent masses. This **increases** the propagation speed.
- **Increasing the mass $m$:** Increases the inertia of each particle, meaning they take longer to accelerate in response to the spring forces. This **decreases** the propagation speed.

## Final Result

- **Equations of Motion:** $\ddot{u}_i = \frac{k}{m} (u_{i+1} - 2u_i + u_{i-1})$
- **Boundary Conditions:** Fixed ends ($u_0 = u_{N+1} = 0$).
- **Pulse Propagation:** A disturbance travels down the chain, demonstrating dispersion and reflecting inverted at the fixed ends.
- **Wave Speed Dependence:** The speed of the pulse is proportional to $\sqrt{k}$ and inversely proportional to $\sqrt{m}$.

## Interpretation

The discrete chain beautifully reveals how macroscopic wave phenomena emerge from microscopic Newtonian mechanics. The "wave" is not a physical object, but rather a coordinated transfer of kinetic and potential energy from one oscillator to the next. The delay inherent in accelerating the mass (inertia) versus the urgency dictated by the spring stiffness perfectly balances to create a finite propagation speed, laying the foundational concepts for the speed of sound in solids.