# Task 06 – Cycloid: trajectory of a point on a rolling circle

## Problem Statement

A circle of radius $R$ rolls without slipping along the $x$-axis. A point on the rim of the circle traces a cycloid: 

$$
x(t)=R(\omega t-\sin(\omega t)),\qquad y(t)=R(1-\cos(\omega t))
$$

1. Determine the velocity vector $\vec v(t)$ and the acceleration $\vec a(t)$.
2. Calculate $|\vec v(t)|$ and indicate the moments when the point temporarily "stops" relative to the ground.
3. Determine the maximum values of $|\vec v|$ and $|\vec a|$.
4. Create an HTML animation:
   - the circle rolling on the axis,
   - the point on the rim,
   - the cycloid trace,
   - optionally, the vectors $\vec v$ and $\vec a$ at a chosen moment.
5. Compare the cycloid with circular motion in a reference frame attached to the circle.

## Theory



A cycloid is the curve traced by a point on the rim of a circular wheel as the wheel rolls along a straight line without slipping. The condition "without slipping" means that the linear distance the center of the circle translates ($x_c = R\omega t$) is exactly equal to the arc length rolled along the circumference.

Kinematically, the motion of the point can be viewed as the superposition (vector sum) of two simpler motions:
1. The uniform linear translation of the wheel's center.
2. The uniform circular motion of the point around the wheel's center.

## Step-by-Step Solution

### 1. Velocity and acceleration vectors

The position vector is given by:

$$
\vec r(t) = \bigl( R(\omega t - \sin(\omega t)), R(1 - \cos(\omega t)) \bigr)
$$

The velocity vector is the time derivative of the position:

$$
\begin{align}
\vec v(t) &= \left( \frac{d}{dt} [R(\omega t - \sin(\omega t))], \frac{d}{dt} [R(1 - \cos(\omega t))] \right) \\
          &= \bigl( R(\omega - \omega\cos(\omega t)), R(\omega\sin(\omega t)) \bigr) \\
          &= \bigl( R\omega(1 - \cos(\omega t)), R\omega\sin(\omega t) \bigr)
\end{align}
$$

The acceleration vector is the time derivative of the velocity:

$$
\begin{align}
\vec a(t) &= \left( \frac{d}{dt} [R\omega(1 - \cos(\omega t))], \frac{d}{dt} [R\omega\sin(\omega t)] \right) \\
          &= \bigl( R\omega(\omega\sin(\omega t)), R\omega(\omega\cos(\omega t)) \bigr) \\
          &= \bigl( R\omega^2\sin(\omega t), R\omega^2\cos(\omega t) \bigr)
\end{align}
$$

### 2. Magnitude of velocity and stopping moments

The magnitude of the velocity vector is:

$$
\begin{align}
|\vec v(t)| &= \sqrt{ (R\omega(1 - \cos(\omega t)))^2 + (R\omega\sin(\omega t))^2 } \\
            &= \sqrt{ R^2\omega^2 (1 - 2\cos(\omega t) + \cos^2(\omega t)) + R^2\omega^2\sin^2(\omega t) } \\
            &= R\omega \sqrt{ 1 - 2\cos(\omega t) + (\cos^2(\omega t) + \sin^2(\omega t)) } \\
            &= R\omega \sqrt{ 2 - 2\cos(\omega t) } \\
            &= R\omega \sqrt{ 2(1 - \cos(\omega t)) }
\end{align}
$$

Using the half-angle trigonometric identity $1 - \cos(\theta) = 2\sin^2\left(\frac{\theta}{2}\right)$, this simplifies to:

$$
\begin{align}
|\vec v(t)| &= R\omega \sqrt{ 4\sin^2\left(\frac{\omega t}{2}\right) } \\
            &= 2R\omega \left| \sin\left(\frac{\omega t}{2}\right) \right|
\end{align}
$$

The point temporarily "stops" relative to the ground when $|\vec v(t)| = 0$. From the expression before the half-angle identity, this occurs when:

