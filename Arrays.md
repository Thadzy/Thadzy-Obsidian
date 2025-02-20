---
tags:
  - cpp
date: 
Link: "[[Matrix]]"
---
![[Pasted image 20250220161437.png]]
Array is the list used to store multiple values of similar data types in a contiguous memory location.
## Properties of Arrays in C++

- An Array is a collection of data of the same data type, stored at a contiguous memory location.
- Indexing of an array starts from 0. It means the first element is stored at the 0th index, the second at 1st, and so on.
- Elements of an array can be accessed using their indices.
- Once an array is declared its size remains constant throughout the program.
- An array can have multiple dimensions.
- The size of the array in bytes can be determined by the sizeof operator using which we can also find the number of elements in the array.
- We can find the size of the type of elements stored in an array by subtracting adjacent addresses.
## Array Declaration in C++
```cpp
data_type array_name[Size_of_array];
```

```cpp
int arr[5];
```
