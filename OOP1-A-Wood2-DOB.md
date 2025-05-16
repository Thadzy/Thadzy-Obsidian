```cpp
#include "dob.h"
#include <iostream>

// struct DateOfBirth {
//   std::string name;
//   int birth_year;
//   int birth_month;
//   int birth_date;
// };

DateOfBirth DoB(std::string name, std::string date_of_birth) {
    DateOfBirth dob;
    
    dob.name = name;
    dob.birth_date = std::stoi(date_of_birth.substr(0, 2));
    dob.birth_month = std::stoi(date_of_birth.substr(3, 2));
    dob.birth_year = std::stoi(date_of_birth.substr(6, 9));

    return dob;
}
```

