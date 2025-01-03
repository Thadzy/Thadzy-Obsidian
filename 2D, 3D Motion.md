#Physics 
[[1D Motion]]
[[Projectile Motion]]
[[Circular Motion]]
# 2D Motion
![[Pasted image 20250103172935.png | 600]]
## Vector
A vector is defined as an object characterized by both a magnitude (length) and a direction. Geometrically, it can be visualized as a directed line segment, where the length of the segment corresponds to the magnitude and the arrow indicates the direction
### Type of vector 
- **Zero Vector**: A vector with zero magnitude and no specific direction.
- ![[Pasted image 20250103173037.png]]
- **Unit Vector**: A vector with a magnitude of one, used to indicate direction.
	- How to calculate the unit vector $$u = \frac{v}{||v||}$$
	- Pythagorean $$u = \sqrt{a^2 + b^2}$$
- ![[Pasted image 20250103173058.png]]
- **Position Vector**: Represents the position of a point in space relative to an origin.
- ![[Pasted image 20250103173122.png]]
- **Displacement Vector**: Indicates the change in position from one point to another
- ![[Pasted image 20250103173257.png]]
> What is the different between vector in Physics, Math, Machine learning
>> Ans
### Vector in physics
- **Definition**: In physics, a vector is a quantity that has both **magnitude** and **direction**. Common examples include displacement, velocity, acceleration, and force
- **Representation**: Vectors are often represented graphically as arrows, where the length indicates magnitude and the arrowhead indicates direction. For instance, a force vector might show how strong and in which direction a force is applied
- **Operations**: Physics utilizes vector operations such as addition (using the head-to-tail method) and scalar multiplication to analyze forces and motion. The laws governing these operations are crucial for solving problems related to dynamics and kinematics
### Vectors in Mathematics

- **Definition**: In mathematics, vectors are defined similarly as entities with both magnitude and direction but can also represent ordered tuples of numbers in vector spaces. They can exist in any dimension, not just physical space
- **Types**: There are various types of vectors in mathematics, including zero vectors, unit vectors, position vectors, and more. Each type serves different purposes in mathematical analysis and geometry
- **Applications**: Vectors are fundamental in linear algebra, where they are used to solve systems of equations, perform transformations, and model various mathematical structures. Operations like dot product and cross product are essential for understanding relationships between vectors
### Vectors in Deep Learning (AI)

- **Definition**: In deep learning, vectors often represent data points or features. They can be thought of as arrays of numbers that encode information about an input or output in a model
- **Representation**: Each vector corresponds to a point in a high-dimensional space. For example, an image can be represented as a vector where each element corresponds to pixel intensity values
- **Operations**: Vector operations in AI include addition and scalar multiplication but also involve more complex operations such as matrix multiplication during the training of neural networks. These operations help in adjusting weights during backpropagation to minimize error functions

## How to calculate?
$$ v = \frac{d}{dt}r = \frac{d}{dt}(xi + yj) = \frac{d}{dt}(xi)+\frac{d}{dt}(yj)$$
$$= i\frac{dx}{dt}+ j \frac{dy}{dt} $$
$$ v = v_xi + v_yi $$
$$ v_x = \frac{dx}{dt}, v_y = \frac{dy}{dt}$$
## How to draw the vector
### Pythagorean
$$v = \sqrt{v_i^2+v_j^2}$$
### Arctan
>**Why Arctan?**
>>*Ans* The arctangent function is specifically suited for this purpose because it relates the opposite side (vertical component vjvj​) to the adjacent side (horizontal component vivi​) of a right triangle formed by these components. The tangent of an angle in a right triangle is defined as:
$$θ = tan^{-1}(\frac{v_i}{v_j})$$
![[Pasted image 20241022154608.png]]

## How to find velocity
t = t, t_small points to find v from $v = \sqrt{v_i^2+v_j^2}$ and arctan
## How to find acceleration
### a parallel
#### First method
$$a_{ll} = \frac{v - u}{t} $$
#### Second method 
cos
![[Pasted image 20241022164432.png | 500]]
### a perpendicular 
sin
#### Prediction
1. V increasing because of $a_{ll}$ has the same direction with v
2. acceleration $a_p$ make the particle move circular

