# StructList -- Bronze 
## Description
พี่เทียนมี Struct Node ให้น้องๆ โดยใน Node จะประกอบด้วย Address และ Value พี่อยากให้น้องๆทำการเรียง Value ให้ให้ตรงลำดับค่าของ Address โดยให้เรียงตาม Address จากน้อยไปหามาก ซึ่ืงหน้าตาของ Struct Node จะเป็นดังนี้(ไฟล์จะอยู่ใน `base_class.h`)
- Address จะมีค่าไม่ซ้ำกัน แต่ไม่จะเป็นต้องเรียงกันครบทุกตัวนะ
```c++
struct Node
{
    std::string Value;
    int address;
};
```

- Input(s): `std::vector<Node> SList`
- Output: `std::vector<std::string> AnsList`
- Function:
```c++
std::vector<std::string> StructList(const std::vector<Node> &SList);
``` 

### Examples
```
SList => {{"Chicken", 2}, {"Pork", 1}, {"Beef", 3}, {"Fish", 5}, {"Sheep", 4}}
AnsList => {"Pork", "Chicken", "Beef", "Sheep", "Fish"}
```

```cpp
#include <vector>
#include <string>
#include <algorithm>  // สำหรับ std::sort
#include "base_class.h"  // ต้องรวม header ที่มี struct Node
#include "StructList.h"

std::vector<std::string> StructList(const std::vector<Node> &SList) {
    // สร้างสำเนาเพื่อไม่แก้ของเดิม
    std::vector<Node> sortedList = SList;

    // เรียงตาม address จากน้อยไปมาก
    std::sort(sortedList.begin(), sortedList.end(), [](const Node &a, const Node &b) {
        return a.Address < b.Address;
    });

    // เก็บเฉพาะ Value มาเป็นคำตอบ
    std::vector<std::string> AnsList;
    for (const Node &node : sortedList) {
        AnsList.push_back(node.Value);
    }

    return AnsList;
}

```
