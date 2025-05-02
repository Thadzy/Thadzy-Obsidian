---
tags:
  - Cpp
  - OOP
date: 2025-05-01
---
## Introduction 
Object-Oriented Programming is about writing procedures or functions that perform operations on the data, while object-oriented programming is about creating objects that contain both data and functions. 
![[Pasted image 20250501154730.png]]
>What is the variable_ the "_" after the variable in private opp in cpp what does it means?

In C++ (especially in **Object-Oriented Programming**, or OOP), using a trailing underscore (e.g., `variable_`) in **private member variables** is a **naming convention**, not a language feature. It has **no functional meaning to the compiler**, but it serves an important purpose for **code readability and maintainability**.

### Meaning of `variable_` (trailing underscore)
- `variable_` indicates that the variable is a **private member of a class**.
- It helps distinguish member variables from local variables or parameters, especially in constructors or setters.

```cpp
class Person {
private:
    std::string name_;  // private member variable
public:
    Person(const std::string& name) {
        name_ = name; // clearly assigns the parameter to the member
    }
};
```

```cpp
Person(const std::string& name) {
    this->name = name; // use of this-> required to avoid name conflict
}
```

|Signature|Meaning|Efficiency|
|---|---|---|
|`std::string name`|Passed by value → copied|❌ slow|
|`std::string& name`|Passed by reference, modifiable|⚠️ risky|
|`const std::string& name`|Passed by reference, **read-only** (✔ preferred)|✅ efficient|
