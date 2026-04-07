# 🔍 Check String

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/check-string1818/1

## 📝 Problem Description
Given a string `s`, check whether all characters in the string are the same.

Return `true` if all characters are identical, otherwise return `false`.

## 💡 Approach
- Use a `HashSet` to store unique characters.
- Traverse the string:
    - Add each character to the set.
    - If the set size becomes greater than 1, return `false`.
- If traversal completes with only one unique character, return `true`.

**Why optimal?**
- Stops early if more than one unique character is found.
- Single pass ensures **O(n)** time.

## 💻 Java Code
```java
class Sol {
    Boolean check(String s) {
        Set<Character> chars = new HashSet<>();
        
        for(char c : s.toCharArray()){
            chars.add(c);
            if(chars.size() > 1)
                return false;
        }
        
        return true;
    }
}