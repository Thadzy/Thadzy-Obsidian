```cpp
#include "bmi.h"
#include "base_class.h"
#include <iostream>

double BMI(PersonalInfo Info) {
  double w = Info.weight;
  double h = Info.height;
  double h2 = Info.height * Info.height;

  double BMI = w/h2 * 10000;

  return BMI;
}

// int main() {
//   PersonalInfo p = {"Thadzy", 1997, 25, 100};

//   std::cout << "  Name: " << p.name << "\n";
//   std::cout << "  BirthYear: " << p.birth_year << "\n";
//   std::cout << "  Height: " << p.height << "\n";
//   std::cout << "  Weight: " << p.weight << "\n";
//   std::cout << "  BMI : " << BMI(p) << '\n';  // Fixed line
// }

```