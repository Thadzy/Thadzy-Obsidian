

Created: March 25, 2025 10:50 PM
Tags: Mathematics

[1.Vectors, Lines and Planes_Student.pdf](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/1.Vectors_Lines_and_Planes_Student.pdf)

[2.+Vector+Functions_Student-1 (2).pdf](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/2.VectorFunctions_Student-1_(2).pdf)

# 1. Vector in Coordination Systems

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image.png)

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%201.png)

# 2. Vector between 2 points

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%202.png)

How to find Ex if B, C at coordinates (-1,-2,3) and (1,1,4) please find the Vector CB 

Solution **last - before** Therefore CB = B - C

# 3. Magnitude of Vector (Norm)

is the length or the size of the vector 

$$
|| A || = \sqrt{a_1^2+a_2^2+a_3^2}
$$

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%203.png)

<aside>
💡

How to Pythagorean can find the Magnitude of the vector? 

Maybe about the shadow it’s represent the components x,y,z

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%204.png)

</aside>

# 4. Unit Vector

is the vector size = 1

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%205.png)

$$
u = \frac{v}{||v||}
$$

<aside>
💡

Why unit vector = 1?

$|\hat{v}| = \sqrt{\left(\frac{x}{\sqrt{x^2 + y^2 + z^2}}\right)^2 + \left(\frac{y}{\sqrt{x^2 + y^2 + z^2}}\right)^2 + \left(\frac{z}{\sqrt{x^2 + y^2 + z^2}}\right)^2}$

simplify this

$|\hat{v}| = \sqrt{\frac{x^2 + y^2 + z^2}{x^2 + y^2 + z^2}} = \sqrt{1} = 1$

</aside>

# 5. Dot Product

is the multiply 2 vectors to scale the length

$$
A⋅B=Ax​Bx​+Ay​By​+Az​Bz​
$$

$$
a⋅b=∣a∣∣b∣cos(θ)
$$

<aside>
💡

What is cos theta 

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/061c76ff-a63a-4d31-942c-7db570cffbfb.png)

measure how 2 vectors closely align in direction if 

**θ = 0 parallel**

**θ = 90 perpendicular**

**θ < 90 negative (opposite direction)**

</aside>

# 6. Angle Between Vectors

$$
\theta = cos^{-1}(\frac{AB}{|A||B|})
$$

# 7. Direction angle and Direction cosine

https://www.youtube.com/watch?v=ZoCxUV893fo

maybe just use Angle Between Vectors of 3 dimension 

find the vector that the problem wants and calculate the theta by the axis

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%206.png)

# 8. Vector Projection

https://www.youtube.com/watch?v=Rw70zkvqEiE

is the process of projecting 1 vector onto another vector it helps to determine how much one vector lies in the direction of another  there are 2 types

## Scalar Projection

Components of one vector along another

Ex. Components of vector A along vector B

$$
Comp_B(A) = \frac{AB}{|B|}
$$

## Vector Projection

$$
proj_B(A) = \frac{AB}{|B|^2}B
$$

<aside>
💡

Imagine a flashlight shining from a tip of A onto B

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%207.png)

</aside>

<aside>
💡

Observation

Vector Projection is the vector

Scalar Projection is length of projection (Non-negative)

Scalar Component might be negative if the obtuse angle

</aside>

# 9. Cross Product

is the product between 2 vectors that output third vector that will be perpendicular to A and B 

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%208.png)

$$
\mathbf{A} \times \mathbf{B} =\begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ A_x & A_y & A_z \\ B_x & B_y & B_z \end{vmatrix}
$$

## Magnitude of the Cross Product

$$
∥A×B∥=∥A∥∥B∥sinθ
$$

<aside>
💡

If θ = 0, θ = 180 vectors are parallel, and the cross product is zero

If θ = 90, vectors are perpendicular

</aside>

# 10. Triple Product

there are 2 types

## Scalar Triple Product

is volume of parallelopiped

$$
A(B \times C)
$$

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%209.png)

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2010.png)

### Find the  volume of parallelopiped

Base Area = $|B \times C|$

Height = $|proj_{B \times C}A|$

## Vector Triple Product

$$
A \times (B \times C)
$$

# 11. Straight line in 3D coordinate system

Give the line L pass the point $P_0(x_0,y_0,z_0)$ and parallel with the vector v

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2011.png)

Therefore,  every point in P(x,y,z) on line L will have the real number t that makes :

$$
P_0P = tv
$$

- $P_0P$  is the distance between $P_0$  to any P
- v give the direction of the line
- t is the scalar

$$
or (x-x_0,y-y_0,z-z_0)=(ta,tb,tc)
$$

<aside>
💡

Pipeline

1. Start at Point $P_0$
2. Vector v shows which way it goes
3. By scaling t to v to make it reach the point $P_0$
</aside>

In other words, it’s called

## Parametric Equation

use to describe the path of an object

$$
x = x_0 + at
$$

$$
y = y_0 +bt
$$

$$
z = z_0 + ct
$$

- v is the direction vector of line L
- a,b,c is the direction number

we call the equation of L in

$$
\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}
$$

and a,b,c ≠ 0 we called symmetric equation

# 12. Distance between point and straight  line

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2012.png)

Distance between Q and line L =

$$
|PQ|sin\theta=\frac{|PQ \times v|}{|v|}
$$

# 13. **Plane Equation**

Plane is the set of point (x,y,z) according to equation Ax+By+Cz+D = 0

$$
a(x−x0​)+b(y−y0​)+c(z−z0​)=0
$$

- A,B,C are the components of a vector to the plane
- (x,y,z) are the coordinates of any point on the plane
- D is a constant that determines the position of the plane

