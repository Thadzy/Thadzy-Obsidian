#cpp 
The data types that are derived from the primitive or built-in datatypes are referred to as Derived Data Types. They are generally the data types that are created from the primitive data types and provide some additional functionality.
## Arrays
An array is a collection of items stored at continuous memory locations. The idea of array is to represent many variables using a single name. The below example demonstrates the use of array in C++.
```cpp
#include <iostream>
using namespace std;

int main() {

    // Array Derived Type
    int arr[5] = {1, 2, 3, 4, 5};
    arr[0] = 5;
    arr[2] = -10;
    arr[3] = arr[0];

      // Printing the data
    for (int i = 0; i < 5; i++)
          printf("%d ", arr[i]);

    return 0;
}
```

## Pointers
**Pointers** are symbolic representation of addresses. They can be said as the variables that can store the address of another variable as its value. The below example demonstrates the use of pointer in C++.
```cpp
#include <iostream>
using namespace std;

int main() { 
    int var = 20;

    // Pointers Derived Type
    // declare pointer variable
    int* ptr;

    // note that data type of ptr
    // and var must be same
    ptr = &var;

    // assign the address of a variable
    // to a pointer
    cout << "Value at ptr = " << ptr << endl;
    cout << "Value at var = " << var << endl;
    cout << "Value at *ptr = " << *ptr;
  
      return 0;
}
```
### Output
``` 
Value at ptr = 0x7fffa5bef2cc
Value at var = 20
Value at *ptr = 20
```

## References 
When a variable is declared as reference, it becomes an alternative name for an existing variable. A variable can be declared as reference by putting ‘&’ in the declaration.
```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 10;

    // Reference Derived Type
    // ref is a reference to x.
    int& ref = x;

    // Value of x is now changed to 20
    ref = 20;
    cout << "x = " << x << endl;

    // Value of x is now changed to 30
    x = 30;
    cout << "ref = " << ref << endl;

    return 0;
}
```