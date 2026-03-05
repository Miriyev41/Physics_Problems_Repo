# Task 08 – First-order differential equation

## Problem Statement

A system is governed by the following first-order ordinary differential equation:

$$
\frac{dy}{dt} = -k y
$$

Solve the equation analytically. Outline the conceptual approach for visualizing the solution in an HTML/JS application to study the influence of the parameter $k$ and the initial condition $y(0)$.

## Theory

A first-order ordinary differential equation (ODE) involves an unknown function $y(t)$ and its first derivative. When the derivative is proportional to the function itself, the equation models processes such as radioactive decay, population dynamics, or cooling. 

The standard method for solving equations of the form $\frac{dy}{dt} = f(t)g(y)$ is the separation of variables. This technique involves algebraically rearranging the equation so that all terms containing $y$ are on one side and all terms containing $t$ are on the other, allowing both sides to be integrated independently.



## Step-by-Step Solution

Begin with the given differential equation.

$$
\frac{dy}{dt} = -k y
$$

Assume $y \neq 0$ and divide both sides by $y$, multiplying by the differential $dt$ to separate the variables.

$$
\frac{1}{y} \, dy = -k \, dt
$$

Integrate both sides.

$$
\int \frac{1}{y} \, dy = \int -k \, dt
$$

The indefinite integrals yield a logarithmic function and a linear function, plus an arbitrary constant of integration $C$.

$$
\ln|y| = -kt + C
$$

Apply the exponential function to both sides to solve for $|y|$.

$$
|y| = e^{-kt + C}
$$

Use the properties of exponents to separate the constant term.

$$
|y| = e^C e^{-kt}
$$

Remove the absolute value by introducing a new constant $y_0 = \pm e^C$. Note that the trivial solution $y=0$ is recovered if $y_0 = 0$.

$$
y(t) = y_0 e^{-kt}
$$

To determine the meaning of $y_0$, evaluate the function at $t = 0$.

$$
y(0) = y_0 e^{-k(0)}
$$

$$
y(0) = y_0 (1)
$$

$$
y_0 = y(0)
$$

Substitute the initial condition back into the general solution.

$$
y(t) = y(0) e^{-kt}
$$

### Application Architecture

To visualize this solution using web technologies:

1.  **Interface (HTML/CSS):** Create slider input elements (type="range") for the parameter $k$ (e.g., $k \in [0, 5]$) and the initial condition $y(0)$ (e.g., $y(0) \in [0, 100]$). Add a canvas element for the coordinate system.
2.  **Logic (JavaScript):** Write a function `calculateY(t, y0, k)` that returns `y0 * Math.exp(-k * t)`. 
3.  **Rendering:** Use an event listener on the sliders to trigger a continuous redraw loop. The drawing function should iterate over a range of $t$ values (pixel columns), evaluate $y(t)$, and map the physical coordinates to the canvas pixel grid to draw the exponential curve.

## Final Result

* General solution: 

$$
y(t) = y(0) e^{-kt}
$$

## Interpretation

The solution $y(t)$ describes an exponential decay process. The initial condition $y(0)$ determines the starting amplitude (the $y$-intercept on a graph). The parameter $k$ represents the decay constant. A larger value of $k$ results in a steeper curve, meaning the system decays to zero much faster. If $k=0$, the derivative is zero, and the system remains constant at $y(0)$. The structural simplicity of the formula allows for highly efficient real-time visualization in scripting environments without requiring numerical integration algorithms.