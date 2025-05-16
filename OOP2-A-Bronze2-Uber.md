# Uber -- Bronze
## Description
- Objective: ให้นักศึกษาเลือกรถ Uber โดยอ้างอิงจาก ราคาค่าโดยสารที่น้อยที่สุด แต่ต้องดูด้วยว่า Uber ไปในระยะที่เราค้องการได้และอยู่ในงบด้วย
- Input(s): 
  - distance ระยะทางที่เราต้องการที่จะไป
  - budget งบประมาณของเรา
  - std::vector<DriverInfo> UberList รายการคนขับ Uber

- Output:  ชื่อคนขับที่คิดค่าโดยสารถูกที่สุด (std::string) ถ้าไม่มีคนขับที่ไปได้ให้คืนเป็นสตริงว่างเปล่า ""
- Function: 
```
        std::string Uber(double distance, double budget, std::vector<DriverInfo> UberList)
```

- Struct
```c++
struct DriverInfo {
  std::string name; // driver's name
  double range;     // km 
  double fee;       // baht/km
};
```

## Examples
`Uber(10,200, std::vector<DriverInfo>{{"Nueng" , 10 , 15},{"Tien" , 20, 18},{"Peemai", 15, 12},{"Ioon", 18 , 16}}) --> "Peemai"`
`Uber(10,100, std::vector<DriverInfo>{{"Nueng" , 10 , 15},{"Tien" , 20, 18},{"Peemai", 15, 12},{"Ioon", 18 , 16}}) --> ""`
`Uber(8,1000, std::vector<DriverInfo>{{"Nueng" , 10 , 15},{"Tien" , 20, 15},{"Peemai", 15, 15},{"Ioon", 18 , 15}}) --> "Nueng"`
หากราคาเท่ากันให้เลือกคนแรกที่ราคาถูกที่สุด

## วิธีการทดสอบ
- สามารถกด run script เพื่อทดสอบกับ test cases ที่เตรียมไว้ให้โดยการรัน `run_eval_windows.ps1` (หรือ `run_eval_mac.sh` สำหรับคนที่ใช้ MacOS) บน terminal ภายใน VSCode (หรือคลิ๊กขวาที่ไฟล์แล้วเลือก `Run Code`)
- ถ้า code สามารถรันได้ จะมีผลลัพธ์แสดงอยู่ใน `result.out` ซึ่งจะแจ้งให้ทราบว่าผ่านหรือไม่ผ่านเทสอะไร
- ถ้าใครติดปัญหาเรื่อง Permission บน Windows ให้รัน `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser` ก่อน
