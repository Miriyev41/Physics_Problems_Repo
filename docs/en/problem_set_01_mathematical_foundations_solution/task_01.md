# Task 01 – Vectors and Linear Transformations

## Problem Statement

Given two vectors in three-dimensional space:

$$
\vec a = (2,-1,3), \qquad \vec b = (1,4,-2)
$$

Calculate the following:
1. The lengths of the vectors $|\vec a|$ and $|\vec b|$.
2. The normalized vector $\hat a = \frac{\vec a}{|\vec a|}$.
3. The dot product $\vec a \cdot \vec b$ and the angle between the vectors.
4. The cross product $\vec a \times \vec b$ and the area of the parallelogram spanned by these vectors.

For the given matrix:

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

Calculate the following:
1. The matrix-vector product $A\vec a$.
2. The determinant $\det A$.
3. Check if the transformation preserves the orientation of the space.

## Theory

A vector in three-dimensional Cartesian space is represented by its components. The magnitude (length) of a vector is calculated using the Euclidean norm. Normalizing a vector means scaling it so that its magnitude becomes exactly $1$, while preserving its direction.

The dot product of two vectors yields a scalar and is geometrically related to the cosine of the angle between them. 

The cross product of two vectors yields a new vector that is orthogonal to both original vectors. The magnitude of this cross product is equal to the area of the parallelogram spanned by the two vectors.

A matrix represents a linear transformation. Multiplying a matrix by a vector applies this transformation to the vector. The determinant of the transformation matrix describes how volumes scale under the transformation. If the determinant is positive, the transformation preserves the orientation of the space (e.g., a right-handed coordinate system remains right-handed). If it is negative, the orientation is reversed.

## Step-by-Step Solution

### 1. Lengths of the vectors

The length of vector $\vec a$ is given by:

$$
|\vec a| = \sqrt{a_x^2 + a_y^2 + a_z^2}
$$

Substituting the components of $\vec a$:

$$
\begin{align}
|\vec a| &= \sqrt{2^2 + (-1)^2 + 3^2} \\
         &= \sqrt{4 + 1 + 9} \\
         &= \sqrt{14}
\end{align}
$$

Similarly, for vector $\vec b$:

$$
\begin{align}
|\vec b| &= \sqrt{1^2 + 4^2 + (-2)^2} \\
         &= \sqrt{1 + 16 + 4} \\
         &= \sqrt{21}
\end{align}
$$

### 2. Normalized vector $\hat a$

The normalized vector is obtained by dividing each component of $\vec a$ by its length:

$$
\hat a = \frac{1}{|\vec a|} \vec a
$$

Substituting the known values:

$$
\hat a = \frac{1}{\sqrt{14}} (2, -1, 3)
$$

This can also be written as:

$$
\hat a = \left( \frac{2}{\sqrt{14}}, -\frac{1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)
$$

### 3. Dot product and angle

The algebraic definition of the dot product is:

$$
\vec a \cdot \vec b = a_x b_x + a_y b_y + a_z b_z
$$

Calculating the sum of the products of the components:

$$
\begin{align}
\vec a \cdot \vec b &= (2)(1) + (-1)(4) + (3)(-2) \\
                    &= 2 - 4 - 6 \\
                    &= -8
\end{align}
$$

The geometric definition of the dot product is:

$$
\vec a \cdot \vec b = |\vec a| |\vec b| \cos \theta
$$

Solving for the angle $\theta$:

$$
\cos \theta = \frac{\vec a \cdot \vec b}{|\vec a| |\vec b|}
$$

Substituting the previously calculated values:

$$
\cos \theta = \frac{-8}{\sqrt{14} \sqrt{21}}
$$

Simplifying the denominator:

$$
\cos \theta = \frac{-8}{\sqrt{294}}
$$

Taking the inverse cosine yields the angle:

$$
\theta = \arccos \left( \frac{-8}{\sqrt{294}} \right)
$$

### 4. Cross product and parallelogram area

The cross product $\vec a \times \vec b$ is evaluated using the determinant of the standard basis vectors:

$$
\vec a \times \vec b = 
\begin{pmatrix}
a_y b_z - a_z b_y \\
a_z b_x - a_x b_z \\
a_x b_y - a_y b_x
\end{pmatrix}
$$

Substituting the components:

$$
\begin{align}
\vec a \times \vec b &= 
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
&= 
\begin{pmatrix}
-10 \\
7 \\
9
\end{pmatrix}
\end{align}
$$

The vector result can be written as $(-10, 7, 9)$.

The area of the parallelogram is the magnitude of the cross product:

$$
S = |\vec a \times \vec b|
$$

Calculating the magnitude:

$$
\begin{align}
S &= \sqrt{(-10)^2 + 7^2 + 9^2} \\
  &= \sqrt{100 + 49 + 81} \\
  &= \sqrt{230}
\end{align}
$$

### 5. Matrix-vector product $A\vec a$

To multiply the matrix $A$ by the vector $\vec a$, the vector is treated as a column vector:

$$
A \vec a =
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

Performing the row-by-column multiplication:

$$
\begin{align}
A \vec a &=
\begin{pmatrix}
(2)(2) + (1)(-1) + (0)(3) \\
(0)(2) + (1)(-1) + (-1)(3) \\
(1)(2) + (0)(-1) + (1)(3)
\end{pmatrix} \\
&=
\begin{pmatrix}
4 - 1 + 0 \\
0 - 1 - 3 \\
2 + 0 + 3
\end{pmatrix} \\
&=
\begin{pmatrix}
3 \\
-4 \\
5
\end{pmatrix}
\end{align}
$$

### 6. Determinant of matrix A

The determinant of a $3 \times 3$ matrix is calculated using cofactor expansion along the first row:

$$
\det A = 2 \det \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} - 1 \det \begin{pmatrix} 0 & -1 \\ 1 & 1 \end{pmatrix} + 0 \det \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:

$$
\begin{align}
\det A &= 2( (1)(1) - (-1)(0) ) - 1( (0)(1) - (-1)(1) ) + 0 \\
       &= 2(1 - 0) - 1(0 + 1) \\
       &= 2 - 1 \\
       &= 1
\end{align}
$$

### 7. Orientation preservation

The orientation of space under a linear transformation is determined by the sign of the determinant.

Since $\det A = 1$, which is strictly greater than zero, the transformation preserves orientation.

## Final Result

- Lengths: $|\vec a| = \sqrt{14}$, $|\vec b| = \sqrt{21}$
- Normalized vector: $\hat a = \left( \frac{2}{\sqrt{14}}, -\frac{1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)$
- Dot product: $\vec a \cdot \vec b = -8$
- Angle: $\theta = \arccos \left( \frac{-8}{\sqrt{294}} \right)$
- Cross product: $\vec a \times \vec b = (-10, 7, 9)$
- Parallelogram area: $\sqrt{230}$
- Transformed vector: $A\vec a = (3, -4, 5)^T$
- Determinant: $\det A = 1$
- The transformation preserves orientation.

## Interpretation

The negative dot product indicates that the angle between vectors $\vec a$ and $\vec b$ is obtuse (greater than $90^\circ$). The cross product provides a normal vector perpendicular to the plane defined by $\vec a$ and $\vec b$. 

The transformation matrix $A$ acts on the space such that volumes remain unchanged, because the determinant is exactly equal to $1$. The positive sign of the determinant confirms that a right-handed coordinate system remains right-handed after the transformation.