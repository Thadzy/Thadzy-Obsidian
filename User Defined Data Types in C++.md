#cpp 
***User defined data types*** are those data types that are defined by the user himself. In C++, these data types allow programmers to extend the basic data types provided and create new types that are more suited to their specific needs. C++ supports 5 user-defined data types:
- [Class](https://www.geeksforgeeks.org/user-defined-data-types-in-c/#1-class)
- [Structure](https://www.geeksforgeeks.org/user-defined-data-types-in-c/#2-structure)
- [Union](https://www.geeksforgeeks.org/user-defined-data-types-in-c/#3-union)
- [Enumeration](https://www.geeksforgeeks.org/user-defined-data-types-in-c/#4-enumeration)
- [Typedef](https://www.geeksforgeeks.org/user-defined-data-types-in-c/#5-typedef)
## Class
A Class is the building block of C++’s Object-Oriented programming paradigm. It is a user-defined data type, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A class is like a blueprint for an object.
```cpp
#include <bits/stdc++.h>
using namespace std;

class GfG {
    // Access specifier
public:
    // Data Member
    string name;
    // Member Function
    void printname() {
        cout << name;
    }
};

int main() {

    // Declare an object of class geeks
    GfG g;
    // Accessing data member
    g.name = "GeeksForGeeks";
    // Accessing member function
    g.printname();
    return 0;
}
```

## Structure
A Structure is a user-defined data type like class. A structure creates a data type that can be used to group items of possibly different types into a single type.

```cpp
#include <iostream>
using namespace std;

// Declaring structure
struct A {
    int i;
    char c;
};

int main() {
    
    // Create an instance of structure
    A a;

    // Initialize structure members
    a.i = 65;
    a.c = 'A';
        
    cout << a.c << ": " << a.i;

    return 0;
}
```

## Union
Like structures , [***union***](https://www.geeksforgeeks.org/cpp-unions/) is also user-defined data type used to group data of different type into a single type. But in union, all members share the same memory location.
```cpp
#include <iostream>
using namespace std;

// Declaration of union is same as the structures
union A {
    int i;
      char c;
};

int main() {
    // A union variable t
    A a;
  
      // Assigning value to c, i will also
      // assigned the same
    a.c = 'A';
    
    cout << "a.i: " << a.i << endl;
      cout << "a.c: " << a.c;

    return 0;
}
```
## Enumeration
[***Enumeration***](https://www.geeksforgeeks.org/enumeration-enum-c/) (or enum) is a user-defined data type in C++ mainly used to assign names to integral constants, the names make a program easy to read and maintain.
```cpp
#include <iostream>
using namespace std;

// Declaring enum
enum Week { Mon, Tue, Wed, Thur, Fri, Sat, Sun };

int main() {
  
      // Creating enum variable
    enum Week day;

      // Assigning value to the variabe
    day = Wed;

    cout << day;
    return 0;
}
```

## Typedef and Using
C++ allows you to define explicitly new data type names by using the keywords [**typedef***](https://www.geeksforgeeks.org/typedef-in-cpp/) or [**using**](https://www.geeksforgeeks.org/using-keyword-in-cpp-stl/). They do not create a new data class, rather, defines a name for an existing type. This can increase the portability (the ability of a program to be used across different types of machines; i.e., mini, mainframe, micro, etc; without many changes to the code) of a program as only the typedef statements would have to be changed.
```cpp
#include <iostream>
using namespace std;

// Using typedef to define a new name for existing type
typedef float f;

// Using 'using' to define a new name for existing type
using integer = int;

int main() {
    // Declaring variables using new type names
    f x = 3.14;
    integer y = 42;

    cout << "Float Value: " << x << endl;
    cout << "Integer Value: " << y;

    return 0;
}
```