---
tags:
  - Calculus
  - Calculus2
date:
---
## Introduction 
A vector is an object that has both a magnitude and a direction. 
# 1. Vector in Coordination Systems

![image.png](attachment:c1e3cfdd-2f24-4ad4-8ee4-258c138ff6f8:image.png)

![image.png](attachment:14e18aab-544c-4c97-a3ca-7f32baf18c33:image.png)

# 2. Vector between 2 points

![image.png](attachment:ec183c71-e327-4f10-8785-a0f21a73e3a9:image.png)

How to find Ex if B, C at coordinates (-1,-2,3) and (1,1,4) please find the Vector CB

Solution **last - before** Therefore CB = B - C

# 3. Magnitude of Vector (Norm)

is the length or the size of the vector

$$ || A || = \sqrt{a_1^2+a_2^2+a_3^2} $$

![image.png](attachment:2729dc55-1d9c-45aa-8c96-4b0b451e6c2a:image.png)

<aside> 💡

How to Pythagorean can find the Magnitude of the vector?

Maybe about the shadow it’s represent the components x,y,z

![image.png](attachment:c9a881a9-da82-43b2-8401-62619b1ee021:image.png)

</aside>

# 4. Unit Vector

is the vector size = 1

![image.png](attachment:daca862c-4dc5-4f6a-8d5c-9d2a8fdc0672:image.png)

$$ u = \frac{v}{||v||} $$

<aside> 💡

Why unit vector = 1?

$|\hat{v}| = \sqrt{\left(\frac{x}{\sqrt{x^2 + y^2 + z^2}}\right)^2 + \left(\frac{y}{\sqrt{x^2 + y^2 + z^2}}\right)^2 + \left(\frac{z}{\sqrt{x^2 + y^2 + z^2}}\right)^2}$

simplify this

$|\hat{v}| = \sqrt{\frac{x^2 + y^2 + z^2}{x^2 + y^2 + z^2}} = \sqrt{1} = 1$

</aside>

# 5. Dot Product

is the multiply 2 vectors to scale the length

$$ A⋅B=AxBx+AyBy+AzBz $$

$$ a⋅b=∣a∣∣b∣cos(θ) $$

<aside> 💡

What is cos theta

![image.png](attachment:48bf11ea-2b6f-4118-a51a-483ca2a41398:061c76ff-a63a-4d31-942c-7db570cffbfb.png)

measure how 2 vectors closely align in direction if

**θ = 0 parallel**

**θ = 90 perpendicular**

**θ < 90 negative (opposite direction)**

</aside>

# 6. Angle Between Vectors

$$ \theta = cos^{-1}(\frac{AB}{|A||B|}) $$

# 7. Direction angle and Direction cosine

