This is a comprehensive problem set covering the essential mathematical foundations for physics and engineering. Below are the step-by-step solutions and conceptual explanations for each problem.

---

## Problem 1 – Vectors and Linear Transformations

**Vector Calculations:**
Given $\vec a = (2,-1,3)$ and $\vec b = (1,4,-2)$:

* **Lengths:**
* $|\vec a| = \sqrt{2^2 + (-1)^2 + 3^2} = \sqrt{4 + 1 + 9} = \mathbf{\sqrt{14}}$
* $|\vec b| = \sqrt{1^2 + 4^2 + (-2)^2} = \sqrt{1 + 16 + 4} = \mathbf{\sqrt{21}}$


* **Normalized vector $\hat a$:**
* $\hat a = \frac{1}{\sqrt{14}}(2, -1, 3) = \mathbf{(\frac{2}{\sqrt{14}}, -\frac{1}{\sqrt{14}}, \frac{3}{\sqrt{14}})}$


* **Dot Product & Angle:**
* $\vec a \cdot \vec b = (2)(1) + (-1)(4) + (3)(-2) = 2 - 4 - 6 = \mathbf{-8}$
* $\cos \theta = \frac{\vec a \cdot \vec b}{|\vec a||\vec b|} = \frac{-8}{\sqrt{14}\sqrt{21}} \approx -0.466$
* $\theta = \arccos(-0.466) \approx \mathbf{117.8^\circ}$


* **Cross Product & Area:**
* $\vec a \times \vec b = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & -1 & 3 \\ 1 & 4 & -2 \end{vmatrix} = \mathbf{i}(2-12) - \mathbf{j}(-4-3) + \mathbf{k}(8+1) = \mathbf{(-10, 7, 9)}$
* $\text{Area} = |\vec a \times \vec b| = \sqrt{(-10)^2 + 7^2 + 9^2} = \sqrt{100+49+81} = \mathbf{\sqrt{230}}$



**Matrix Calculations:**

* **$A\vec a$:** $\begin{pmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ 1 & 0 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 4-1+0 \\ 0-1-3 \\ 2+0+3 \end{pmatrix} = \mathbf{\begin{pmatrix} 3 \\ -4 \\ 5 \end{pmatrix}}$
* **$\det A$:** $2(1-0) - 1(0 - (-1)) + 0 = 2 - 1 = \mathbf{1}$
* **Orientation:** Since $\det A > 0$, the transformation **preserves** the orientation of the space.

---

## Problem 2 – Parametric Trajectory

Given $\vec r(t) = (t^2, \sin t, 5)$:

* **Velocity:** $\vec v(t) = \frac{d\vec r}{dt} = \mathbf{(2t, \cos t, 0)}$
* **Acceleration:** $\vec a(t) = \frac{d\vec v}{dt} = \mathbf{(2, -\sin t, 0)}$
* **Magnitude $|\vec v(1)|$:** $\vec v(1) = (2, \cos 1, 0) \implies |\vec v(1)| = \sqrt{4 + \cos^2(1)} \approx \mathbf{2.07}$
* **$\vec v \cdot \vec a$:** $(2t)(2) + (\cos t)(-\sin t) + 0 = \mathbf{4t - \sin t \cos t}$
* **$\vec v \times \vec a$:** $\begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2t & \cos t & 0 \\ 2 & -\sin t & 0 \end{vmatrix} = \mathbf{k}(-2t \sin t - 2 \cos t) = \mathbf{(0, 0, -2t \sin t - 2 \cos t)}$

---

## Problem 3 – Integration of Motion

**A) Velocity to Position:**
$\vec r(t) = (0,1,2) + \int_0^t (2\tau, 3, -e^{-\tau}) d\tau = (0,1,2) + [\tau^2, 3\tau, e^{-\tau}]_0^t$
$\vec r(t) = (0,1,2) + (t^2, 3t, e^{-t} - 1) = \mathbf{(t^2, 3t+1, e^{-t}+1)}$
$\vec a(t) = \frac{d\vec v}{dt} = \mathbf{(2, 0, e^{-t})}$

