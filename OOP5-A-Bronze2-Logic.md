---
tags:
  - Cpp
  - OOP
date: 2025-05-02
---
## README
# Logic -- Bronze
## Description
- Objective: ให้น้องๆช่วยพี่ทีเอเขียนคลาส LogicTools ให้เรียบร้อย โดย class นี้จะถูกสร้างด้วยค่าเริ่มต้น 1 ค่า (`a`) แล้วนำมาเก็บไว้ใน `data_` และภายในคลาสจะมีคำสั่งหลักคือ Operate ซึ่งจะทำการคำนวณค่าทางตรรกะระหว่างข้อมูลที่มีอยู่กับข้อมูลที่รับเข้ามา (`b`) ด้วยชุดค่าสำสั่งใน `cmd` ซึ่งประกอบไปด้วย `{"OR", "AND"}` แล้วนำข้อมูลมาเก็บไว้ใน `data_`

พี่ทีเอเขียนฟังก์ชัน Operate ไว้ให้เรียบร้อยแล้วแต่ว่ายังไม่ได้เขียนฟังก์ชันย่อยของคลาส LogicTools ดังนี้

```cpp
  // returns string representing data_ AND b
  std::string AND(std::string b);

  // returns string representing data_ OR b
  std::string OR(std::string b);
```

- ---
### Input Example

a = "1001"  

b = "0110"  

cmd = {"OR", "AND"}
### ขั้นตอนการคำนวณ
เริ่มต้นด้วยค่า `a = "1001"`
คำสั่งแรกใน `cmd` คือ "OR"  
ทำการ OR ระหว่าง `a` กับ `b`: ผลลัพธ์หลังจากการ OR: `a = "1111"`
คำสั่งถัดไปใน `cmd` คือ "AND"  
ทำการ AND ระหว่าง `a` (ที่อัปเดตแล้ว) กับ `b`: ผลลัพธ์หลังจากการ AND: `a = "0110"`
### หมายเหตุ
- `a` และ `b` ต้องมีความยาวเท่ากัน
- รองรับคำสั่ง `OR` และ `AND` เท่านั้นใน `cmd`
- ทุกคำสั่งใน `cmd` จะอัปเดตค่า `a` ตามลำดับ
- Function:
```cpp
class LogicTools {
public:
  // constructor รับค่าตั้งต้นมาเก็บไว้ใน data_
  LogicTools(std::string init);
  // Getter for data_
  std::string data() const { return data_; }
  // returns string representing data_ AND b
  std::string AND(std::string b);
  // returns string representing data_ OR b
  std::string OR(std::string b);
  // Operate function (Do not need to modify this function)
  void Operate(std::string b, const std::vector<std::string>& cmd);
private:
  std::string data_;
};

```

## Examples

`a = 1001, b = 0110 , cmd {"AND"} -> a = 0000`

`a = 1001, b = 0110 , cmd {"OR"}  -> a = 1111`

# Logic.cpp
```cpp
#include "Logic.h"
#include <iostream>
LogicTools::LogicTools(std::string a) {
  // add constructor code here
  data_ = a;
}
std::string LogicTools::AND(std::string b) {
  // add code here
  std::string AND = "";
  for(int i = 0;i < data_.size(); i++){
    if(data_[i] == '1' && b[i] == '1'){
      AND += '1';
    }
    else{
      AND += '0';
    }
  }
  return AND;
}
std::string LogicTools::OR(std::string b) {
  // code here
  std::string OR = "";
  for(int i = 0;i < data_.size(); i++){
    if(data_[i] == '1' || b[i] == '1'){
      OR += '1';
    }
    else{
      OR += '0';
    }
  }
  return OR;

}

// Operate function (Do not need to modify this function)
void LogicTools::Operate(std::string b, const std::vector<std::string>& cmd) {
  for (const auto &command : cmd) {
    if (command == "AND") {
      data_ = AND(b);
    } else if (command == "OR") {
      data_ = OR(b);
    }
  }
}

  

//a = 1001, b = 0110 , cmd {"AND"} -> a = 0000 a = 1001, b = 0110 , cmd {"OR"}  -> a = 1111

// int main() {

//   std::string a = "1001";

//   std::string b = "0110";

//   std::vector<std::string> cmd1 = {"AND"};

//   std::vector<std::string> cmd2 = {"OR"};

  

//   LogicTools tool(a);

  

//   // Test AND

//   tool.Operate(b, cmd1);

//   std::cout << "Result after AND: " << tool.data() << std::endl;

  

//   // Reinitialize tool

//   tool = LogicTools(a);

  

//   // Test OR

//   tool.Operate(b, cmd2);

//   std::cout << "Result after OR: " << tool.data() << std::endl;

  

//   return 0;

// }
```
