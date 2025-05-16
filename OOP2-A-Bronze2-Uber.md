
```cpp
#include "Uber.h"

std::string Uber(double distance, double budget,
                    std::vector<DriverInfo> UberList) {
    std::string best_driver = "";
    double min_total_cost =
        std::numeric_limits<double>::max(); // กำหนดค่าเริ่มต้นให้แพงที่สุด

    for (const auto &driver : UberList) {
        if (driver.range >= distance) {
        double total_cost = driver.fee * distance;
        if (total_cost <= budget && total_cost < min_total_cost) {
            min_total_cost = total_cost;
            best_driver = driver.name;
        }
        }
    }

    return best_driver;
}

// int main() {
//     std::vector<DriverInfo> drivers1 = {
//         {"Nueng", 10, 15},
//         {"Tien", 20, 18},
//         {"Peemai", 15, 12},
//         {"Ioon", 18, 16}
//     };

//     std::vector<DriverInfo> drivers2 = drivers1; // same set for second test
//     std::vector<DriverInfo> drivers3 = {
//         {"Nueng", 10, 15},
//         {"Tien", 20, 15},
//         {"Peemai", 15, 15},
//         {"Ioon", 18, 15}
//     };

//     std::cout << "Test Case 1: " << Uber(10, 200, drivers1) << std::endl; // Expected: Peemai
//     std::cout << "Test Case 2: " << Uber(10, 100, drivers2) << std::endl; // Expected: (empty)
//     std::cout << "Test Case 3: " << Uber(8, 1000, drivers3) << std::endl; // Expected: Nueng

//     return 0;
// }
```