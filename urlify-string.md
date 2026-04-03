# URLify a Given String 🔗

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/urlify-a-given-string--141625/1

## 📝 Problem Description
Given a string `s`, replace all spaces in the string with `"%20"` and return the modified string.

## 💡 Approach
- Traverse the string character by character.
- Use a `StringBuilder` to build the result efficiently:
    - If the character is a space, append `"%20"`.
    - Otherwise, append the character as it is.

**Why optimal?**
- Avoids repeated string concatenation (which is costly in Java).
- Runs in linear time using a single pass.

## 💻 Java Code
```java
class Solution {
    String URLify(String s) {
        StringBuilder sb = new StringBuilder();
        
        for(char c : s.toCharArray()){
            if(c == ' ')
                sb.append("%20");
            else
                sb.append(c);
        }
        
        return sb.toString();
    }
}