[https://www.youtube.com/watch?v=ZoCxUV893fo](https://www.youtube.com/watch?v=ZoCxUV893fo)

maybe just use Angle Between Vectors of 3 dimension

find the vector that the problem wants and calculate the theta by the axis

![image.png](attachment:b5d11fc2-62d6-4bbc-a41b-ba35b918304a:image.png)

# 8. Vector Projection

[https://www.youtube.com/watch?v=Rw70zkvqEiE](https://www.youtube.com/watch?v=Rw70zkvqEiE)

is the process of projecting 1 vector onto another vector it helps to determine how much one vector lies in the direction of another there are 2 types

## Scalar Projection

Components of one vector along another

Ex. Components of vector A along vector B

$$ Comp_B(A) = \frac{AB}{|B|} $$

## Vector Projection

$$ proj_B(A) = \frac{AB}{|B|^2}B $$

<aside> 💡

Imagine a flashlight shining from a tip of A onto B

![image.png](attachment:f7445910-8b95-4f32-99c6-cf93224b7183:image.png)

</aside>

<aside> 💡

Observation

Vector Projection is the vector

Scalar Projection is length of projection (Non-negative)

Scalar Component might be negative if the obtuse angle

</aside>

# 9. Cross Product

is the product between 2 vectors that output third vector that will be perpendicular to A and B

![image.png](attachment:c92f32e9-9c8a-48e8-81a1-b1626bd52d15:image.png)

$$ \mathbf{A} \times \mathbf{B} =\begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ A_x & A_y & A_z \\ B_x & B_y & B_z \end{vmatrix} $$

## Magnitude of the Cross Product

$$ ∥A×B∥=∥A∥∥B∥sinθ $$

<aside> 💡

If θ = 0, θ = 180 vectors are parallel, and the cross product is zero

If θ = 90, vectors are perpendicular

</aside>

# 10. Triple Product

there are 2 types

## Scalar Triple Product

is volume of parallelopiped

$$ A(B \times C) $$

![image.png](attachment:75b5dc34-0761-413c-8dcf-7e8619b3374e:image.png)

![image.png](attachment:79bbeab4-8570-485f-a418-39ec39259ff6:image.png)

### Find the volume of parallelopiped

Base Area = $|B \times C|$

Height = $|proj_{B \times C}A|$

## Vector Triple Product

$$ A \times (B \times C) $$

# 11. Straight line in 3D coordinate system

Give the line L pass the point $P_0(x_0,y_0,z_0)$ and parallel with the vector v

![image.png](attachment:f3e04205-536b-4858-bd25-8d45a25bd03b:image.png)

Therefore, every point in P(x,y,z) on line L will have the real number t that makes :

$$ P_0P = tv $$

- $P_0P$ is the distance between $P_0$ to any P
- v give the direction of the line
- t is the scalar

$$ or (x-x_0,y-y_0,z-z_0)=(ta,tb,tc) $$

<aside> 💡

Pipeline

1. Start at Point $P_0$
2. Vector v shows which way it goes
3. By scaling t to v to make it reach the point $P_0$ </aside>

In other words, it’s called

## Parametric Equation

use to describe the path of an object

$$ x = x_0 + at $$

$$ y = y_0 +bt $$

$$ z = z_0 + ct $$

- v is the direction vector of line L
- a,b,c is the direction number

we call the equation of L in

$$ \frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c} $$

and a,b,c ≠ 0 we called symmetric equation

# 12. Distance between point and straight line

![image.png](attachment:18128609-158c-4bcb-a669-f1d8e9f4a8d1:image.png)

Distance between Q and line L =

$$ |PQ|sin\theta=\frac{|PQ \times v|}{|v|} $$

# 13. **Plane Equation**

Plane is the set of point (x,y,z) according to equation Ax+By+Cz+D = 0

$$ a(x−x0)+b(y−y0)+c(z−z0)=0 $$

- A,B,C are the components of a vector to the plane
- (x,y,z) are the coordinates of any point on the plane
- D is a constant that determines the position of the plane

<aside> 💡

The key concept is

![image.png](attachment:82f86eb6-3ccc-4f8f-8e79-2457afc1794a:image.png)

It uses position vector and perpendicular concepts is

**Position vector concept**

$$ P_0P $$

**Perpendicularity Condition**

$$ N \cdot P_0P = 0 $$

Therefore, N = (a,b,c), P = x-x0

$$ a(x−x0)+b(y−y0)+c(z−z0)=0 $$

</aside>

# 14. Angles and intersections between planes

**Angle between plane =** angle between normal vector of two planes act on each other

![image.png](attachment:f9c2d259-fc47-4745-8c19-aef33b22c324:image.png)

$$ cos \theta = \frac{N_1 \cdot N_2}{|N_1||N_2|} $$

$$ \theta = cos^{-1}\frac{N_1 \cdot N_2}{|N_1||N_2|} $$

<aside> 💡

Two planes if not parallel, always intersect; $N_1 \times N_2$ is the vector parallel with the two planes.

</aside>

# 15. Vector Functions

$$ r(t) = x(t)i + y(t)i + z(t)k $$

- r(t) is function vector of t
- x(t), y(t), z(t) is component of r(t)

## Might useful example

$$ r(t) = 2costi + 2sintj + tk $$

![image.png](attachment:87ddcf58-897e-4bac-a411-56a049c68d98:image.png)

This is a **Circular helix $x^2 + y^2 = 4$**

# 16. Derivative of a vector function

use derivative

$$ r'(t) = \lim_{\Delta t\to0}\frac{r(t + \Delta t) -r(t)}{\Delta t} $$

<aside> 💡

if |r(t)| ≠ 0; |r(t)| is const when r’(t) ⊥ r(t) for every t

</aside>

## Smooth Curve

if r(t) is continuous and ≠ 0 for every a ≤ t ≤ b ⇒ **Smooth Curve**

and we call curve C from r(t) is smooth curve

## Length of a space curve

we can find the length of curve C on [a, b]

$$ L = \int_a^b\sqrt{[x'(t)]^2+[y'(t)]^2+[z'(t)]^2} dt $$

$$ \int_a^b|r'(t)|dt $$

# 17. Arc length as a parameter

![image.png](attachment:e7cc0b87-c4cd-4d11-8f09-1e9dac85cdf0:image.png)

$$ s(\tau) = \int_a^\tau|r'(\tau)|d\tau = \int_a^\tau\sqrt{[x'(\tau)]^2+[y'(\tau)]^2+[z'(\tau)]^2} dt $$

<aside> 💡

$$ \frac{ds}{dt} = |r'(t)| $$

If C is the Smooth curve

$$ r(s) = x(s)i+y(s)j+z(s)k $$

When s is the arc length parameter therefore

$$ |r'(s)|=1 $$

</aside>

# 18. Tangent Vector

is a vector that is tangent to the curve

![image.png](attachment:47806cab-8649-4455-bed9-6ec1d8af7986:image.png)

- No definition of tangent vector if r’(t) = 0
- The equation is of curve C at $t = t_0$

$$ r(t) = r(t_0) + tr'(t_0) $$

# 19. Velocity, Acceleration and Speed

1. Velocity vector is $r'(t)$
2. Acceleration vector is $r''(t)$
3. Speed is $|v(t)|$
4. Direction of v(t) is $\frac{v(t)}{|v(t)|}$

# 20. Unit Tangent Vector

It’s like the Tangent vector but = 1

$$ T(t) = \frac{r'(t)}{|r'(t)|} = \frac{v(t)}{|v(t)|} $$

![image.png](attachment:aa39cf2f-6200-419d-bdf7-6bf9f7e59485:f86ac2bd-6e8d-4d29-a954-de98f43035d2.png)

# 21. Curvature

![image.png](attachment:28598189-47d8-4afa-aa2c-962f2aaf1774:image.png)

As we see this T since P1 → P2 has a little changed but P3 is very much so we will use **The rate of change of the tangent vector is 1 unit compare with s to tell the Curvature (C)**

<aside> 💡

Because of Unit tangent vector doesn’t change the volume but change only direction

</aside>

K is Kappa

$$ K(s) = |\frac{dT}{ds}| = |r''(s)| $$

$$ K(t) = |\frac{dT}{ds}| = \frac{1}{|v|}|\frac{dT}{ds}| = \frac{T'(t)}{r'(t)} $$

$$ K(t) = \frac{|r'(t) \times r''(t)|}{|r'(t)|^3} = \frac{|v(t) \times a(t)|}{|v(t)^3|} $$

# 22. Unit Normal Vector

a normal vector that is perpendicular to the vector

![image.png](attachment:16aaca00-2857-4b8e-afd8-5d515bad1424:image.png)

$$ N(t) = \frac{T'(t)}{|T'(t)|} $$

What if r(s) it will be

$$ N(s) = \frac{1}{K}\frac{dT}{ds} $$

N(s) is Principal unit normal vector

<aside> 💡

N always point to the circle

</aside>

# 23. Circle of Curvature and Radius of Curvature

![image.png](attachment:2e87de90-7ab6-47ad-83e2-4d06c23c8d27:image.png)

We call the circle that is tangent with circle C at P the **Circle of curvature or Osculation circle**

and the Radius of Curvature is

$$ \rho = \frac{1}{K} $$

and the center call **Center of Curvature**

# 22. Unit Binormal Vector

is a unit vector that orthogonal T(t) and N(t)

![image.png](attachment:df111da9-bee7-4717-acf1-ff8f90eec1bd:image.png)

$$ B = T \times N $$

<aside> 💡

B is unit vector because $||B|| = ||T \times N|| = ||T||||N||sin\frac{\pi}{2} = 1$

</aside>

## Frenet frame or TNB Frame

![image.png](attachment:0ab99baf-7a2e-4b3f-a8f3-d3b6bbfde681:image.png)

- T - N is Osculating plane
- N - B is Normal plane
- B - T is Rectifying plane

# 23. Torsion

It is a tool used to measure how twisted a curve is

![image.png](attachment:822f465a-a08f-4bf0-90b0-37aa50680cd4:image.png)

$$ τ=−\frac{dB/dt⋅N}{∣∣dr/dt∣∣} $$

- Tangent vector (T(t)) shows the direction of the curve
- Normal vector (N(t)) points toward the curve’s curvature direction
- Binormal vector (B(t)) forms a right-handed systems with T and N