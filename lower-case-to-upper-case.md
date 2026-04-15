# 🔠 Lower Case to Upper Case

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/lower-case-to-upper-case3410/1

## 📝 Problem Description
Given a string `str` containing only lowercase letters, convert all characters to uppercase and return the resulting string.

## 💡 Approach
- Traverse the string character by character.
- Convert each lowercase character to uppercase using:
    - ASCII conversion (`c - 'a' + 'A'`) OR
    - Built-in method like `Character.toUpperCase()`.
- Build the result using `StringBuilder`.

**Why optimal?**
- Single traversal ensures **O(n)** time.
- No extra complex operations required.

## 💻 Java Code
```java
class Solution {
    public String to_upper(String str) {
        StringBuilder sb = new StringBuilder();
        
        for(char c : str.toCharArray()){
            sb.append(Character.toUpperCase(c));
        }
        
        return sb.toString();
    }
}