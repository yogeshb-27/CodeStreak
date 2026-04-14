# 🐪 Count of Camel Case Characters

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/find-the-camel3348/1

## 📝 Problem Description
Given a string `s`, count the number of **Camel Case characters** (uppercase letters) present in the string.

## 💡 Approach
- Traverse the string character by character.
- Check if a character lies between `'A'` and `'Z'`.
- Increment the count whenever an uppercase character is found.

**Why optimal?**
- Single pass over the string ensures **O(n)** time.
- No extra space required → **O(1)**.

## 💻 Java Code
```java
class Sol {
    int countCamelCase(String s) {
        int count = 0;
        
        for(char c : s.toCharArray()){
            if(c >= 'A' && c <= 'Z')
                count++;
        }
        
        return count;
    }
}