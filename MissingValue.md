#cpp #coding #Medium 
# MissingValue -- Bronze
## Description
พี่ได้ไปเก็บข้อมูลคะแนนจากกลุ่มตัวอย่างที่เป็นนักศึกษามา แต่ดูเหมือนว่าจะมีข้อมูลบางส่วนหายไป(เขียนแทนด้วย -1) อยากให้น้องๆช่วยเขียนโปรแกรมในการเติมข้อมูลส่วนที่ขาดหายไปให้พี่หน่อย โดยวิธีการเติมข้อมูลมีอยู่สองวิธีคือ `Mean` และ `Median`
`Mean` หรือค่าเฉลี่ย วิธีนี้จะนำค่าอื่นมาเฉลี่ยกันและนำไปแทนข้อมูลที่หายไป
`Median` หรือมัธยฐาน วิธีนี้จะนำข้อมูลอื่นมาเรียงและหาค่ากลาง

`**ในการคำนวณค่า Mean และ Median ให้ปัดเศษทิ้งเสมอ เช่นคำนวณได้ 30.8 ให้ใช้ 30**`

** สามารถ Sort(จากน้อยไปมาก) ได้ด้วยการเรียกฟังก์ชัน `void Sort(std::vector<int>* vec_to_sort);` หรือสามารถใช้ Sort วิธีอื่นได้เช่นกัน **

- Objective: เขียนโปรแกรมเพื่อช่วยพี่เติมค่าข้อมูลที่ขาดหายไป
- Input(s): `(vector<int> *, string)` - (ข้อมูลที่พี่เก็บมา, วิธีที่ต้องการใช้)
- Output: `void`
- Function: `void MissingValue(vector<int> *data, string mode)`

## Examples
- Input : `({10,30,-1,40,45,-1},"Median")` => Output : `{10, 30, 35, 40, 45, 35}`
- Input : `({10,30,-1,40,45,-1},"Mean")` => Output : `{10, 30, 31, 40, 45, 31}`

## วิธีการทดสอบ
- สามารถกด run script เพื่อทดสอบกับ test cases ที่เตรียมไว้ให้โดยการรัน `run_eval_windows.ps1` (หรือ `run_eval_mac.sh` สำหรับคนที่ใช้ MacOS) บน terminal ภายใน VSCode (หรือคลิ๊กขวาที่ไฟล์แล้วเลือก `Run Code`)
- ถ้า code สามารถรันได้ จะมีผลลัพธ์แสดงอยู่ใน `result.out` ซึ่งจะแจ้งให้ทราบว่าผ่านหรือไม่ผ่านเทสอะไร
- ถ้าใครติดปัญหาเรื่อง Permission บน Windows ให้รัน `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser` ก่อน

```cpp
#include <vector>
#include <string>
#include <algorithm>
#include <numeric>
#include <cmath>

void Sort(std::vector<int>* vec_to_sort) {
    std::sort(vec_to_sort->begin(), vec_to_sort->end());
}

void MissingValue(std::vector<int> *data, std::string mode) {
    std::vector<int> valid_values;
    
    // Collect valid values (excluding -1)
    for (int num : *data) {
        if (num != -1) {
            valid_values.push_back(num);
        }
    }
    
    int replacement_value = 0;
    
    if (mode == "Mean") {
        int sum = std::accumulate(valid_values.begin(), valid_values.end(), 0);
        replacement_value = sum / valid_values.size(); // Truncate decimal part
    } else if (mode == "Median") {
        Sort(&valid_values);
        int size = valid_values.size();
        if (size % 2 == 1) {
            replacement_value = valid_values[size / 2];
        } else {
            replacement_value = (valid_values[size / 2 - 1] + valid_values[size / 2]) / 2;
        }
    }
    
    // Replace -1 with calculated value
    for (int &num : *data) {
        if (num == -1) {
            num = replacement_value;
        }
    }
}

```