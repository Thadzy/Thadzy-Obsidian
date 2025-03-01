pp 
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

## Loop vector
In C++, you can loop through a `std::vector` using several methods. Below are the most common ways to iterate over a vector:

---

### 1. **Using a Range-Based For Loop (C++11 and later)**
This is the simplest and most modern way to loop through a vector.

#### Syntax:
```cpp
for (auto& element : vectorName) {
    // Use 'element'
}
```

#### Example:
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    for (auto& num : vec) {
        std::cout << num << " ";
    }

    return 0;
}
```

**Output**:
```
1 2 3 4 5
```

---

### 2. **Using an Index-Based For Loop**
You can use a traditional `for` loop with an index to access elements of the vector.

#### Syntax:
```cpp
for (size_t i = 0; i < vectorName.size(); i++) {
    // Use 'vectorName[i]'
}
```

#### Example:
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    for (size_t i = 0; i < vec.size(); i++) {
        std::cout << vec[i] << " ";
    }

    return 0;
}
```

**Output**:
```
1 2 3 4 5
```

---

### 3. **Using an Iterator**
You can use iterators to loop through a vector. This is useful when you need more control over the iteration process.

#### Syntax:
```cpp
for (auto it = vectorName.begin(); it != vectorName.end(); ++it) {
    // Use '*it'
}
```

#### Example:
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    for (auto it = vec.begin(); it != vec.end(); ++it) {
        std::cout << *it << " ";
    }

    return 0;
}
```

**Output**:
```
1 2 3 4 5
```

---

### 4. **Using `std::for_each` with a Lambda Function (C++11 and later)**
You can use the `std::for_each` algorithm from the `<algorithm>` library to loop through a vector.

#### Syntax:
```cpp
#include <algorithm>

std::for_each(vectorName.begin(), vectorName.end(), [](auto& element) {
    // Use 'element'
});
```

#### Example:
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    std::for_each(vec.begin(), vec.end(), [](int& num) {
        std::cout << num << " ";
    });

    return 0;
}
```

**Output**:
```
1 2 3 4 5
```

---

### 5. **Using a While Loop with an Iterator**
You can also use a `while` loop with iterators for more flexibility.

#### Syntax:
```cpp
auto it = vectorName.begin();
while (it != vectorName.end()) {
    // Use '*it'
    ++it;
}
```

#### Example:
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    auto it = vec.begin();
    while (it != vec.end()) {
        std::cout << *it << " ";
        ++it;
    }

    return 0;
}
```

**Output**:
```
1 2 3 4 5
```

---

### Summary Table

| Method                     | Syntax Example                              | Use Case                              |
|----------------------------|---------------------------------------------|---------------------------------------|
| Range-Based For Loop        | `for (auto& x : vec)`                      | Simple iteration                      |
| Index-Based For Loop        | `for (size_t i = 0; i < vec.size(); i++)`  | Access elements by index              |
| Iterator-Based For Loop     | `for (auto it = vec.begin(); it != vec.end(); ++it)` | More control over iteration |
| `std::for_each` with Lambda | `std::for_each(vec.begin(), vec.end(), [](auto& x) { ... })` | Functional programming style |
| While Loop with Iterator    | `while (it != vec.end())`                  | Flexible iteration                    |

---

### When to Use Which Method?
- **Range-Based For Loop**: Use this for simple iteration when you don't need the index or iterator.
- **Index-Based For Loop**: Use this when you need the index of the elements.
- **Iterator-Based For Loop**: Use this when you need more control, such as modifying the vector during iteration.
- **`std::for_each`**: Use this for a functional programming style or when applying a function to each element.
- **While Loop with Iterator**: Use this for more complex iteration logic.

Let me know if you need further clarification! 😊