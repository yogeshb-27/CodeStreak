# 🏔 Check if an Array is Max Heap

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/does-array-represent-heap4345/1

## 📝 Problem Description
Given an array `arr[]`, determine whether it represents the level-order traversal of a valid **max heap**.

Return `true` if the array satisfies max-heap properties, otherwise return `false`.

## 💡 Approach
- In a max heap:
    - Every parent node must be greater than or equal to its children.
- For an index `i`:
    - Left child → `2*i + 1`
    - Right child → `2*i + 2`
- Traverse only till the last non-leaf node `(n-2)/2`:
    - Check if parent is smaller than any child → return `false`.

**Why optimal?**
- Only checks necessary nodes (non-leaf) → efficient.
- Single traversal ensures **O(n)** time.

## 💻 Java Code
```java
class Solution {
    public boolean isMaxHeap(int[] arr) {
        int n = arr.length;
        
        for(int i = 0; i <= (n - 2) / 2; i++){
            int left = 2 * i + 1;
            int right = 2 * i + 2;
            
            if(left < n && arr[i] < arr[left])
                return false;
            
            if(right < n && arr[i] < arr[right])
                return false;
        }
        
        return true;
    }
}