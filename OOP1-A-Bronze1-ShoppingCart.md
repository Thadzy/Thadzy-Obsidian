# ShoppingCart -- Bronze

## Description

พี่เต็งได้ไปรับงานช่วยเขียนโปรแกรมเพื่อคำนวณราคารวมของสินค้าในตะกร้าให้แก่ร้านสะดวกซื้อแห่งหนึ่ง ซึ่งทางร้านมีโปรแกรมสแกนสินค้าในตะกร้าอยู่แล้วและจะให้ค่าข้อมูลของสินค้าแต่ละประเภทในตะกร้าออกมาในรูปแบบของ struct ที่มีชื่อว่า ItemInfo

  

โดย ItemInfo มีการประกาศดังนี้ (สามารถกดเข้าไปดูได้ใน `dependencies/include/base_class.h`)

```C++

struct ItemInfo {

std::string id; // item`s ID

double unit_price; // price per unit (exclude VAT)

int count; // number of this item in the cart

};

```

  

และสินค้าทั้งหมดในตะกร้าจะถูกจัดเก็บเป็นเวคเตอร์ของ ItemInfo เพื่อนำมาคำนวณราคารวม

  

แต่ว่าราคาของสินค้ายังไม่ได้รวม `VAT`เลย ซึ่งการคิด `VAT` จะขึ้นอยู่กับประเภทของสินค้า โดยร้าน minimart นี้ใช้หลักการว่าสินค้าทุกชนิดยกเว้นอาหารจะต้องคิด `VAT 7%` ส่วนอาหารไม่มี `VAT` และสามารถตรวจสอบว่าสินค้าเป็นอาหารหรือไม่โดยการเช็ค ID ซึ่ง ID ของอาหารจะต้องมีอย่างน้อย 6 หลักและขึ้นต้นด้วย 5,6, หรือ 7 เท่านั้น

- Objective: `เขียนโปรแกรมเพื่อหาคำนวณราคารวมของสินค้าในตะกร้า`

- Input(s): `std::vector<ItemInfo> items`

- Output: `double`

- Function: `double ShoppingCart(const std::vector<ItemInfo>& items);`

  

## Examples

  

```

Example1

Items: {{"10000", 10, 10}, {"10003", 20, 5}} // {non-food, non-food}

Total Price: (10*10)+(20*5) = 200 + VAT(=200*0.07) => 214

```

  

```

Example2

Items: {{"500001", 1000, 3}, {"600001", 100, 5}} // {food, food}

Total Price: (1000*3)+(100*5) = 3500 (no VAT) => 3500

```

  

