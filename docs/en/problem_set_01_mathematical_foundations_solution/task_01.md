# Task 01 – Vectors and linear transformations

## Problem Statement

Given two vectors in three-dimensional space:

$$
\vec a = (2,-1,3), \qquad
\vec b = (1,4,-2)
$$

Calculate the lengths of the vectors, the normalized vector $\hat a$, the dot product, the angle between the vectors, the cross product, and the area of the spanned parallelogram. 

Additionally, for the matrix:

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

Calculate $A\vec a$, $\det A$, and determine if the transformation preserves the orientation of the space.

## Theory

The length (magnitude) of a vector in 3D Euclidean space is given by the Euclidean norm. Normalizing a vector involves dividing it by its magnitude to obtain a unit vector pointing in the same direction. 

The dot product yields a scalar and relates to the cosine of the angle $\theta$ between two vectors:

$$
\vec a \cdot \vec b = |\vec a| |\vec b| \cos\theta
$$

The cross product yields a pseudo-vector orthogonal to both original vectors, and its magnitude equals the area of the parallelogram spanned by them.

For a linear transformation described by a matrix $A$, the determinant $\det A$ indicates how the transformation scales volumes. If $\det A > 0$, the transformation preserves the orientation (handedness) of the space.

## Step-by-Step Solution

First, compute the magnitudes of both vectors.

$$
\begin{align}
|\vec a| &= \sqrt{2^2 + (-1)^2 + 3^2} \\
         &= \sqrt{4 + 1 + 9} \\
         &= \sqrt{14}
\end{align}
$$

$$
\begin{align}
|\vec b| &= \sqrt{1^2 + 4^2 + (-2)^2} \\
         &= \sqrt{1 + 16 + 4} \\
         &= \sqrt{21}
\end{align}
$$

Next, determine the normalized vector $\hat a$.

$$
\hat a = \frac{\vec a}{|\vec a|}
$$

$$
\hat a = \left( \frac{2}{\sqrt{14}}, \frac{-1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)
$$

Compute the dot product by summing the products of corresponding components.

$$
\begin{align}
\vec a \cdot \vec b &= (2)(1) + (-1)(4) + (3)(-2) \\
                    &= 2 - 4 - 6 \\
                    &= -8
\end{align}
$$

Use the dot product to find the angle $\theta$.

$$
\cos\theta = \frac{\vec a \cdot \vec b}{|\vec a| |\vec b|}
$$

$$
\cos\theta = \frac{-8}{\sqrt{14} \sqrt{21}}
$$

$$
\cos\theta = \frac{-8}{\sqrt{294}}
$$

$$
\theta = \arccos \left( \frac{-8}{\sqrt{294}} \right)
$$

Calculate the cross product using the determinant of the standard basis vectors.

$$
\vec a \times \vec b = 
\begin{pmatrix}
\hat i & \hat j & \hat k \\
2 & -1 & 3 \\
1 & 4 & -2
\end{pmatrix}
$$

$$
\vec a \times \vec b = \left( (-1)(-2) - (3)(4), (3)(1) - (2)(-2), (2)(4) - (-1)(1) \right)
$$

$$
\vec a \times \vec b = (2 - 12, 3 + 4, 8 + 1)
$$

$$
\vec a \times \vec b = (-10, 7, 9)
$$

The area of the parallelogram is the magnitude of the cross product.

$$
\text{Area} = |\vec a \times \vec b|
$$

$$
\begin{align}
\text{Area} &= \sqrt{(-10)^2 + 7^2 + 9^2} \\
            &= \sqrt{100 + 49 + 81} \\
            &= \sqrt{230}
\end{align}
$$

Now, evaluate the matrix-vector multiplication $A\vec a$.

$$
A\vec a =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
3
\end{pmatrix}
$$

$$
A\vec a =
\begin{pmatrix}
(2)(2) + (1)(-1) + (0)(3) \\
(0)(2) + (1)(-1) + (-1)(3) \\
(1)(2) + (0)(-1) + (1)(3)
\end{pmatrix}
$$

$$
A\vec a =
\begin{pmatrix}
4 - 1 \\
-1 - 3 \\
2 + 3
\end{pmatrix}
$$

$$
A\vec a =
\begin{pmatrix}
3 \\
-4 \\
5
\end{pmatrix}
$$

Calculate the determinant of matrix $A$ using cofactor expansion along the first row.

$$
\det A = 2( (1)(1) - (-1)(0) ) - 1( (0)(1) - (-1)(1) ) + 0
$$

$$
\det A = 2(1) - 1(1)
$$

$$
\det A = 1
$$

## Final Result

* Magnitudes: $|\vec a| = \sqrt{14}$, $|\vec b| = \sqrt{21}$
* Normalized vector: $\hat a = \left( \frac{2}{\sqrt{14}}, \frac{-1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)$
* Dot product: $\vec a \cdot \vec b = -8$
* Angle: $\theta = \arccos \left( \frac{-8}{\sqrt{294}} \right) \approx 2.05 \text{ rad}$
* Cross product: $\vec a \times \vec b = (-10, 7, 9)$
* Area of parallelogram: $\sqrt{230}$
* Transformed vector: $A\vec a = (3, -4, 5)^T$
* Determinant: $\det A = 1$

## Interpretation

The negative dot product indicates that the angle between the two vectors is obtuse (greater than $\frac{\pi}{2}$). The linear transformation represented by matrix $A$ corresponds to a volume-preserving mapping, as its determinant is exactly $1$. Because the determinant is strictly positive, the transformation maintains the standard right-handed orientation of the coordinate system.