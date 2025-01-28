#cpp
# main() function
The main function **serves as the starting point for program execution**
```cpp
#include <iostream>
#include <vector>
#include <cmath>
#include <iomanip>
#include <ctime>

int main(){

	return 0;
}
```

# Input and output using std::cin and std::cout
The std is **a short form of standard**, the std namespace contains the built-in classes and declared functions.
```cpp
 std::cout << "I like picture" << "\n";
```

# Getline
The C++ ***getline()*** is a standard library function that is used to read a string or a line from an input stream.
```cpp
#include <iostream>
#include <string>
using namespace std;

int main()
{
    string str;

    cout << "Please enter your name: \n";
    getline(cin, str);
    cout << "Hello, " << str
         << " welcome to GfG !\n";

    return 0;
}
```

https://www.youtube.com/watch?v=wpDSWDbGXrQ