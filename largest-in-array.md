# 📈 Largest in Array

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/largest-element-in-array4009/1

## 📝 Problem Description
Given an array `arr[]`, find and return the largest element present in the array.

## 💡 Approach
- Initialize a variable `max` with the smallest possible integer.
- Traverse the array:
    - Compare each element with `max`.
    - Update `max` if a larger element is found.
- Return the final value of `max`.

**Why optimal?**
- Only one pass through the array → **O(n)** time.
- No extra space used → **O(1)**.

## 💻 Java Code
```java
class Solution {
    public static int largest(int[] arr) {
        int max = Integer.MIN_VALUE;
        
        for(int x : arr){
            max = Math.max(x, max);
        }
        
        return max;
    }
}