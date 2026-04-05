# 🧹 Remove Spaces

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/remove-spaces0128/1

## 📝 Problem Description
Given a string `s`, remove all the spaces from the string and return the modified string while preserving the order of characters.

## 💡 Approach
- Traverse the string character by character.
- Use a `StringBuilder` to construct the result:
    - Append only non-space characters.
- Skip all spaces during traversal.

**Why optimal?**
- Single pass over the string → **O(n)**.
- Avoids costly string concatenation by using `StringBuilder`.

## 💻 Java Code
```java
class Solution {
    String removeSpaces(String s) {
        StringBuilder sb = new StringBuilder();
        
        for(char c : s.toCharArray())
            if(c != ' ')
                sb.append(c);
        
        return sb.toString();
    }
}