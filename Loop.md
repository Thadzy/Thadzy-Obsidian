#cpp 
# C++ Loops Cheatsheet

This cheatsheet provides a quick reference to the different types of loops available in C++. Loops are used to execute a block of code repeatedly until a specified condition is met.

## Table of Contents
1. [For Loop](#for-loop)
2. [While Loop](#while-loop)
3. [Do-While Loop](#do-while-loop)
4. [Range-Based For Loop](#range-based-for-loop)
5. [Nested Loops](#nested-loops)
6. [Loop Control Statements](#loop-control-statements)

## For Loop

The `for` loop is used when you know in advance how many times you want to execute a block of code.

### Syntax
```cpp
for (initialization; condition; update) {
    // Code to be executed
}
```

### Example
```cpp
for (int i = 0; i < 5; i++) {
    std::cout << "i = " << i << std::endl;
}
```

## While Loop

The `while` loop is used when you want to repeat a block of code as long as a condition is true.

### Syntax
```cpp
while (condition) {
    // Code to be executed
}
```

### Example
```cpp
int i = 0;
while (i < 5) {
    std::cout << "i = " << i << std::endl;
    i++;
}
```

## Do-While Loop

The `do-while` loop is similar to the `while` loop, but it guarantees that the block of code is executed at least once, even if the condition is false.

### Syntax
```cpp
do {
    // Code to be executed
} while (condition);
```

### Example
```cpp
int i = 0;
do {
    std::cout << "i = " << i << std::endl;
    i++;
} while (i < 5);
```

## Range-Based For Loop

The range-based `for` loop is used to iterate over elements in a container (e.g., an array or a vector).

### Syntax
```cpp
for (element : container) {
    // Code to be executed
}
```

### Example
```cpp
std::vector<int> vec = {1, 2, 3, 4, 5};
for (int i : vec) {
    std::cout << "i = " << i << std::endl;
}
```

## Nested Loops

Nested loops are loops inside other loops. They are useful for working with multi-dimensional data structures.

### Example
```cpp
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        std::cout << "i = " << i << ", j = " << j << std::endl;
    }
}
```

## Loop Control Statements

C++ provides several control statements to manage the flow of loops:

- **`break`**: Terminates the loop immediately.
- **`continue`**: Skips the rest of the loop body and continues with the next iteration.
- **`goto`**: Jumps to a labeled statement (use sparingly).

### Example
```cpp
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        break; // Exit the loop when i is 5
    }
    if (i % 2 == 0) {
        continue; // Skip even numbers
    }
    std::cout << "i = " << i << std::endl;
}
```