<aside>
💡

The key concept is 

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2013.png)

It uses position vector and perpendicular concepts is 

**Position vector concept**

$$
P_0P
$$

**Perpendicularity Condition**

$$
N \cdot P_0P = 0
$$

Therefore, N = (a,b,c), P = x-x0

$$
a(x−x0)+b(y−y0)+c(z−z0)=0
$$

</aside>

# 14. Angles and intersections between planes

**Angle between plane =** angle between normal vector of two planes act on each other

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2014.png)

$$
cos \theta = \frac{N_1 \cdot N_2}{|N_1||N_2|}
$$

$$
\theta = cos^{-1}\frac{N_1 \cdot N_2}{|N_1||N_2|}
$$

<aside>
💡

Two planes if not parallel, always intersect; $N_1 \times N_2$ is the vector parallel with the two planes.

</aside>

# 15.  Vector Functions

$$
r(t) = x(t)i + y(t)i + z(t)k
$$

- r(t) is function vector of t
- x(t), y(t), z(t) is component of r(t)

## Might useful example

$$
r(t) = 2costi + 2sintj + tk
$$

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2015.png)

This is a **Circular helix  $x^2 + y^2 = 4$**

# 16. Derivative of a vector function

use derivative 

$$
r'(t) = \lim_{\Delta t\to0}\frac{r(t + \Delta t) -r(t)}{\Delta t}
$$

<aside>
💡

if |r(t)| ≠ 0; |r(t)| is const when r’(t) ⊥ r(t) for every t 

</aside>

## Smooth Curve

if r(t) is continuous and ≠ 0 for every a ≤ t ≤ b ⇒ **Smooth Curve** 

and we call curve C from r(t) is smooth curve

## Length of a space curve

we can find the length of curve C on [a, b]

$$
L = \int_a^b\sqrt{[x'(t)]^2+[y'(t)]^2+[z'(t)]^2} dt
$$

$$
\int_a^b|r'(t)|dt
$$

# 17. Arc length as a parameter

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2016.png)

$$
s(\tau) = \int_a^\tau|r'(\tau)|d\tau = \int_a^\tau\sqrt{[x'(\tau)]^2+[y'(\tau)]^2+[z'(\tau)]^2} dt
$$

<aside>
💡

$$
\frac{ds}{dt} = |r'(t)|
$$

If C is the Smooth curve

$$
r(s) = x(s)i+y(s)j+z(s)k
$$

When s is the arc length parameter therefore

$$
|r'(s)|=1
$$

</aside>

# 18. Tangent Vector

is a vector that is tangent to the curve

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2017.png)

- No definition of tangent vector if r’(t) = 0
- The equation is of curve C at $t = t_0$

$$
r(t) = r(t_0) + tr'(t_0)
$$

# 19. Velocity, Acceleration and Speed

1. Velocity vector is $r'(t)$
2. Acceleration vector is $r''(t)$
3. Speed is $|v(t)|$
4. Direction of v(t) is $\frac{v(t)}{|v(t)|}$

# 20. Unit Tangent Vector

It’s like the Tangent vector but = 1

$$
T(t) = \frac{r'(t)}{|r'(t)|} = \frac{v(t)}{|v(t)|}
$$

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/f86ac2bd-6e8d-4d29-a954-de98f43035d2.png)

# 21. Curvature

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2018.png)

As we see this T since P1 → P2 has a little changed but P3 is very much so we will use **The rate of change of the tangent vector is 1 unit compare with s to tell the Curvature (C)**

<aside>
💡

Because of Unit tangent vector doesn’t change the volume but change only direction

</aside>

K is Kappa

$$
K(s) = |\frac{dT}{ds}| = |r''(s)|
$$

$$
K(t) = |\frac{dT}{ds}| = \frac{1}{|v|}|\frac{dT}{ds}| = \frac{T'(t)}{r'(t)}
$$

$$
K(t) = \frac{|r'(t) \times r''(t)|}{|r'(t)|^3} = \frac{|v(t) \times a(t)|}{|v(t)^3|}
$$

# 22. Unit Normal Vector

a normal vector that is perpendicular to the vector

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2019.png)

$$
N(t) = \frac{T'(t)}{|T'(t)|}
$$

What if r(s) it will be

$$
N(s) = \frac{1}{K}\frac{dT}{ds}
$$

N(s) is Principal unit normal vector

<aside>
💡

N always point to the circle

</aside>

# 23. Circle of Curvature and Radius of Curvature

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2020.png)

We call the circle that is tangent with circle C at P the **Circle of curvature  or Osculation circle**

and the Radius of Curvature is 

$$
\rho = \frac{1}{K}
$$

and the center call **Center of Curvature**

# 22. Unit Binormal Vector

is a unit vector that orthogonal  T(t) and N(t)

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2021.png)

$$
B = T \times N
$$

<aside>
💡

B is unit vector because $||B|| = ||T \times N|| = ||T||||N||sin\frac{\pi}{2} = 1$

</aside>

## Frenet frame or TNB Frame

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2022.png)

- T - N is Osculating plane
- N - B is Normal plane
- B - T is Rectifying plane

# 23. Torsion

It is a tool used to measure how twisted a curve is

![image.png](Calculus%20II%20Vector%201c16a0bdba2a807fa2f9dfd84b22916a/image%2023.png)

$$
τ=−\frac{dB/dt⋅N}{∣∣dr/dt∣∣}
$$

- Tangent vector (T(t)) shows the direction of the curve
- Normal vector (N(t)) points toward the curve’s curvature direction
- Binormal vector (B(t)) forms a right-handed systems with T and N