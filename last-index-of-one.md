# 🔍 Last Index of One

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/last-index-of-15847/1

## 📝 Problem Description
Given a binary string `s` consisting only of `'0'` and `'1'`, find the last index of `'1'`.

Return `-1` if `'1'` is not present in the string.

## 💡 Approach
- Traverse the string from right to left.
- As soon as a `'1'` is found, return its index.
- If no `'1'` is found, return `-1`.

**Why optimal?**
- Starts from the end, so it finds the answer early in many cases.
- Single traversal ensures **O(n)** time with **O(1)** space.

## 💻 Java Code
```java
class Solution {
    public int lastIndex(String s) {
        for(int i = s.length() - 1; i >= 0; i--){
            if(s.charAt(i) == '1')
                return i;
        }
        return -1;
    }
}