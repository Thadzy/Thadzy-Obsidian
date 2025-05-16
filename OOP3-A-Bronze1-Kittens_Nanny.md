# KittensNanny -- Bronze

วันนี้น้อง ๆ รับบทเป็นพี่เลี้ยงแมวหนึ่งวัน น้อง ๆ มีหน้าที่จัดสรรบ้านที่เหมาะสมที่สุดสำหรับการรับเลี้ยงแมว โดยจะมีข้อมูลที่เกี่ยวข้องทั้งหมด 2 structs ดังนี้ (สามารถดูการประกาศได้ใน `base_class.h`)
```cpp
// ข้อมูลของน้องแมว
struct Cat {
  int age;            // years
  double weight;      // kg
  std::string habits; // separate by ','
  std::string home;   // initial with ""
};

// ข้อมูลของบ้านสำหรับน้องแมว
struct Home {
  std::string owner; // name
  double area;       // m^2
  bool hasGarden;    // boolean
};
```

ในการเลือกบ้านให้น้องแมว จะต้องเลือกโดยอิงจากกฎ ดังนี้
1. แมวหนึ่งตัวมีได้หลายนิสัย แต่ถ้าแมวมีนิสัย "anxious", "irritated", หรือ "frightened" (แม้แต่นิสัยเดียว) พื้นที่บ้านต้องมีมากกว่า 100 ตารางเมตรเป็นอย่างน้อย แต่ถ้าแมวมีนิสัย "friendly", "relaxed" หรือ "trusting" พื้นที่บ้านจะต้องมากกว่า 50 ตารางเมตร 
2. แมวที่มีสัดส่วนไม่เหมาะสมต้องการมีสวนเพื่อวิ่งเล่น โดยให้คิดสัดส่วนของแมวจากสูตร (%) = (weight/age)*10 หากคำนวณแล้วมากกว่า 50 % แปลว่าแมวต้องการสวน
3. หากเจอบ้านที่ตรงทั้งสองเงื่อนไข ให้อัพเดต .home ของแมวเป็นชื่อ owner ของบ้านที่เหมาะสมที่สุด แต่
    - หากบังเอิญเจอบ้านที่เหมาะสมเหมือนกัน ให้เลือกบ้านหลังที่พื้นนี้กว้างกว่าเสมอ
    - จะไม่เจอกรณีที่เหมาะสมเหมือนกันแล้วพื้นที่บ้านเท่ากัน
    - หากไม่พบบ้านใดที่เหมาะสมเลย ให้เติมคำว่า "None" ลงไปในช่อง .home

## Suggestion
```
หากน้อง ๆ ใช้คำสั่ง string.find("substring") != std::string::npos อาจสามารถช่วยประหยัดเวลาน้อง ๆ ได้ (มีความหมายว่า "หากใน string ไม่พบ substring ตัวที่ตามหา")
```

## Description
- Objective: `<จงหาบ้านที่เหมาะสมที่สุดสำหรับแมว>`
- Input(s): `<Cat kitten, std::vector<Home> homes>`
- Output: `<Cat ที่อัพเดต home>`
- Function: `<Cat KittensNanny(Cat kitten, std::vector<Home> homes) >`

## Examples
```
example 1 : input ->Cat = {2, 4.5, "anxious,playful,trusting", ""}
                    Home = {{"Rick", 50.0, true}, {"Morty", 200.0, false}}
        - แมวมีนิสัย anxious, playful, trusting จะเห็นว่ามีนิสัย anxious ยังไง area ก็ต้องมากกว่า 100 ตรม.
        - แมวมีสัดส่วน (4.5/2)*10 = 22.5 ยังไม่มากกว่า 50 แปลว่าไม่จำเป็นต้องมีสวน

        # Output {2, 4.5, "anxious,playful,trusting", "Morty"} 

example 2 : input ->Cat = {2, 6.5, "playful,trusting", ""}
                    Home = {{"Summer", 100, true}, {"Beth", 200, false}, {"Jerry", 50, true}}
        - แมวมีนิสัย playful, trusting ทำให้ area ก็ต้องมากกว่า 50 ตรม.
        - แมวมีสัดส่วน (ุ6.5/2)*10 = 32.5 ยังไม่มากกว่า 50 แปลว่าไม่จำเป็นต้องมีสวน
        เมื่อทั้ง Summer และ Beth เหมาะสมหมด ฉะนั้นต้องตอบ Beth ที่มี area มากกว่า
        # Output {2, 6.5, "playful,trusting", "Beth"} 
```

```cpp

```
