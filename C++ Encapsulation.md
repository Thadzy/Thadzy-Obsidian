---
tags:
  - Cpp
  - OOP
date: 2025-05-01
---
## Introduction 
The meaning of **Encapsulation**, is to make sure that "sensitive" data is hidden from users.
**If you want others to read or modify** the value of a private member, you can provide public **get** and **set** methods.
```cpp
#include <iostream>  
using namespace std;  
  
class Employee {  
  private:  
    // Private attribute  
    int salary;  
  
  public:  
    // Setter  
    void setSalary(int s) {  
      salary = s;  
    }  
    // Getter  
    int getSalary() {  
      return salary;  
    }  
};  
  
int main() {  
  Employee myObj;  
  myObj.setSalary(50000);  
  cout << myObj.getSalary();  
  return 0;  
}
```
