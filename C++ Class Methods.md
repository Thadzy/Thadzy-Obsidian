---
tags:
  - Cpp
  - OOP
date: 2025-05-01
---
## Introduction 
Methods are **functions** that belongs to the class.
There are two ways to define functions that belongs to a class:
- Inside class definition
- Outside class definition
In the following example, we define a function inside the class, and we name it "`myMethod`".
### Inside Example
```cpp
class MyClass {        // The class  
  public:              // Access specifier  
    void myMethod() {  // Method/function defined inside the class  
      cout << "Hello World!";  
    }  
};  
  
int main() {  
  MyClass myObj;     // Create an object of MyClass  
  myObj.myMethod();  // Call the method  
  return 0;  
}
```
### Outside Example
```cpp
class MyClass {        // The class  
  public:              // Access specifier  
    void myMethod();   // Method/function declaration  
};  
  
// Method/function definition outside the class  
void MyClass::myMethod() {  
  cout << "Hello World!";  
}  
  
int main() {  
  MyClass myObj;     // Create an object of MyClass  
  myObj.myMethod();  // Call the method  
  return 0;  
}
```
To define a function outside the class definition, you have to declare it inside the class and then define it outside of the class. This is done by specifiying the name of the class, followed the scope resolution `::`operator, followed by the name of the function:
## Parameters
```cpp
#include <iostream>  
using namespace std;  
  
class Car {  
  public:  
    int speed(int maxSpeed);  
};  
  
int Car::speed(int maxSpeed) {  
  return maxSpeed;  
}  
  
int main() {  
  Car myObj; // Create an object of Car  
  cout << myObj.speed(200); // Call the method with an argument  
  return 0;  
}
```
