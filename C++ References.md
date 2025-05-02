---
tags:
  - Cpp
  - OOP
date: 2025-05-02
---
## Introduction 
In C++, a **reference** works as an alias for an existing variable, providing an alternative name for it and allowing you to work with the original data directly.
## Creating References
A reference variable is a "reference" to an existing variable, and it is created with the `&` operator:
```cpp
string food = "Pizza";  // food variable  
string &meal = food;    // reference to food
```

