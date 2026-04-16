# 🔢 Check for Binary String

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/check-for-binary/1

## 📝 Problem Description
Given a non-empty string `s`, check whether it is a **binary string** (contains only `'0'` and `'1'`).

Return `true` if the string is binary, otherwise return `false`.

## 💡 Approach
- Traverse the string character by character.
- Check if each character is either `'0'` or `'1'`.
- If any character is not valid, return `false`.
- If all characters are valid, return `true`.

**Why optimal?**
- Single pass over the string ensures **O(n)** time.
- Early exit improves performance.

## 💻 Java Code
```java
class Solution {
    boolean isBinary(String s) {
        for(char c : s.toCharArray()){
            if(c != '0' && c != '1')
                return false;
        }
        
        return true;
    }
}