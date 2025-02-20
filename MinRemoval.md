#cpp #coding
```cpp
#include <iostream>
#include <string>
#include <algorithm>

int MinRemoval(const std::string& binary) {
    int count_ones = 0, min_removals = 0;
    
    for (char c : binary) {
        if (c == '1') {
            count_ones++;
        } else {
            min_removals = std::min(min_removals + 1, count_ones);
        }
    }
    
    return min_removals;
}

int main() {
    std::cout << MinRemoval("01011") << std::endl;  // Output: 1
    std::cout << MinRemoval("101000001") << std::endl;  // Output: 2
    std::cout << MinRemoval("1111") << std::endl;  // Output: 0
    std::cout << MinRemoval("0000") << std::endl;  // Output: 0
    return 0;
}
```