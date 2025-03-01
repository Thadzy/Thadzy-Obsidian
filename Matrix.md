cpp 
A matrix in C++ is essentially a 2D array, where data is organized in rows and columns. Below is a cheatsheet for working with matrices in C++, including declaration, initialization, and common operations.

---

# C++ Matrix Cheatsheet

This cheatsheet provides a quick reference for working with matrices (2D arrays) in C++.

## Table of Contents
1. [Matrix Declaration](#matrix-declaration)
2. [Matrix Initialization](#matrix-initialization)
3. [Accessing Matrix Elements](#accessing-matrix-elements)
4. [Matrix Input and Output](#matrix-input-and-output)
5. [Matrix Operations](#matrix-operations)
   - [Addition](#addition)
   - [Subtraction](#subtraction)
   - [Multiplication](#multiplication)
   - [Transpose](#transpose)
6. [Dynamic Matrices](#dynamic-matrices)

---

## Matrix Declaration

A matrix is declared as a 2D array with a fixed number of rows and columns.

### Syntax
```cpp
datatype matrixName[rows][columns];
```

### Example
```cpp
int matrix[3][3]; // A 3x3 integer matrix
```

---

## Matrix Initialization

Matrices can be initialized during declaration or later using nested loops.

### Static Initialization
```cpp
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

### Dynamic Initialization (Using Loops)
```cpp
int matrix[3][3];
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        matrix[i][j] = i + j;
    }
}
```

---

## Accessing Matrix Elements

Matrix elements are accessed using row and column indices.

### Example
```cpp
int value = matrix[1][2]; // Access element at row 1, column 2
```

---

## Matrix Input and Output

### Input
```cpp
int matrix[3][3];
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        std::cin >> matrix[i][j];
    }
}
```

### Output
```cpp
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        std::cout << matrix[i][j] << " ";
    }
    std::cout << std::endl;
}
```

---

## Matrix Operations

### Addition
To add two matrices, their dimensions must be the same.

```cpp
int matrix1[2][2] = {{1, 2}, {3, 4}};
int matrix2[2][2] = {{5, 6}, {7, 8}};
int result[2][2];

for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 2; j++) {
        result[i][j] = matrix1[i][j] + matrix2[i][j];
    }
}
```

### Subtraction
Subtraction is similar to addition.

```cpp
for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 2; j++) {
        result[i][j] = matrix1[i][j] - matrix2[i][j];
    }
}
```

### Multiplication
Matrix multiplication requires the number of columns in the first matrix to match the number of rows in the second matrix.

```cpp
int matrix1[2][3] = {{1, 2, 3}, {4, 5, 6}};
int matrix2[3][2] = {{7, 8}, {9, 10}, {11, 12}};
int result[2][2] = {0};

for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 2; j++) {
        for (int k = 0; k < 3; k++) {
            result[i][j] += matrix1[i][k] * matrix2[k][j];
        }
    }
}
```

### Transpose
The transpose of a matrix is obtained by swapping rows and columns.

```cpp
int matrix[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
int transpose[3][3];

for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        transpose[j][i] = matrix[i][j];
    }
}
```

---

## Dynamic Matrices

For matrices with dynamic sizes, use `std::vector` or dynamically allocated arrays.

### Using `std::vector`
```cpp
#include <vector>

std::vector<std::vector<int>> matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

### Using Dynamic Arrays
```cpp
int rows = 3, cols = 3;
int** matrix = new int*[rows];
for (int i = 0; i < rows; i++) {
    matrix[i] = new int[cols];
}

// Don't forget to deallocate memory
for (int i = 0; i < rows; i++) {
    delete[] matrix[i];
}
delete[] matrix;
```

---