# 🔤 Remove Vowels from String

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/remove-vowels-from-string1446/1

## 📝 Problem Description
Given a string `s`, remove all vowels from the string and return the modified string while preserving the order of remaining characters.

## 💡 Approach
- Traverse the string character by character.
- Maintain a collection of vowels.
- Use a `StringBuilder`:
    - Append only those characters which are not vowels.

**Why optimal?**
- Single traversal ensures **O(n)** time.
- Efficient string construction using `StringBuilder`.

## 💻 Java Code
```java
class Solution {
    String removeVowels(String s) {
        StringBuilder sb = new StringBuilder();
        ArrayList<Character> vowels = new ArrayList<>(
            Arrays.asList('A','E','I','O','U','a','e','i','o','u')
        );

        for(char c : s.toCharArray()){
            if(!vowels.contains(c))
                sb.append(c);
        }

        return sb.toString();
    }
}