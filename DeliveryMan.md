# DeliveryMan -- Bronze

```
วันนี้น้อง ๆ ทำงานเป็นพนักงานขนส่งสินค้าของบริษัทแห่งหนึ่ง ซึ่งได้รับมอบหมายให้ส่งสินค้าตามลำดับที่กำหนดไว้ แต่เกิดข้อผิดพลาดในการบันทึกข้อมูลที่อยู่ โดยรายชื่อผู้รับใน vector ถูกเลื่อนไปจากตำแหน่งเดิม ทำให้น้อง ๆ ต้องปรับรายชื่อกลับให้ตรงกับลำดับที่ถูกต้อง

โดยข้อมูลที่น้อง ๆ จะได้รับ (inputs) มีดังนี้
1. std::vector<std::string> *customers : vector ของ string ในรูปแบบ Pointer ที่ประกอบไปด้วยชื่อผู้รับ 
2. int shift : ตัวเลขจำนวนเต็ม แสดงจำนวนการเลื่อนตำแหน่งของรายชื่อ:
    - หากเป็นบวก (+) หมายถึงเลื่อนไปทางขวา
    - หากเป็นลบ (-) หมายถึงเลื่อนไปทางซ้าย
3. int to_deliver : ตัวเลขจำนวนเต็ม แสดง ตำแหน่ง ของคนที่ต้องไปส่งสินค้า (คนแรกเริ่มนับว่าเป็น 1)

***สิ่งที่ต้องทำ***
1. เขียนฟังก์ชันที่รับข้อมูลดังกล่าว และ return ชื่อของผู้รับสินค้าที่อยู่ในตำแหน่ง to_deliver ที่กำหนด (หลังจากปรับลำดับเรียบร้อย)
2. หากตำแหน่งของชื่อที่ต้องไปส่งน้อยกว่า 1 หรือเกินขนาดของ vector ให้ return เป็น "Wrong Input"
```

## Warning
```
ระวังเรื่องการใส่ Input ด้วย Pointer (Pass By Pointer) ให้ดี น้อง ๆ อาจไม่สามารถเข้าถึงข้อมูลของตัวแปร customers ได้แบบปกติ
```

## Description
- Objective: `<แสดงรายชื่อที่ถูกต้องในการส่งของ โดยปรับลำดับของรายชื่อใน vector ให้ตรงกับลำดับที่ถูกต้องตามจำนวนที่ถูกเลื่อน>`
- Input(s): `<std::vector<std::string> *vecs, int shift, int to_deliver>`
- Output: `<ชื่อของผู้รับสินค้าตามตำแหน่งที่กำหนด (หลังจากปรับลำดับแล้ว)>`
- Function: `<std::string DeliveryMan(std::vector<std::string> *vecs , int shift, int to_deliver)>`


## Examples
```
ex1 = {"Joy","Title","Junggun","Yuth", "Ben"};
Example 1 = DeliveryMan(&ex1,5,2) : Output = "Title"
    *คำอธิบาย* >> shift ไปทางขวา 5 ครั้ง
    - ครั้งที่ 1 : {"Ben", "Joy", "Title", "Junggun", "Yuth"}
    - ครั้งที่ 2 : {"Yuth", "Ben", "Joy", "Title", "Junggun"}
    - ครั้งที่ 3 : {"Junggun", "Yuth", "Ben", "Joy", "Title"}
    - ครั้งที่ 4 : {"Title", "Junggun", "Yuth", "Ben", "Joy"}
    - ครั้งที่ 5 : {"Joy", "Title", "Junggun", "Yuth", "Ben"}
    ต้องไปส่งของให้คนในตำแหน่งที่ 2 คือ "Title" #
    
ex2 = {"Pokpong","Fifa","Baipor","Hertz", "Games", "Gang"};
Example 2 = DeliveryMan(&ex2,2,3) : Output = "Pokpong"
    *คำอธิบาย* >> shift ไปทางขวา 2 ครั้ง
    - ครั้งที่ 1 : {"Gang", "Pokpong","Fifa","Baipor","Hertz", "Games"}
    - ครั้งที่ 2 : {"Games", "Gang", "Pokpong","Fifa","Baipor","Hertz"}
    ต้องไปส่งของให้คนในตำแหน่งที่ 3 คือ "Pokpong" #
```


## วิธีการทดสอบ
- สามารถกด run script เพื่อทดสอบกับ test cases ที่เตรียมไว้ให้โดยการรัน `run_eval_windows.ps1` (หรือ `run_eval_mac.sh` สำหรับคนที่ใช้ MacOS) บน terminal ภายใน VSCode (หรือคลิ๊กขวาที่ไฟล์แล้วเลือก `Run Code`)
- ถ้า code สามารถรันได้ จะมีผลลัพธ์แสดงอยู่ใน `result.out` ซึ่งจะแจ้งให้ทราบว่าผ่านหรือไม่ผ่านเทสอะไร
- ถ้าใครติดปัญหาเรื่อง Permission บน Windows ให้รัน `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser` ก่อน
```cpp
#include <iostream>
#include <vector>
#include <string>

std::string DeliveryMan(std::vector<std::string> *customers, int shift, int to_deliver) {
    if (!customers || customers->empty()) return "Wrong Input";
    int n = customers->size();
    
    if (to_deliver < 1 || to_deliver > n) return "Wrong Input";
    
    // Normalize shift to be within range
    shift = (shift % n + n) % n;  // Ensures shift is positive and within range
    
    // Rotate the vector to the right by `shift`
    std::vector<std::string> rotated(n);
    for (int i = 0; i < n; i++) {
        rotated[(i + shift) % n] = (*customers)[i];
    }
    
    // Return the customer at the given position (1-based index)
    return rotated[to_deliver - 1];
}

int main() {
    std::vector<std::string> ex1 = {"Joy", "Title", "Junggun", "Yuth", "Ben"};
    std::cout << DeliveryMan(&ex1, 5, 2) << std::endl; // Output: "Title"
    
    std::vector<std::string> ex2 = {"Pokpong", "Fifa", "Baipor", "Hertz", "Games", "Gang"};
    std::cout << DeliveryMan(&ex2, 2, 3) << std::endl; // Output: "Pokpong"
    
    return 0;
}

```