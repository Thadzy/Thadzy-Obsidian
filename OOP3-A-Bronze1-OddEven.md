# OddEven -- Bronze

## Description

- Objective: `ให้น้องช่วยพี่ๆทีเอสร้าง class OddEvenTools ที่ช่วยทำการแยกเลขคู่และเลขคี่ออกจากกัน โดยจะแบ่งเก็บใน vector 2 ตัวที่เป็นประเภท private โดยให้ลำดับเรียงตามข้อมูลที่เข้ามา และน้องๆต้องช่วยเขียน getter อีกสองตัวคือ get_odd_numbers() และ get_even_numbers() สำหรับการอ่านค่าด้วยนะ`

## Function:

```cpp

class OddEvenTools

{

public:

// Constructor

OddEvenTools(const std::vector<int> &n);

  

// function that return vector of odd numbers

std::vector<int> get_odd_numbers() const;

// function that return vector of even numbers

std::vector<int> get_even_numbers() const;

  

private:

std::vector<int> odd_numbers_;

std::vector<int> even_numbers_;

};

```

  

## Examples

```cpp

Input: {5,6,7,8,9,10,11,12}

Output: get_odd_numbers() = {5,7,9,11} , get_even_numbers = {6,8,10,12}

```

  
```cpp

```