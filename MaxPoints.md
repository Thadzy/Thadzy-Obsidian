#cpp #coding #hard
## Description

พวกพี่ๆกำลังเล่นเกมที่มีรูปแบบการคิดคะแนนด้วยการนำเลขสองตัวมาคูณกัน (A x B) ซึ่งมีกติกาดังนี้
- A และ B จะมีค่าพื้นฐานคือ `base_a`, `base_b` 
- จะมีลิสต์ของโบนัส (`bonuses`) ที่จะนำมาคำนวณร่วมกับ `base_a` และ `base_b` เพื่อหาคะแนนสุดท้าย
- ค่า `bonus` จะเป็น string ซึ่งประกอบไปด้วยตัวเลขและตัวอักษรบ่งบอกประเภท โดยโบนัสจะมีทั้งหมด 3 ประเภทได้แก่
    - `a` นำไปรวมกับ ค่าปัจจุบันของ A (เริ่มต้นด้วย base_a) มีค่าเป็นจำนวนเต็ม
    - `b` นำไปรวมกับ ค่าปัจจุบันของ B (เริ่มต้นด้วย base_b) มีค่าเป็นจำนวนเต็มที่ไม่ติดลบ
    - `m` นำไปคูณกับ ค่าปัจจุบันของ B (เริ่มต้นด้วย base_b) มีค่าเป็นจำนวนเต็มที่ไม่ติดลบ
    - ตัวอย่าง:
        - `3a` คือ เพิ่ม A ไป 3 (`A = A+3`)
        - `2m` คือ คูณค่าปัจจุบันของ B ด้วย 2 (`B = B * 2`)
- โบนัสจะทำการคำนวณไปทีละตัวตามลำดับในลิสต์ (vector) ยกตัวอย่างเช่น
    - `base_a = 10, base_b = 2`
    - `bonus = {"2b", "3m", "10b", "10a"}`
    - ผลลัพธ์ (ถ้าไม่มีการแก้ไขลำดับเลย)
        - `A = base_a + 10 = 20`
        - `B = ((base_b + 2) * 3) + 10 = 22`
        - `point = A * B = 440`
- โบนัสแต่ละตัวในลิสต์สามารถมีมากกว่าหนึ่งประเภทและแต่ละประเภทมีมากกว่า 1 ตัวได้ ซึ่งการนำไปคิดคะแนนของโบนัสแถวนั้นจะทำทีละประเภทโดยเริ่มจากทำ `a` ทั้งหมดก่อนแล้วตามด้วย `b` ทั้งหมด แล้วจึงทำ `m` ทั้งหมด
    - ตัวอย่าง: `"5b3m2b4a"` มีค่าเสมือนว่าเป็น `"4a5b2b3m"` นั่นคือจะทำการเพิ่มค่า A ไป 4 แล้วตามด้วย เพิ่มค่า B ไป 5+2 = 7 แล้วจึงคูณค่า B ด้วย 3

อยากให้น้องๆช่วยพี่เขียนโปรแกรมเพื่อหาคะแนนที่สูงที่สุดที่เป็นไปได้จากการสลับลำดับของโบนัสในลิสต์ที่ให้มา

- Objective: `เขียนโปรแกรมเพื่อหาคะแนนที่สูงที่สุดที่เป็นไปได้จากการสลับลำดับของโบนัสในลิสต์ที่ให้มา`
- Input(s): `std::vector<const std::string *> bonuses, int base_a, int base_b`
- Output: `double`
- Function: `double MaxPoints(std::vector<const std::string *> bonuses, int base_a, int base_b)`

## Useful commands
- `std::stoi(s)` แปลง string เป็น integer (แต่สตริงต้องมีแต่ตัวเลขนะ)
- สามารถนำสตริงมาต่อกันได้ด้วยเครื่องหมาย `+` เช่น `"12" + "3" => "123"`
- `string substr (size_t pos, size_t len) const;` ใช้ในการดึงบางส่วนของสตริงออกมาเป็นสตริงใหม่เช่น
    - สมมติว่ามี `s = "132abc";` 
    - `s.substr(0,3); => "132"`
    - `s.substr(2,2); => "2a`
- `std::reverse()` สามารถใช้ในการกลับด้านสมาชิกใน vector ได้ เช่น 
    - `vector<int> v{1,2,3};`
    - `std::reverse(v.begin(), v.end()); => v = {3,2,1}` 
    - แต่อย่าลืมใส่ `#include<algorithm>` ก่อนใช้งานนะ
 
## Examples
### Ex1:
- `bonuses = {3a, 4b, 5m}, base_a = 10, base_b = 2`
- `output = 390`

### Ex2:
- `bonuses = {10a, 4b10a, 5m2b}, base_a = 30, base_b = 4`
- `output = 2500`

## วิธีการทดสอบ
- สามารถกด run script เพื่อทดสอบกับ test cases ที่เตรียมไว้ให้โดยการรัน `run_eval_windows.ps1` (หรือ `run_eval_mac.sh` สำหรับคนที่ใช้ MacOS) บน terminal ภายใน VSCode (หรือคลิ๊กขวาที่ไฟล์แล้วเลือก `Run Code`)
- ถ้า code สามารถรันได้ จะมีผลลัพธ์แสดงอยู่ใน `result.out` ซึ่งจะแจ้งให้ทราบว่าผ่านหรือไม่ผ่านเทสอะไร
- ถ้าใครติดปัญหาเรื่อง Permission บน Windows ให้รัน `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser` ก่อน
```cpp
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <regex>

double MaxPoints(std::vector<const std::string*> bonuses, int base_a, int base_b) {
    int A = base_a;
    int B = base_b;
    std::vector<int> a_list, b_list, m_list;

    // แยกค่าของโบนัสออกเป็นประเภท a, b, m
    std::regex pattern(R"((\d+)([abm]))");
    for (const auto& bonus_ptr : bonuses) {
        std::string bonus = *bonus_ptr;
        std::sregex_iterator it(bonus.begin(), bonus.end(), pattern);
        std::sregex_iterator end;
        while (it != end) {
            int value = std::stoi((*it)[1]);
            char type = (*it)[2].str()[0];
            if (type == 'a') a_list.push_back(value);
            else if (type == 'b') b_list.push_back(value);
            else if (type == 'm') m_list.push_back(value);
            ++it;
        }
    }

    // เรียงลำดับเพื่อให้ได้คะแนนสูงสุด
    std::sort(a_list.begin(), a_list.end(), std::greater<int>());
    std::sort(b_list.begin(), b_list.end(), std::greater<int>());
    std::sort(m_list.begin(), m_list.end(), std::greater<int>());

    // คำนวณคะแนน
    for (int a : a_list) A += a;
    for (int b : b_list) B += b;
    for (int m : m_list) B *= m;

    return static_cast<double>(A) * B;
}

int main() {
    std::vector<const std::string*> bonuses1 = {new std::string("3a"), new std::string("4b"), new std::string("5m")};
    std::cout << MaxPoints(bonuses1, 10, 2) << std::endl; // 390

    std::vector<const std::string*> bonuses2 = {new std::string("10a"), new std::string("4b10a"), new std::string("5m2b")};
    std::cout << MaxPoints(bonuses2, 30, 4) << std::endl; // 2500

    // ลบหน่วยความจำที่จองไว้
    for (auto ptr : bonuses1) delete ptr;
    for (auto ptr : bonuses2) delete ptr;

    return 0;
}

```