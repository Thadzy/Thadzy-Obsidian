cpp 
## First Method:- Using Float precision
```cpp
#include<bits/stdc++.h>
using namespace std;

int main()
{
    float var = 37.66666;

    // Directly print the number with .2f precision
    cout << fixed << setprecision(2) << var; 
    return 0;
}

// This code is contributed by shivanisinghss2110
```
## Second Method: Using integer typecast If we are in Function then how return two decimal point value

```cpp
#include <iostream>
using namespace std;
float round(float var)
{
    // 37.66666 * 100 =3766.66
    // 3766.66 + .5 =3767.16    for rounding off value
    // then type cast to int so value is 3767
    // then divided by 100 so the value converted into 37.67
    float value = (int)(var * 100 + .5);
    return (float)value / 100;
}

int main()
{
    float var = 37.66666;
    cout << round(var);
    return 0;
}
```
## Third Method: using sprintf() and sscanf() 
```cpp
#include <iostream>
using namespace std;
float round(float var)
{
    // we use array of chars to store number
    // as a string.
    char str[40]; 

    // Print in string the value of var 
    // with two decimal point
    sprintf(str, "%.2f", var);

    // scan string value in var 
    sscanf(str, "%f", &var); 

    return var; 
}

int main()
{
    float var = 37.66666;
    cout << round(var);
    return 0;
}
```

## Assign to variable
```cpp
#include <iostream>
#include <cmath>

int main() {
    double num = 3.14159;
    double roundedNum = std::round(num * 100) / 100; // Rounds to 2 decimal places

    std::cout << "Rounded Number: " << roundedNum << std::endl;
    return 0;
}

```

```cpp
#include <iostream>
#include <iomanip>

int main() {
    double num = 3.14159;
    std::cout << std::fixed << std::setprecision(2) << "Rounded Number: " << num << std::endl;
    return 0;
}

```

```cpp
#include <iostream>
#include <sstream>
#include <iomanip>

int main() {
    double num = 3.14159;
    std::stringstream stream;
    stream << std::fixed << std::setprecision(2) << num;
    double roundedNum;
    stream >> roundedNum; // Extract the rounded value as a double

    std::cout << "Rounded Number: " << roundedNum << std::endl;
    return 0;
}

```