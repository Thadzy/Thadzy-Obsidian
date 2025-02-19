#cpp 
## Introduction
Vector is the array that can resize and must have the same type
```cpp
#include <vector>
```
## Create a vector
```cpp
vector<string> cars;
```
## Loop through vector
```cpp 
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
   
for (string car : cars) {  
  cout << car << "\n";  
}
```
## Access a vector
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
  
cout << cars[0];  // Outputs Volvo  
cout << cars[1];  // Outputs BMW
```
### Also can access at back and front
```cpp 
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"};  
  
cout << cars.front();  
cout << cars.back();
```
### And specific
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"}; 

cout << cars.at(1);   
cout << cars.at(2);
```
### Change a Vector Element
```cpp
vector<string> cars = {"Volvo", "BMW", "Ford", "Mazda"}; 

cars[0] = "Opel";  
cout << cars[0];  // Now outputs Opel instead of Volvo
```




