# 📊 Min and Max in Array

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1

## 📝 Problem Description
Given an array `arr[]`, find and return both the minimum and maximum elements in the array.

Return the result as a list `[min, max]`.

## 💡 Approach
- Initialize two variables:
    - `min` with `Integer.MAX_VALUE`
    - `max` with `Integer.MIN_VALUE`
- Traverse the array:
    - Update `min` using `Math.min()`
    - Update `max` using `Math.max()`
- Return both values as a list.

**Why optimal?**
- Single traversal ensures **O(n)** time.
- No extra space used apart from variables → **O(1)**.

## 💻 Java Code
```java
class Solution {
    public ArrayList<Integer> getMinMax(int[] arr) {
        int min = Integer.MAX_VALUE, max = Integer.MIN_VALUE;
        
        for(int i : arr){
            min = Math.min(min, i);
            max = Math.max(max, i);
        }
        
        return new ArrayList<Integer>(Arrays.asList(min, max));
    }
}