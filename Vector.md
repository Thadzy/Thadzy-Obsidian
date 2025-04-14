---
tags:
  - Calculus
  - Calculus2
date:
---

---

# 📘 Introduction to Vectors in 3D Space

A **vector** is a mathematical object characterized by **magnitude** (length) and **direction**. Vectors are fundamental in physics, engineering, and mathematics, especially in 3D coordinate systems.

---

## 1. Vectors in Coordinate Systems

![Vector Representations](attachment:c1e3cfdd-2f24-4ad4-8ee4-258c138ff6f8:image.png)

Vectors are often represented in 2D and 3D Cartesian coordinate systems using component form:

v⃗=ai^+bj^+ck^\vec{v} = a\hat{i} + b\hat{j} + c\hat{k}

---

## 2. Vector Between Two Points

Given two points:

- B(−1,−2,3)B(-1, -2, 3)
    
- C(1,1,4)C(1, 1, 4)
    

To find the vector **CB**, subtract the coordinates of **C** from **B**:

CB⃗=B⃗−C⃗=(−1,−2,3)−(1,1,4)=(−2,−3,−1)\vec{CB} = \vec{B} - \vec{C} = (-1, -2, 3) - (1, 1, 4) = (-2, -3, -1)

> 💡 Rule: **Vector from point P to Q is** PQ⃗=Q⃗−P⃗\vec{PQ} = \vec{Q} - \vec{P}

---

## 3. Magnitude of a Vector (Norm)

The **magnitude** (or **norm**) of a vector A⃗=(a1,a2,a3)\vec{A} = (a_1, a_2, a_3) is:

∥A⃗∥=a12+a22+a32\|\vec{A}\| = \sqrt{a_1^2 + a_2^2 + a_3^2}

![Norm Diagram](attachment:2729dc55-1d9c-45aa-8c96-4b0b451e6c2a:image.png)

---

## 4. Unit Vector

A **unit vector** has a magnitude of **1**. It is calculated by dividing a vector by its norm:

u^=v⃗∥v⃗∥\hat{u} = \frac{\vec{v}}{\|\vec{v}\|} ∣v^∣=(x∥v⃗∥)2+(y∥v⃗∥)2+(z∥v⃗∥)2=x2+y2+z2x2+y2+z2=1=1|\hat{v}| = \sqrt{\left(\frac{x}{\|\vec{v}\|}\right)^2 + \left(\frac{y}{\|\vec{v}\|}\right)^2 + \left(\frac{z}{\|\vec{v}\|}\right)^2} = \sqrt{\frac{x^2 + y^2 + z^2}{x^2 + y^2 + z^2}} = \sqrt{1} = 1

---

## 5. Dot Product

The **dot product** (scalar product) of two vectors:

A⃗⋅B⃗=AxBx+AyBy+AzBz\vec{A} \cdot \vec{B} = A_xB_x + A_yB_y + A_zB_z

Alternatively:

A⃗⋅B⃗=∣A⃗∣∣B⃗∣cos⁡θ\vec{A} \cdot \vec{B} = |\vec{A}| |\vec{B}| \cos\theta

---

## 6. Angle Between Vectors

θ=cos⁡−1(A⃗⋅B⃗∣A⃗∣∣B⃗∣)\theta = \cos^{-1} \left( \frac{\vec{A} \cdot \vec{B}}{|\vec{A}||\vec{B}|} \right)

---

## 7. Direction Angles and Cosines

