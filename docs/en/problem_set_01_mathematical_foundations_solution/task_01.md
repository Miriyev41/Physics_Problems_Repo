# Task 01 – Vectors and linear transformations

## Problem Statement

Given two vectors in three-dimensional space:

$$
\vec a = (2,-1,3), \qquad \vec b = (1,4,-2)
$$

The required operations are:
1. Calculate the lengths $|\vec a|$ and $|\vec b|$.
2. Determine the normalized vector $\hat a = \frac{\vec a}{|\vec a|}$.
3. Calculate the dot product $\vec a \cdot \vec b$ and the angle between the vectors.
4. Calculate the cross product $\vec a \times \vec b$ and the area of the spanned parallelogram.

For the given matrix:

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

The required operations are:
1. Calculate the matrix-vector product $A\vec a$.
2. Calculate the determinant $\det A$.
3. Check if the transformation preserves the orientation of the space.

## Theory

The length (magnitude) of a vector in $\mathbb{R}^3$ is derived from the Pythagorean theorem. For a vector $\vec v = (v_1, v_2, v_3)$, the length is:

$$
|\vec v| = \sqrt{v_1^2 + v_2^2 + v_3^2}
$$

A normalized vector (unit vector) $\hat v$ has a magnitude of 1 and points in the same direction as the original vector. It is found by dividing each component by the vector's length.

The dot product $\vec a \cdot \vec b$ is a scalar quantity defined as the sum of the products of corresponding components. Geometrically, it relates to the angle $\theta$ between the vectors:

$$
\vec a \cdot \vec b = |\vec a| |\vec b| \cos \theta
$$

The cross product $\vec a \times \vec b$ results in a third vector that is perpendicular to the plane containing $\vec a$ and $\vec b$. Its magnitude equals the area of the parallelogram formed by the two vectors.

Matrix-vector multiplication $A\vec v$ represents a linear transformation where the vector is mapped to a new position in space. The determinant $\det A$ represents the volume scaling factor of this transformation. If $\det A > 0$, the transformation preserves the "handedness" (orientation) of the coordinate system.

## Step-by-Step Solution

### 1. Lengths of the vectors $|\vec a|$ and $|\vec b|$

For vector $\vec a = (2, -1, 3)$:

$$
\begin{align}
|\vec a| &= \sqrt{2^2 + (-1)^2 + 3^2} \\
         &= \sqrt{4 + 1 + 9} \\
         &= \sqrt{14}
\end{align}
$$

For vector $\vec b = (1, 4, -2)$:

$$
\begin{align}
|\vec b| &= \sqrt{1^2 + 4^2 + (-2)^2} \\
         &= \sqrt{1 + 16 + 4} \\
         &= \sqrt{21}
\end{align}
$$

### 2. Normalized vector $\hat a$

We divide the vector $\vec a$ by its length $|\vec a| = \sqrt{14}$:

$$
\begin{align}
\hat a &= \frac{1}{\sqrt{14}}(2, -1, 3) \\
       &= \left( \frac{2}{\sqrt{14}}, -\frac{1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)
\end{align}
$$

### 3. Dot product and the angle $\theta$

**Step 1: Compute the dot product**

$$
\begin{align}
\vec a \cdot \vec b &= (2 \cdot 1) + (-1 \cdot 4) + (3 \cdot -2) \\
                    &= 2 - 4 - 6 \\
                    &= -8
\end{align}
$$

**Step 2: Calculate the angle**

Using the formula $\cos \theta = \frac{\vec a \cdot \vec b}{|\vec a| |\vec b|}$:

$$
\begin{align}
\cos \theta &= \frac{-8}{\sqrt{14} \cdot \sqrt{21}} \\
            &= \frac{-8}{\sqrt{294}} \\
            &= \frac{-8}{7\sqrt{6}}
\end{align}
$$

The angle is:

$$
\theta = \arccos\left( \frac{-8}{7\sqrt{6}} \right) \approx 117.8^\circ
$$

### 4. Cross product and parallelogram area

**Step 1: Compute the cross product**

$$
\begin{align}
\vec a \times \vec b &=
\begin{pmatrix}
a_y b_z - a_z b_y \\
a_z b_x - a_x b_z \\
a_x b_y - a_y b_x
\end{pmatrix} \\
&=
\begin{pmatrix}
(-1)(-2) - (3)(4) \\
(3)(1) - (2)(-2) \\
(2)(4) - (-1)(1)
\end{pmatrix} \\
&=
\begin{pmatrix}
2 - 12 \\
3 + 4 \\
8 + 1
\end{pmatrix} \\
&= (-10, 7, 9)
\end{align}
$$

**Step 2: Calculate the area**

The area is the magnitude of the cross product:

$$
\begin{align}
\text{Area} &= \sqrt{(-10)^2 + 7^2 + 9^2} \\
            &= \sqrt{100 + 49 + 81} \\
            &= \sqrt{230}
\end{align}
$$

### 5. Matrix-vector product $A\vec a$

Multiply each row of $A$ by the column vector $\vec a$:

$$
\begin{align}
A\vec a &=
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
3
\end{pmatrix} \\
&=
\begin{pmatrix}
(2 \cdot 2) + (1 \cdot -1) + (0 \cdot 3) \\
(0 \cdot 2) + (1 \cdot -1) + (-1 \cdot 3) \\
(1 \cdot 2) + (0 \cdot -1) + (1 \cdot 3)
\end{pmatrix} \\
&=
\begin{pmatrix}
4 - 1 + 0 \\
0 - 1 - 3 \\
2 + 0 + 3
\end{pmatrix} \\
&= (3, -4, 5)
\end{align}
$$

### 6. Determinant of $A$

Expand along the first row:

$$
\begin{align}
\det A &= 2 \begin{vmatrix} 1 & -1 \\ 0 & 1 \end{vmatrix} - 1 \begin{vmatrix} 0 & -1 \\ 1 & 1 \end{vmatrix} + 0 \\
       &= 2(1 \cdot 1 - (-1) \cdot 0) - 1(0 \cdot 1 - (-1) \cdot 1) \\
       &= 2(1) - 1(1) \\
       &= 1
\end{align}
$$

### 7. Orientation check

A transformation preserves orientation if $\det A > 0$. Since $\det A = 1$:

**The transformation preserves the orientation of the space.**

## Final Result

* $| \vec a | = \sqrt{14}$, $| \vec b | = \sqrt{21}$
* $\hat a = \left( \frac{2}{\sqrt{14}}, -\frac{1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)$
* $\vec a \cdot \vec b = -8$, $\theta \approx 117.8^\circ$
* $\vec a \times \vec b = (-10, 7, 9)$, Area $= \sqrt{230}$
* $A\vec a = (3, -4, 5)$
* $\det A = 1$ (Orientation preserved)

## Interpretation



The negative dot product confirms that the angle between $\vec a$ and $\vec b$ is obtuse (greater than $90^\circ$). The cross product provides a vector that is the normal to the plane defined by $\vec a$ and $\vec b$. In terms of the linear transformation $A$, a determinant of $1$ indicates that the transformation is "equi-volume"—it changes the shape and position of objects in space but keeps their total volume constant and does not flip the coordinate system (it preserves right-handedness).