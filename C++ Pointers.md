---
tags:
  - Cpp
  - OOP
date: 2025-05-02
---
## Introduction 
A **pointer** however, is a variable that **stores the memory address as its value**.
A pointer variable points to a data type (like `int` or `string`) of the same type, and is created with the `*` operator. The address of the variable you're working with is assigned to the pointer:
```cpp
string food = "Pizza";  // A food variable of type string  
string* ptr = &food;    // A pointer variable, with the name ptr, that stores the address of food  
  
// Output the value of food (Pizza)  
cout << food << "\n";  
  
// Output the memory address of food (0x6dfed4)  
cout << &food << "\n";  
  
// Output the memory address of food with the pointer (0x6dfed4)  
cout << ptr << "\n";
```
Create a pointer variable with the name `ptr`, that **points to** a `string` variable, by using the asterisk sign `*` (`string* ptr`). Note that the type of the pointer has to match the type of the variable you're working with.
Use the `&` operator to store the memory address of the variable called `food`, and assign it to the pointer.
Now, `ptr` holds the value of `food`'s memory address.

```
There are three ways to declare pointer variables, but the first way is preferred:
string* mystring; // Preferred  
string *mystring;  
string * mystring;
```

[[C++ Dereference]]