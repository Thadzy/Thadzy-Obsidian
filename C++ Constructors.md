---
tags:
  - Cpp
  - OOP
date: 2025-05-01
---
## Introduction 
A constructor in C++ is a **special method** **that is automatically called when an object of a class is created.**
```cpp
class MyClass {     // The class  
  public:           // Access specifier  
    MyClass() {     // Constructor  
      cout << "Hello World!";  
    }  
};  
  
int main() {  
  MyClass myObj;    // Create an object of MyClass (this will call the constructor)  
  return 0;  
}
```

