```cpp
#include "dna_linked_list.h"
#include <vector>
#include <unordered_map>
#include <algorithm>

// #pragma once
// #include "base_class.h"

// class DNALinkedList {
// public:
//   DNALinkedList() = default;
//   DNALinkedList(const std::string &s);

//   DNANode *header() { return header_; }
//   DNANode *tail() { return tail_; }
//   int length() { return length_; }
//   char GetPair(char c);
//   void AddDNABase(char c);
//   bool isPalindrome();
//   bool CanFormPalindrome();                          
//   void MakePalindrome();

// private:
//   DNANode *header_ = nullptr; // โหนดแรกของลิงค์ลิสต์ DNA
//   DNANode *tail_ = nullptr;   // โหนดสุดท้ายของลิงค์ลิสต์ DNA
//   int length_ = 0;            // ความยาวของลิงค์ลิสต์ DNA
// };

// 1. สร้างลิงค์ลิสต์จาก string ที่รับเข้ามา โดยแปลงแต่ละตัวอักษรเป็นคู่ฐาน (base pair)
DNALinkedList::DNALinkedList(const std::string &s) {
  for (char c : s) {
    char pair = GetPair(c);  // เรียกใช้ฟังก์ชันแปลงคู่ฐาน
    AddDNABase(pair);        // เพิ่มฐานที่แปลงแล้วเข้าไปในลิงค์ลิสต์
  }
}

// 1.1. แปลงตัวอักษร DNA ให้เป็นคู่ของมัน: A<->T, C<->G
char DNALinkedList::GetPair(char c) {
  switch (c) {
    case 'A': return 'T';
    case 'T': return 'A';
    case 'C': return 'G';
    case 'G': return 'C';
    default:  return c; // ถ้าไม่ใช่ A/T/C/G ให้คืนค่าตัวเดิม
  }
}

// 1.2. เพิ่มโหนดตัวใหม่เข้าไปในลิงค์ลิสต์แบบต่อท้าย
void DNALinkedList::AddDNABase(char c) {
  DNANode* newNode = new DNANode{c, nullptr, nullptr}; // สร้างโหนดใหม่
  if (!header_) {
    header_ = tail_ = newNode; // ถ้าเป็นโหนดแรก
  } else {
    tail_->next = newNode;
    newNode->prev = tail_;     // เชื่อมโยงแบบสองทาง
    tail_ = newNode;           // อัปเดตโหนดสุดท้าย
  }
  length_++; // เพิ่มความยาว
}

// 2. เช็คว่าลิงค์ลิสต์นี้เป็นพาลินโดรมหรือไม่ (อ่านจากหน้าไปหลังแล้วเหมือนอ่านจากหลังไปหน้า)
bool DNALinkedList::isPalindrome() {
  DNANode* left = header_;
  DNANode* right = tail_;
  while (left && right && left != right && left->prev != right) {
    if (left->base != right->base)
      return false; // ถ้าฐานไม่ตรงกัน ไม่ใช่พาลินโดรม
    left = left->next;
    right = right->prev;
  }
  return true;
}

// 3. เช็คว่าลิงค์ลิสต์นี้สามารถจัดเรียงใหม่ให้เป็นพาลินโดรมได้หรือไม่
bool DNALinkedList::CanFormPalindrome() {
  std::unordered_map<char, int> freq;
  DNANode* node = header_;
  while (node) {
    freq[node->base]++; // นับความถี่ของแต่ละฐาน
    node = node->next;
  }

  int oddCount = 0;
  for (const auto& pair : freq) {
    if (pair.second % 2 != 0)
      oddCount++; // ถ้ามีฐานที่จำนวนคี่เกิน 1 ตัว จะจัดเป็นพาลินโดรมไม่ได้
  }
  return oddCount <= 1;
}

// 4. จัดเรียงลิงค์ลิสต์ให้กลายเป็นพาลินโดรมที่เรียงตามลำดับตัวอักษร
void DNALinkedList::MakePalindrome() {
  if (isPalindrome()) return; // ถ้าเป็นอยู่แล้วไม่ต้องทำอะไร

  std::unordered_map<char, int> freq;
  DNANode* node = header_;
  while (node) {
    freq[node->base]++;
    node = node->next;
  }

  std::vector<char> half;
  char midChar = '\0';
  for (auto& [c, count] : freq) {
    for (int i = 0; i < count / 2; ++i)
      half.push_back(c); // เพิ่มแต่ละครึ่งหนึ่งของคู่
    if (count % 2 == 1)
      midChar = c;       // ถ้ามีจำนวนคี่ เก็บไว้ตรงกลาง
  }

  std::sort(half.begin(), half.end());
  std::vector<char> fullList = half;
  if (midChar != '\0') fullList.push_back(midChar);
  for (auto it = half.rbegin(); it != half.rend(); ++it)
    fullList.push_back(*it); // เติมครึ่งหลังกลับด้าน

  // เขียนค่าใหม่ลงในลิงค์ลิสต์เดิม
  node = header_;
  for (char c : fullList) {
    node->base = c;
    node = node->next;
  }
}
```