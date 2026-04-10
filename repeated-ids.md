# 🔁 Repeated IDs

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/repeated-ids0116/1

## 📝 Problem Description
Given an array `arr` of single-digit employee IDs, remove duplicate IDs while preserving the order of their first occurrence.

Return the list of unique IDs.

## 💡 Approach
- Use a `LinkedHashSet`:
    - Automatically removes duplicates.
    - Preserves insertion order.
- Traverse the array and add elements to the set.
- Convert the set back to an `ArrayList`.

**Why optimal?**
- Eliminates duplicates in a single pass → **O(n)**.
- Maintains order without extra logic.

## 💻 Java Code
```java
class Solution {
    public ArrayList<Integer> uniqueId(int[] arr) {
        Set<Integer> unique = new LinkedHashSet<>();
        
        for(int i : arr)
            unique.add(i);
        
        return new ArrayList<>(unique);
    }
}