$$
\begin{align}
1 - \cos(\omega t) &= 0 \\
\cos(\omega t) &= 1
\end{align}
$$

This happens at $\omega t = 2\pi k$ for any integer $k = 0, 1, 2, \dots$ 
Therefore, the stopping times are:

$$
t = \frac{2\pi k}{\omega}
$$

Physically, these are the exact moments when the tracing point touches the ground.

### 3. Maximum values of $|\vec v|$ and $|\vec a|$

From the velocity magnitude equation $|\vec v(t)| = R\omega \sqrt{ 2(1 - \cos(\omega t)) }$, the maximum value occurs when $\cos(\omega t) = -1$ (which happens at the top of the wheel's trajectory). 

$$
|\vec v|_{max} = R\omega \sqrt{ 2(1 - (-1)) } = R\omega \sqrt{4} = 2R\omega
$$

The magnitude of the acceleration is:

$$
\begin{align}
|\vec a(t)| &= \sqrt{ (R\omega^2\sin(\omega t))^2 + (R\omega^2\cos(\omega t))^2 } \\
            &= \sqrt{ R^2\omega^4 (\sin^2(\omega t) + \cos^2(\omega t)) } \\
            &= R\omega^2
\end{align}
$$

The magnitude of the acceleration is constant, so its maximum value is simply:

$$
|\vec a|_{max} = R\omega^2
$$

### 5. Comparison with circular motion in the circle's reference frame

Let us shift our reference frame to the center of the rolling circle. The position of the center relative to the ground is $\vec r_c(t) = (R\omega t, R)$.

The position of the point *relative to the center* is:

$$
\begin{align}
\vec r'(t) &= \vec r(t) - \vec r_c(t) \\
           &= \bigl( R(\omega t - \sin(\omega t)) - R\omega t, R(1 - \cos(\omega t)) - R \bigr) \\
           &= \bigl( -R\sin(\omega t), -R\cos(\omega t) \bigr)
\end{align}
$$

This equation $\vec r'(t) = (-R\sin(\omega t), -R\cos(\omega t))$ perfectly describes uniform circular motion of radius $R$ and angular velocity $\omega$, starting from the bottom of the circle (at $(0, -R)$ when $t=0$). 

The velocity in this moving frame is $\vec v'(t) = (-R\omega\cos(\omega t), R\omega\sin(\omega t))$, which has a constant magnitude of $R\omega$. 

The acceleration in the moving frame is $\vec a'(t) = (R\omega^2\sin(\omega t), R\omega^2\cos(\omega t))$. Notice that this is identical to the acceleration $\vec a(t)$ in the ground frame. Because the center of the wheel moves with a constant horizontal velocity, the reference frame attached to it is inertial, meaning accelerations are identical in both frames.

## Final Result

- **Velocity:** $\vec v(t) = (R\omega(1 - \cos(\omega t)), R\omega\sin(\omega t))$
- **Acceleration:** $\vec a(t) = (R\omega^2\sin(\omega t), R\omega^2\cos(\omega t))$
- **Speed:** $|\vec v(t)| = 2R\omega \left| \sin\left(\frac{\omega t}{2}\right) \right|$
- **Stopping moments:** $t = \frac{2\pi k}{\omega}$ (for $k = 0, 1, 2, \dots$)
- **Maximum speed:** $|\vec v|_{max} = 2R\omega$
- **Maximum acceleration magnitude:** $|\vec a|_{max} = R\omega^2$ (constant)

## Interpretation

The cycloid reveals fascinating kinematic properties of rolling objects. At the exact moment a point on the tire tread touches the road, its instantaneous velocity relative to the road is strictly zero; it is momentarily stationary, which is why static friction (rather than kinetic friction) grips a rolling tire. Conversely, when that same point reaches the very top of the wheel, it moves forward at exactly twice the speed of the car ($2R\omega$). Despite these wild fluctuations in speed relative to the ground, the internal stresses on the wheel remain uniform, because the acceleration vector's magnitude $R\omega^2$ is constant and always points directly toward the center of the axle.