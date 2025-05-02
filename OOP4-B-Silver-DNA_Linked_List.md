---
tags:
  - Cpp
  - OOP
date: 2025-05-02
---
## README
# DNALinkedList -- Silver

## Description
วันนี้น้อง ๆ ในฐานะวิศวกรกำลังศึกษาดูงานเกี่ยวกับ Genetic Engineering นั่นคือการตัดต่อพันธุกรรมเพื่อพัฒนาสิ่งมีชีวิตที่สมบูรณ์ที่สุด แต่เขาว่ากันว่าโครงสร้าง DNA ที่สมบูรณ์ที่สุดคือโครงสร้างที่อยู่ในลักษณะ Palindrome... ดังนั้นวันนี้น้อง ๆ จะมาเขียนโปรแกรมตัดต่อพันธุกรรมกัน
DNALinkedList เป็นโครงสร้างที่เกิดจากการต่อกันของ DNANodes โดยจะถูกเชื่อมกันเป็นลำดับด้วยเทคโนโลยี Doubly Linked List (Linked List 2 ทางมีถัดไปและก่อนหน้า) ซึ่ง DNANode แต่ละตัวมีรูปแบบดังนี้
```cpp

struct DNANode {

    char base;

    DNANode* next;

    DNANode* prev;

};

```

```
แต่ในการที่จะสร้าง DNALinkedList ขึ้นมาได้นั้น, น้อง ๆ จะต้องเริ่มต้นจากการนำ string ที่ประกอบไปด้วยพยัญชนะภาษาอังกฤษพิมพ์ใหญ่ มาดัดแปลงตามกฎต่อไปนี้:

    1. Contructor(std::string s) แปลง string ที่ได้รับให้อยู่ในลักษณะของ Linked list เช่น "XYX" เป็น 'X'->'Y'->'X' โดยมีรายละเอียดดังนี้
        1.1. ก่อนการแปลงเป็น Linked list จะต้องทำการสลับค่าของ DNA บางตัว ด้วยการใช้ฟังก์ชัน GetPair
            - char GetPair(char c) เป็นฟังก์ชันแปลงคู่เบส หาก char ที่พบเป็น 'A', 'T', 'C' หรือ 'G' โดยจะแปลง char นั้น ให้เป็นคู่ตรงข้าม คือ แปลง ('A' เป็น 'T'), ('T' เป็น 'A'), ('C' เป็น 'G') หรือ ('G' เป็น C)
        1.2. สร้าง Linked List ด้วยฟังก์ชัน AddDNABase (เพิ่ม char ที่แปลงจาก 1.1 เข้า Linked list)
            - void AddDNABase(char c) เป็นฟังก์ชันสำหรับการแปลงแต่ละ char ใน string ให้อยู่ในรูปของ DNANode เพื่อเชื่อมต่อกันเป็น Linked list ด้วยการเพื่ม DNANode ของ char ใด ๆ เข้าที่ tail ของ Linked list

    2. bool IsPalindrome() ตรวจสอบว่า Linked list เป็น Palindrome หรือไม่

    3. bool CanFormPalindrome() ตรวจสอบว่า Linked list สามารถเรียงใหม่ให้อยู่ในลักษณะ Palindrome ได้หรือไม่

    4. void MakePalindrome() หาก Linked List ยังไม่เป็น Palindrome ให้ทำการจัดเรียงข้อมูลภายใน Linked list ใหม่ให้อยู่ในลักษณะของ Palindrome โดยให้เรียงลำดับ DNANode จากน้อยไปมากด้วยค่าของ base ตามลำดับ ASCII ในครึ่งซ้าย เช่น "ZZYYXX" -> "XYZZYX"

    (ครึ่งซ้าย=น้อยไปมาก, ตรงกลาง=ตัวที่เป็นคี่, ครึ่งขวา=มากไปน้อย)
```
## Warning
```
- ต้องแปลงคู่เบสด้วย GetPair() ก่อนสร้าง Linked List ทุกครั้ง

- การเรียงลำดับใน MakePalindrome() จะเกิดขึ้นในกรณีที่ยังไม่เป็น Palindrome เท่านั้นและต้องเป็นไปตามลำดับ ASCII

- แต่ละ function จะมีอธิบายเพิ่มเติมใน dna_linked_list.h
```
## Examples

```
Example 1 (Basic) : input = "XTXTY"
    // CONSTRUCTOR + GetPair + AddDNABase
    DNALinkedList s(input);
    -> switch bases first = "XAXAY"
    Expected : s.header()->base = 'X'
               s.header()->next->base = 'A'
               s.header()->next->next->base = 'X'
               s.header()->next->next->next->base = 'A'
               s.header()->next->next->next->next->base = 'Y'

Example 2 (Advance) : input = "TACOCAT"
    // Constructor + GetPair + AddDNABase
    DNALinkedList s(input);
    -> switch bases first = "ATGOGTA"
    Expected : s.header()->base = 'A'
               s.header()->next->base = 'T'
               s.header()->next->next->base = 'G'
               s.header()->next->next->next->base = 'O'
               s.header()->next->next->next->next->base = 'G'
               s.header()->next->next->next->next->next->base = 'T'
               s.header()->next->next->next->next->next->next->base = 'A'

    // IsPalindrome
    s.IsPalindrome();
    Expected : true
    // CanFormPalindrome
    s.CanFormPalindrome();
    Expected : true
    // MakePalindrome
    s.MakePalindrome();
    Expected : s.header()->base = 'A'
               s.header()->next->base = 'T'
               s.header()->next->next->base = 'G'
               s.header()->next->next->next->base = 'O'
               s.header()->next->next->next->next->base = 'G'
               s.header()->next->next->next->next->next->base = 'T'
               s.header()->next->next->next->next->next->next->base = 'A'
    (Linked List เหมือนเดิมเพราะเป็น Palindrome อยู่แล้ว)
    ; หากตัวอย่างไม่ได้เป็น Palindrome อยู่แล้ว ลำดับ Linked List ก็จะแค่เรียงใหม่
```

# Baseclass.h
```cpp
#pragma once
#include <vector>
#include <string>
struct DNANode {
    char base; // Character of one base
    DNANode* next; // Pointer to the next base
    DNANode* prev; // Pointer to the previous base
};
```
# dna_linked_list.h
```cpp
#pragma once
#include "base_class.h"

class DNALinkedList {
public:
// Default constructor
DNALinkedList() = default;
DNALinkedList(const std::string& s);
DNANode* header() { return header_; }
DNANode* tail() { return tail_; }
int length() { return length_; }
char GetPair(char c);
void AddDNABase(char c);
bool isPalindrome();
bool CanFormPalindrome();
void MakePalindrome();

private:
    DNANode* header_ = nullptr;  // Pointer to first node in DNA Linked List
    DNANode* tail_ = nullptr;    // Pointer to last node in DNA Linked List
    int length_ = 0;             // Number of bases (nodes) in the DNA Linked List
};
```
# dna_linked_list.cpp

