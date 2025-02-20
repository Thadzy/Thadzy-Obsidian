#cpp #Coding #Hard
# MusicPlaylist -- Silver
## Description
อาจารย์รับงานช่วยเขียนโปรแกรมเพื่อสร้าง playlist มา โดยผู้ใช้จะให้รายชื่อเพลงทั้งหมดที่มี (all_songs), ชื่อเพลงที่ชอบ (selected_song), และจำนวนเพลงที่ต้องการ (n) โดยมีข้อกำหนดว่าให้สร้าง playlist โดยใช้เพลงใน all_songs ที่มีความใกล้เคียงกับ selected_song มากที่สุด n ลำดับแรก โดยมีการเปรียบเทียบด้วยเกณฑ์ดังนี้ (เรียงจากสำคัญมากที่สุดไปน้อยที่สุด)
   1. ชื่อตรงกันเป๊ะ
   2. มีจำนวนสระ {a,e,i,o,u} เหมือนกัน และเรียงตรงกัน
   3. จำนวนของสระใน {a,e,i,o,u} ที่มีจำนวนเท่ากัน เช่น `love` และ `have` มี จำนวน {e, i, u} เท่ากัน และ {a, u} ไม่เท่ากัน
   4. มีจำนวนสระ {a,e,i,o,u} รวมเท่ากัน
   5. มีความยาวของชื่อเท่ากัน (รวมสัญลักษณ์และช่องว่าง)
   6. ลำดับของเพลงในลิสต์เทียบกับลำดับแรก โดยการคิดลำดับจะเลื่อนไปด้านหน้าเท่านั้น และเมื่อไปถึงตำแหน่งสุดท้ายของลิสต์แล้วจะวนไปที่ตำแหน่งแรก

### Notes
- `selected_song` จะอยู่ใน `all_songs` เสมอ
- ให้ถือว่าตัวพิมพ์ใหญ่และพิมพ์เล็กมีค่าเหมือนกัน (not case sensitive) และในโจทย์จะไม่มีตัวพิมพ์ใหญ่
- ถ้า n มากกว่าจำนวนเพลงใน `all_songs` ให้คืนค่าแค่เพลงเท่าที่มี (ไม่ต้องใส่ซ้ำ)
- `size()` สามารถใช้เช็คจำนวนตัวอักษรใน string ได้ เช่น ถ้ามี `std::string s;`, สามารถใช้ `s.size()` ได้
- สามารถใช้ for loop ในการเช็คตัวอักษรแต่ละตัวใน string ได้


### Summary
- Objective: `สร้าง playlist จากเพลงที่กำหนด`
- Input(s): `std::vector<const std::string *> all_songs, std::string selected_song, int n`
- Output: `std::vector<std::string>`
- Function: `std::vector<std::string> MusicPlaylist(std::vector<const std::string *> all_songs, std::string selected_song, int n)`

## Examples
### Ex1:
- `all_songs: {"dynamite", "butter", "life goes on", "how you like that", "ddu-du ddu-du", "kill this love", "apt", "rockstar", "pink venom", "moonlit floor"}`
- `selected_song: "pink venom"`
- `n = 3`
- `Output: {"pink venom", "kill this love", "dynamite"}`

### Ex2:
- `all_songs: {"my love", "fool again", "no no", "close", "walk away", "rewind"}`
- `selected_song: "my love"`
- `n = 2`
- `Output: {"my love", "close"}`

## วิธีการทดสอบ
- สามารถกด run script เพื่อทดสอบกับ test cases ที่เตรียมไว้ให้โดยการรัน `run_eval_windows.ps1` (หรือ `run_eval_mac.sh` สำหรับคนที่ใช้ MacOS) บน terminal ภายใน VSCode (หรือคลิ๊กขวาที่ไฟล์แล้วเลือก `Run Code`)
- ถ้า code สามารถรันได้ จะมีผลลัพธ์แสดงอยู่ใน `result.out` ซึ่งจะแจ้งให้ทราบว่าผ่านหรือไม่ผ่านเทสอะไร
- ถ้าใครติดปัญหาเรื่อง Permission บน Windows ให้รัน `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope CurrentUser` ก่อน

```cpp
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <unordered_map>
// Helper function to count vowels and store order
std::pair<std::unordered_map<char, int>, std::string> count_vowels(const std::string &song) {
    std::unordered_map<char, int> vowel_count;
    std::string vowel_order;
    std::string vowels = "aeiou";
    
    for (char c : song) {
        if (vowels.find(c) != std::string::npos) {
            vowel_count[c]++;
            vowel_order.push_back(c);
        }
    }
    return {vowel_count, vowel_order};
}

// Function to calculate similarity score
int calculate_score(const std::string &song1, const std::string &song2) {
    if (song1 == song2) return 100000; // Exact match highest priority
    
    auto [vowel_count1, vowel_order1] = count_vowels(song1);
    auto [vowel_count2, vowel_order2] = count_vowels(song2);
    
    int score = 0;
    if (vowel_order1 == vowel_order2) score += 5000; // Same vowel order
    
    int matching_vowel_count = 0;
    int total_vowel_count1 = 0, total_vowel_count2 = 0;
    
    for (char v : "aeiou") {
        if (vowel_count1[v] == vowel_count2[v]) matching_vowel_count++;
        total_vowel_count1 += vowel_count1[v];
        total_vowel_count2 += vowel_count2[v];
    }
    
    score += matching_vowel_count * 100; // Matching vowel counts
    if (total_vowel_count1 == total_vowel_count2) score += 50; // Total vowel count match
    if (song1.size() == song2.size()) score += 10; // Same length
    
    return score;
}

std::vector<std::string> MusicPlaylist(std::vector<const std::string *> all_songs, std::string selected_song, int n) {
    std::vector<std::pair<int, std::string>> scored_songs;
    
    for (const std::string *song : all_songs) {
        scored_songs.push_back({calculate_score(*song, selected_song), *song});
    }
    
    std::sort(scored_songs.begin(), scored_songs.end(), [](auto &a, auto &b) {
        return a.first > b.first; // Sort by descending score
    });
    
    std::vector<std::string> playlist;
    for (int i = 0; i < std::min(n, (int)scored_songs.size()); ++i) {
        playlist.push_back(scored_songs[i].second);
    }
    
    return playlist;
}

// Example usage
int main() {
    std::vector<const std::string *> all_songs = {
        new std::string("dynamite"),
        new std::string("butter"),
        new std::string("life goes on"),
        new std::string("how you like that"),
        new std::string("ddu-du ddu-du"),
        new std::string("kill this love"),
        new std::string("apt"),
        new std::string("rockstar"),
        new std::string("pink venom"),
        new std::string("moonlit floor")
    };
    
    std::string selected_song = "pink venom";
    int n = 3;
    
    std::vector<std::string> playlist = MusicPlaylist(all_songs, selected_song, n);
    
    for (const auto &song : playlist) {
        std::cout << song << std::endl;
    }
    
    for (auto song : all_songs) delete song; // Cleanup allocated memory
    
    return 0;
}

```