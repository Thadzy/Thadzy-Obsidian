#cpp #coding #Medium 
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int Chopstick(int n, std::vector<int>& array_l) {
    if (n < 2) return 0;
    
    // Sort in descending order
    std::sort(array_l.begin(), array_l.end(), std::greater<int>());
    
    int max_area = 0;
    int first = 0, second = 0;
    
    for (size_t i = 0; i < array_l.size() - 1; ++i) {
        if (array_l[i] == array_l[i + 1]) {
            if (first == 0) {
                first = array_l[i];
            } else {
                second = array_l[i];
                break;
            }
            ++i;  // Skip next element since it's used already
        }
    }
    
    if (first > 0 && second > 0) {
        max_area = first * second;
    }
    
    return max_area;
}

int main() {
    std::vector<int> array_l = {1, 3, 3, 7};
    int n = array_l.size();
    std::cout << Chopstick(n, array_l) << std::endl;
    return 0;
}

```