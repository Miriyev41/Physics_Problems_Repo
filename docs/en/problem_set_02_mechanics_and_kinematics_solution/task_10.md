# Task 10 – Analysis of Motion from Numerical Data

## Problem Statement

For the measurement data $x(t) = t + \frac{1}{20}t^2$ on the interval $t \in [0, 10]$ with a time step $\Delta t = 1$:

1. Create a table of values for $t$ and $x(t)$.
2. Calculate the average velocity $v_{avg}$ in each time interval.
3. Calculate the instantaneous velocity $v(t)$ using the derivative.
4. Compare the average velocities with the instantaneous velocity at the midpoint of each interval.
5. Determine the acceleration $a(t)$.

## Theory

Numerical analysis of motion involves discretizing continuous functions. 

The **average velocity** over a time interval $[t, t + \Delta t]$ is defined as the displacement divided by the time elapsed:

$$
v_{avg} = \frac{x(t + \Delta t) - x(t)}{\Delta t}
$$

The **instantaneous velocity** is the limit of the average velocity as $\Delta t$ approaches zero, which corresponds to the first derivative:

$$
v(t) = \frac{dx}{dt}
$$

In uniformly accelerated motion, the average velocity over an interval is exactly equal to the instantaneous velocity at the temporal midpoint of that interval.

## Step-by-Step Solution

### 1. Table of Values

Using $x(t) = t + 0.05t^2$:

| $t$ | $x(t)$ |
| :--- | :--- |
| 0 | 0.00 |
| 1 | 1.05 |
| 2 | 2.20 |
| 3 | 3.45 |
| 4 | 4.80 |
| 5 | 6.25 |
| 6 | 7.80 |
| 7 | 9.45 |
| 8 | 11.20 |
| 9 | 13.05 |
| 10 | 15.00 |

### 2. Average Velocities

Calculated for intervals $[t, t+1]$:
* $t \in [0, 1]: v_{avg} = (1.05 - 0)/1 = 1.05$
* $t \in [1, 2]: v_{avg} = (2.20 - 1.05)/1 = 1.15$
* $t \in [2, 3]: v_{avg} = (3.45 - 2.20)/1 = 1.25$
* $t \in [3, 4]: v_{avg} = (4.80 - 3.45)/1 = 1.35$

The pattern shows $v_{avg}$ increases by $0.1$ units per interval.

### 3. Instantaneous Velocity and Acceleration

Differentiating $x(t)$:

$$
v(t) = \frac{d}{dt} \left( t + \frac{1}{20}t^2 \right) = 1 + \frac{1}{10}t = 1 + 0.1t
$$

Differentiating $v(t)$ for acceleration:

$$
a(t) = \frac{dv}{dt} = 0.1
$$

### 4. Comparison

Let's check the interval $t \in [0, 1]$. The midpoint is $t_{mid} = 0.5$.
* $v_{avg} = 1.05$
* $v(0.5) = 1 + 0.1(0.5) = 1.05$

The values match perfectly. This identity holds because the position function is quadratic (acceleration is constant).

## Final Result

* **Instantaneous Velocity**: $v(t) = 1 + 0.1t$
* **Acceleration**: $a = 0.1$
* **Verification**: $v_{avg}$ for $[t_1, t_2]$ is equal to $v\left(\frac{t_1+t_2}{2}\right)$.

## Interpretation

Numerical data often hides the underlying physics until rate-of-change analysis is applied. Here, the discrete steps in average velocity reveal a constant acceleration of $0.1\ \text{m/s}^2$. The fact that average velocity equals the midpoint instantaneous velocity is a unique property of motion where the derivative of velocity (acceleration) is zero or constant.