[Watch on YouTube](https://www.youtube.com/watch?v=ZoCxUV893fo)

Direction angles are calculated based on the vector's angle with respect to the **x-, y-, and z-axes**, using the same formula as the angle between vectors.

---

## 8. Vector Projection

[Watch: Vector Projection](https://www.youtube.com/watch?v=Rw70zkvqEiE)

### Scalar Projection:

compB(A⃗)=A⃗⋅B⃗∣B⃗∣\text{comp}_B(\vec{A}) = \frac{\vec{A} \cdot \vec{B}}{|\vec{B}|}

### Vector Projection:

projB(A⃗)=A⃗⋅B⃗∣B⃗∣2B⃗\text{proj}_B(\vec{A}) = \frac{\vec{A} \cdot \vec{B}}{|\vec{B}|^2} \vec{B}

---

## 9. Cross Product

The **cross product** yields a vector perpendicular to both vectors:

A⃗×B⃗=∣i^j^k^AxAyAzBxByBz∣\vec{A} \times \vec{B} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ A_x & A_y & A_z \\ B_x & B_y & B_z \\ \end{vmatrix}

Magnitude:

∣A⃗×B⃗∣=∣A⃗∣∣B⃗∣sin⁡θ|\vec{A} \times \vec{B}| = |\vec{A}||\vec{B}|\sin\theta

---

## 10. Triple Products

### Scalar Triple Product (Volume of Parallelepiped):

A⃗⋅(B⃗×C⃗)\vec{A} \cdot (\vec{B} \times \vec{C})

Volume = Base Area×Height\text{Base Area} \times \text{Height}

Base Area=∣B⃗×C⃗∣,Height=∣projB⃗×C⃗A⃗∣\text{Base Area} = |\vec{B} \times \vec{C}|,\quad \text{Height} = \left| \text{proj}_{\vec{B} \times \vec{C}} \vec{A} \right|

### Vector Triple Product:

A⃗×(B⃗×C⃗)\vec{A} \times (\vec{B} \times \vec{C})

---

## 11. Line in 3D Space

A line LL passing through point P0(x0,y0,z0)P_0(x_0, y_0, z_0) and parallel to vector v⃗=(a,b,c)\vec{v} = (a, b, c) is defined as:

(x,y,z)=(x0+at,y0+bt,z0+ct)(x, y, z) = (x_0 + at, y_0 + bt, z_0 + ct)

### Symmetric Form:

x−x0a=y−y0b=z−z0c\frac{x - x_0}{a} = \frac{y - y_0}{b} = \frac{z - z_0}{c}

---

## 12. Distance from a Point to a Line

Given point QQ and line LL, the distance is:

Distance=∣PQ⃗∣sin⁡θ=∣PQ⃗×v⃗∣∣v⃗∣\text{Distance} = |\vec{PQ}|\sin\theta = \frac{|\vec{PQ} \times \vec{v}|}{|\vec{v}|}

---

## 13. Plane Equation

A plane through point P0(x0,y0,z0)P_0(x_0, y_0, z_0) with normal vector N⃗=(a,b,c)\vec{N} = (a, b, c):

a(x−x0)+b(y−y0)+c(z−z0)=0a(x - x_0) + b(y - y_0) + c(z - z_0) = 0

Or:

Ax+By+Cz+D=0Ax + By + Cz + D = 0

---

## 14. Angle Between Two Planes

cos⁡θ=N1⃗⋅N2⃗∣N1⃗∣∣N2⃗∣⇒θ=cos⁡−1(N1⃗⋅N2⃗∣N1⃗∣∣N2⃗∣)\cos\theta = \frac{\vec{N_1} \cdot \vec{N_2}}{|\vec{N_1}||\vec{N_2}|} \quad \Rightarrow \quad \theta = \cos^{-1}\left(\frac{\vec{N_1} \cdot \vec{N_2}}{|\vec{N_1}||\vec{N_2}|}\right)

---

## 15. Vector Functions

A vector-valued function in space:

r⃗(t)=x(t)i^+y(t)j^+z(t)k^\vec{r}(t) = x(t)\hat{i} + y(t)\hat{j} + z(t)\hat{k}

Each component function describes the path along each axis as tt changes.

---

Let me know if you want this exported as a PDF, Markdown, or formatted as LaTeX for reports.[[Calculus II Vector 1c16a0bdba2a807fa2f9dfd84b22916a]]