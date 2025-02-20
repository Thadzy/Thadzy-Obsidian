#cpp #coding 
```cpp
#include <iostream>
#include <vector>
#include <unordered_map>

std::vector<int> SeenTwice(const std::vector<std::vector<int>>& num) {
    std::vector<int> result;
    
    for (const auto& row : num) {
        std::unordered_map<int, int> freq;
        
        // นับจำนวนครั้งที่แต่ละตัวเลขปรากฏในแถว
        for (int n : row) {
            freq[n]++;
        }
        
        // ตรวจหาตัวเลขที่ปรากฏสองครั้งพอดี และเก็บตามลำดับที่เจอ
        for (int n : row) {
            if (freq[n] == 2) {
                result.push_back(n);
                freq[n] = 0; // ป้องกันการเพิ่มตัวเลขเดิมซ้ำ
            }
        }
    }
    
    return result;
}

int main() {
    std::vector<std::vector<int>> input1 = {{1,2,2,4,3}, {3,1,1,3,3}};
    std::vector<int> output1 = SeenTwice(input1);
    for (int num : output1) std::cout << num << " ";
    std::cout << std::endl;
    
    std::vector<std::vector<int>> input2 = {{9,8,8,9,10}, {6,6,5,5,4}, {1,1,1,1,1}};
    std::vector<int> output2 = SeenTwice(input2);
    for (int num : output2) std::cout << num << " ";
    std::cout << std::endl;
    
    return 0;
}
```