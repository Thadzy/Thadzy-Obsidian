---
tags:
  - Cpp
  - OOP
date: 2025-05-01
---
## Introduction 
In C++, it is possible to inherit attributes and methods from one class to another. We group the "inheritance concept" into two categories:
- **derived class (child) - the class that inherits from another class**
- **base class (parent) - the class being inherited from**
To inherit from a class, use the `:` symbol.
```cpp
// Base class  
class Vehicle {  
  public:  
    string brand = "Ford";  
    void honk() {  
      cout << "Tuut, tuut! \n" ;  
    }  
};  
  
// Derived class  
class Car: public Vehicle {  
  public:  
    string model = "Mustang";  
};  
  
int main() {  
  Car myCar;  
  myCar.honk();  
  cout << myCar.brand + " " + myCar.model;  
  return 0;  
}
```

Output :
```
Tuut, tuut!  
Ford Mustang
```

>Why And When To Use "Inheritance"?
>>It is useful for code reusability: reuse attributes and methods of an existing class when you create a new class.

