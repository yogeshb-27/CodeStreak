# 🔢 Count Type of Characters

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/count-type-of-characters3635/1

## 📝 Problem Description
Given a string `S`, count the number of:
- Uppercase characters
- Lowercase characters
- Numeric characters
- Special characters

Return the result as an array:
- `arr[0] = uppercase`
- `arr[1] = lowercase`
- `arr[2] = numeric`
- `arr[3] = special`

## 💡 Approach
- Traverse the string character by character.
- Use ASCII range checks:
    - `'A' to 'Z'` → uppercase
    - `'a' to 'z'` → lowercase
    - `'0' to '9'` → numeric
    - Else → special character
- Maintain counters for each category.

**Why optimal?**
- Single pass over the string ensures **O(n)** time.
- No extra space used apart from counters → **O(1)**.

## 💻 Java Code
```java
class Sol {
    int[] count(String s) {
        int lowercase = 0, uppercase = 0, special = 0, numeric = 0;
        
        for(char c : s.toCharArray()){
            if(c >= 'A' && c <= 'Z')
                uppercase++;
            else if(c >= 'a' && c <= 'z')
                lowercase++;
            else if(c >= '0' && c <= '9')
                numeric++;
            else
                special++;
        }
        
        return new int[]{uppercase, lowercase, numeric, special};
    }
}