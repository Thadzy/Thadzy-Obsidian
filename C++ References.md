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
#include <iostream>
#include <string>
using namespace std;

int main() {
  string food = "Pizza";
  string &meal = food;

  cout << food << "\n";
  cout << meal << "\n";
  return 0;
}
```

Output :
```
Pizza  
Pizza
```


