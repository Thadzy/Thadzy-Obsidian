#cpp 
# Vector in Computer
## Introduction
Vector is the array that can resize and must have the same type
```cpp
#include <vector>
```
## Create a vector
```cpp
vector<string> cars;
```
## Loop through vector
```cpp 
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
   
for (string car : cars) {  
  cout << car << "\n";  
}
```
or for-each loop
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
  
for (string car : cars) {  
  cout << car << "\n";  
}
```
## Access a vector
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
  
cout << cars[0];  // Outputs Volvo  
cout << cars[1];  // Outputs BMW
```
### Also can access at back and front
```cpp 
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
  
cout << cars.front();  
cout << cars.back();
```
### And specific
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"}; 

cout << cars.at(1);   
cout << cars.at(2);
```
### Change a Vector Element
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"}; 

cars[0] = "Opel";  
cout << cars[0];  // Now outputs Opel instead of Volvo
```
However, it is safer to use the `.at()` function:
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};

cars.at(0) = "Opel";  
cout << cars.at(0);  // Now outputs Opel instead of Volvo
```
### Add Vector Elements
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
cars.push_back("Tesla");  
cars.push_back("VW");  
cars.push_back("Mitsubishi");  
cars.push_back("Mini");
```

### Remove Vector Elements
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
cars.pop_back();
```

## Vector Size
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
cout << cars.size();
```

## All Member Functions of Vector

Following is the list of all member functions of std::vector class in C++:
# Vector Functions

| Function        | Description |
|---------------|-------------|
| `push_back()` | Adds an element to the end of the vector. |
| `pop_back()` | Removes the last element of the vector. |
| `size()` | Returns the number of elements in the vector. |
| `max_size()` | Returns the maximum number of elements that the vector can hold. |
| `resize()` | Changes the size of the vector. |
| `empty()` | Checks if the vector is empty. |
| `operator[]` | Accesses the element at a specific position. |
| `at()` | Accesses the element at a specific position, with bounds checking. |
| `front()` | Accesses the first element of the vector. |
| `back()` | Accesses the last element of the vector. |
| `begin()` | Returns an iterator pointing to the first element of the vector. |
| `end()` | Returns an iterator pointing to the past-the-end element of the vector. |
| `rbegin()` | Returns a reverse iterator pointing to the last element of the vector. |
| `rend()` | Returns a reverse iterator pointing to the element preceding the first element of the vector. |
| `cbegin` | Returns `const_iterator` to beginning. |
| `cend` | Returns `const_iterator` to end. |
| `crbegin` | Returns `const_reverse_iterator` to reverse beginning. |
| `crend` | Returns `const_reverse_iterator` to reverse end. |
| `insert()` | Inserts elements at a specific position in the vector. |
| `erase()` | Removes elements from a specific position or range in the vector. |
| `swap()` | Swaps the contents of the vector with those of another vector. |
| `clear()` | Removes all elements from the vector. |
| `emplace()` | Constructs and inserts an element in the vector. |
| `emplace_back()` | Constructs and inserts an element at the end of the vector. |
| `assign()` | Assigns new values to the vector elements by replacing old ones. |
| `capacity()` | Returns the size of the storage space currently allocated to the vector. |
| `reserve()` | Requests that the vector capacity be at least enough to contain a specified number of elements. |
| `shrink_to_fit()` | Reduces memory usage by freeing unused space. |
| `data()` | Returns a direct pointer to the memory array used internally by the vector to store its owned elements. |
| `get_allocator` | Returns a copy of the allocator object associated with the vector. |


![[Pasted image 20250219235305.png]]
# Vector in Physics
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
