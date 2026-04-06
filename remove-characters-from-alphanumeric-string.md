# 🔢 Remove Characters from Alphanumeric String

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/remove-characters-from-alphanumeric-string

## 📝 Problem Description
Given a string `s`, remove all non-numeric characters and return a string containing only digits while preserving their original order.

## 💡 Approach
- Traverse the string character by character.
- Use a `StringBuilder` to build the result.
- Append only those characters that are digits (`0-9`).

**Why optimal?**
- Single pass over the string ensures **O(n)** time.
- Efficient string construction using `StringBuilder`.

## 💻 Java Code
```java
class Solution {
    String removeCharacters(String s) {
        StringBuilder sb = new StringBuilder();
        
        for(char c : s.toCharArray()){
            if(Character.isDigit(c))
                sb.append(c);
        }
        
        return sb.toString();
    }
}