---
tags:
  - Cpp
  - OOP
date: 2025-05-02
---
## Introduction 
## Get Memory Address and Value
we used the pointer variable to get the memory address of a variable (used together with the `&` **reference** operator). However, you can also use the pointer to get the value of the variable, by using the `*` operator (the **dereference** operator):
```cpp
string food = "Pizza";  // Variable declaration  
**string* ptr = &food;**    // Pointer declaration  
  
// Reference: Output the memory address of food with the pointer (0x6dfed4)  
cout << ptr << "\n";  
  
// Dereference: Output the value of food with the pointer (Pizza)  
cout << *ptr << "\n";
```

## Modify the Pointer Value
```cpp
string food = "Pizza";  
string* ptr = &food;  
  
// Output the value of food (Pizza)  
cout << food << "\n";  
  
// Output the memory address of food (0x6dfed4)  
cout << &food << "\n";  
  
// Access the memory address of food and output its value (Pizza)  
cout << *ptr << "\n";  
  
// Change the value of the pointer  
*ptr = "Hamburger";  
  
// Output the new value of the pointer (Hamburger)  
cout << *ptr << "\n";  
  
// Output the new value of the food variable (Hamburger)  
cout << food << "\n";
```

Output : 
```
Pizza  
0x6dfed4  
Pizza  
Hamburger  
Hamburger
```