#cpp #Coding #Medium 
# Chopsticks -- Bronze 
## Description
- Objective: `พี่เทียนนั่งว่างแล้วเกิดอยากเล่นตะเกียบขึ้นมา โดยที่พี่เทียนจะมีตะเกียบอยู่ทั้งหมด n คู่ ซึ่งในตะเกียบหนึ่งคู่นั้นจะประกอบไปด้วยตะเกียบที่มีความยาว l_i เท่ากันทั้งหมดสองข้าง แต่พี่เทียนไม่ได้มีตะเกียบอยู่แค่อันเดียว พี่เทียนมีตะเกียบอยู่หลายคู่ พี่เทียนเลยอยากรู้ว่า ถ้าเอาตะเกียบทั้งหมดสองคู่จากตะเกียบที่มีมาทำสี่เหลี่ยม จะได้สี่เหลี่ยมที่ใหญ่ที่สุดกี่ตารางหน่วยกันนะ`

- Input(s):
    - n จำนวนคู่ของตะเกียบ [2, 100]
    - array_l ความยาวของตะเกียบแต่ละคู่เป็น Array โดยตะเกียบจะมีค่าความยาวตั้งแต่ [1, 10^9]
- Output: ` A พื้นที่ที่ใหญ่ที่สุดจากตะเกียบที่พี่มี`
- Function: `int Chopstick(int n, int array_l[])`

## Examples
- Input: `3, {1, 2, 3}` ==> Output: `6`
- Input: `4, {1, 3, 3, 7}` ==> Output: `21`

## วิธีการทดสอบ
- สามารถกด run script เพื่อทดสอบกับ test cases ที่เตรียมไว้ให้โดยการรัน `run_eval_windows.ps1` (หรือ `run_eval_mac.sh` สำหรับคนที่ใช้ MacOS) บน terminal ภายใน VSCode (หรือคลิ๊กขวาที่ไฟล์แล้วเลือก `Run Code`)
- ถ้า code สามารถรันได้ จะมีผลลัพธ์แสดงอยู่ใน `result.out` ซึ่งจะแจ้งให้ทราบว่าผ่านหรือไม่ผ่านเทสอะไร
- ถ้าใครติดปัญหาเรื่อง Permission บน Windows ให้รัน `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser` ก่อน

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