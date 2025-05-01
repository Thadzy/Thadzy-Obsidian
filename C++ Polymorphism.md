---
tags:
  - Cpp
  - OOP
date:
---
## Introduction 
Polymorphism means "many forms", and it occurs when we have many classes that are related to each other by inheritance.
lets us inherit attributes and methods from another class. 
**Polymorphism** uses those methods to perform different tasks. This allows us to perform a single action in different ways.
```cpp
// Base class  
class Animal {  
  public:  
    void animalSound() {  
      cout << "The animal makes a sound \n";  
    }  
};  
  
// Derived class  
class Pig : public Animal {  
  public:  
    void animalSound() {  
      cout << "The pig says: wee wee \n";  
    }  
};  
  
// Derived class  
class Dog : public Animal {  
  public:  
    void animalSound() {  
      cout << "The dog says: bow wow \n";  
    }  
};
```
