# 🔤 Convert a List of Characters into a String

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/convert-a-list-of-characters-into-a-string5142/1

## 📝 Problem Description
Given a character array `arr[]` of size `N`, combine all characters to form a single string.

## 💡 Approach
- Use a `StringBuilder` to efficiently construct the string.
- Traverse the character array and append each character to the builder.

**Why optimal?**
- Single traversal ensures **O(n)** time.
- `StringBuilder` avoids costly string concatenation.

## 💻 Java Code
```java
class Solution {
    public String chartostr(char arr[], int N) {
        StringBuilder sb = new StringBuilder();
        
        for(char c : arr)
            if(c != ' ')
                sb.append(c);
        
        return sb.toString();
    }
}