**B) Acceleration to Position:**
$\vec v(t) = (1,0,2) + \int_0^t (4, -\sin \tau, 0) d\tau = (1,0,2) + (4t, \cos t - 1, 0) = \mathbf{(4t+1, \cos t - 1, 2)}$
$\vec r(t) = (0,0,0) + \int_0^t (4\tau+1, \cos \tau - 1, 2) d\tau = \mathbf{(2t^2+t, \sin t - t, 2t)}$

---

## Problem 4 – Geometry of Curves

| Curve | Elimination | Type | $|\vec v|$ Constant? | $|\vec a|$ Constant? |
| :--- | :--- | :--- | :--- | :--- |
| **A** | $x^2 + y^2 = R^2$ | Circle | **Yes** ($R$) | **Yes** ($R$) |
| **B** | $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ | Ellipse | No | No |
| **C** | $y = x^2$ | Parabola | No | **Yes** ($(0, 2)$) |
| **D** | $x^2 - y^2 = 1$ | Hyperbola | No | No |

---

## Problem 5 – Ellipse Curvature

1. $\vec v(t) = (-a \sin t, b \cos t)$, $\vec a(t) = (-a \cos t, -b \sin t)$
2. $\hat T(t) = \frac{(-a \sin t, b \cos t)}{\sqrt{a^2 \sin^2 t + b^2 \cos^2 t}}$
3. **Normal Acceleration at $t=0$:**
At $t=0$, $\vec v = (0, b)$ and $\vec a = (-a, 0)$. Since $\vec v \cdot \vec a = 0$ at this point, the entire acceleration is normal. **$a_n(0) = a$**.
4. **Radius of Curvature:** $R = \frac{v^2}{a_n} = \frac{b^2}{a}$.
5. **Circle:** If $a=b$, $R = \frac{a^2}{a} = a$, which matches the radius of the circle.

**Physical Interpretation:**

* **Yes**, higher curvature ($\frac{1}{R}$) leads to higher $a_n$ for a given speed.
* The ellipse is **more curved at the end of the major axis** (where the radius of curvature is smallest).
* $a_n$ changes the **direction** of the velocity vector without changing its speed.

---

## Problem 6 & 7 – Numerical Integration (Logic)

For Problem 6, the arc length integral is $s = \int_0^1 \sqrt{1 + (2t)^2} dt$.
For Problem 7, the work is $W = \int_0^1 (t^2, 2t) \cdot (1, 2t) dt = \int_0^1 (t^2 + 4t^2) dt = \int_0^1 5t^2 dt = \frac{5}{3}$.

**HTML/JS Implementation Logic:**

```javascript
function trapezoidalRule(f, a, b, n) {
    let h = (b - a) / n;
    let sum = 0.5 * (f(a) + f(b));
    for (let i = 1; i < n; i++) {
        sum += f(a + i * h);
    }
    return sum * h;
}

```

---

## Problem 8 & 9 – Differential Equations

**Problem 8:** $\frac{dy}{dt} = -ky \implies \mathbf{y(t) = y(0)e^{-kt}}$ (Exponential decay).

**Problem 9:** $\frac{d^2 x}{dt^2} + \omega^2 x = 0$.

* General Solution: $\mathbf{x(t) = A \cos(\omega t) + B \sin(\omega t)}$.
* This represents a simple harmonic oscillator (like a mass on a spring).

---

## Problem 10 – Angular Momentum

1. $\vec v(t) = (-R\omega \sin(\omega t), R\omega \cos(\omega t), 0)$
2. $\vec L = m (\vec r \times \vec v) = m \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ R\cos\omega t & R\sin\omega t & 0 \\ -R\omega\sin\omega t & R\omega\cos\omega t & 0 \end{vmatrix} = \mathbf{m(0, 0, R^2\omega \cos^2\omega t + R^2\omega \sin^2\omega t)}$
3. $\vec L = \mathbf{(0, 0, mR^2\omega)}$. The magnitude is constant, and it points along the $z$-axis (perpendicular to the $xy$ plane).
4. **Right-hand rule:** Curl fingers in direction of rotation; thumb points in direction of $\vec L$.

Would you like me to generate the full HTML/JavaScript code for the visualizations mentioned in Problems 6, 8, or 9?