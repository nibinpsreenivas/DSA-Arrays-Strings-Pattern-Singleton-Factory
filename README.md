# 🚀 Week 1 – DSA & Design Patterns (C++)

Welcome to Week 1 of the C++ Interview Prep Series.  
This week focuses on **Arrays & Strings** in DSA, and two essential design patterns: **Singleton** and **Factory**.

---

## ✅ Topics Covered

### 📘 DSA – Arrays & Strings

| Concept | Description |
|--------|-------------|
| Two Pointers | Used for comparing elements in a sequence from both ends. |
| Sliding Window | Used to find subarrays with specific conditions efficiently. |
| Prefix Sum | Helps answer range sum queries in O(1) time. |
| Frequency Count | Count characters or numbers using maps or arrays. |
| In-place Modifications | Rearranging data without extra space. |

---

### 🔗 Practice Problems (LeetCode)

| Problem | Topic | Difficulty | Link |
|--------|-------|------------|------|
| Two Sum | Hash Map | Easy | [Link](https://leetcode.com/problems/two-sum/) |
| Best Time to Buy and Sell Stock | Sliding Window | Easy | [Link](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) |
| Longest Substring Without Repeating Characters | Sliding Window + Map | Medium | [Link](https://leetcode.com/problems/longest-substring-without-repeating-characters/) |
| Move Zeroes | Two Pointers | Easy | [Link](https://leetcode.com/problems/move-zeroes/) |
| Find Pivot Index | Prefix Sum | Easy | [Link](https://leetcode.com/problems/find-pivot-index/) |

---

## 🧠 Design Patterns in C++

### 🔧 1. Singleton Pattern
Ensure a class has only one instance and provide a global access point to it.

#### 📌 Use Case:
- Logging system
- Configuration manager
- DICOM tag registry

#### 🧑‍💻 C++ Example:
```cpp
class Singleton {
private:
    static Singleton* instance;
    Singleton() {}
public:
    static Singleton* getInstance() {
        if (!instance)
            instance = new Singleton();
        return instance;
    }
    void log(const std::string& msg) {
        std::cout << "Log: " << msg << std::endl;
    }
};
Singleton* Singleton::instance = nullptr;
