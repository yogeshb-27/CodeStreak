# Contains Duplicate II 🔁

## 🔗 Problem Link
https://leetcode.com/problems/contains-duplicate-ii/description

## 📝 Problem Description
Given an integer array `nums` and an integer `k`, determine if there exist two distinct indices `i` and `j` such that:
- `nums[i] == nums[j]`
- `abs(i - j) <= k`

Return `true` if such a pair exists, otherwise return `false`.

## 💡 Approach
- Use a **Sliding Window + HashSet** to maintain at most `k` elements.
- Iterate through the array:
    - If the current element already exists in the set → duplicate within range → return `true`.
    - Add the current element to the set.
    - If the window size exceeds `k`, remove the element that goes out of range.

**Why optimal?**
- Brute force would check all pairs → `O(n^2)`.
- Using HashSet with sliding window reduces it to **O(n)** with constant-time lookups.

## 💻 Java Code
```java
class Solution {
    public boolean containsNearbyDuplicate(int[] nums, int k) {
        int n = nums.length;
        Set<Integer> set = new HashSet<>();

        for(int i = 0; i < n; i++){
            if(set.contains(nums[i]))
                return true;
            
            set.add(nums[i]);

            if(set.size() > k)
                set.remove(nums[i - k]);
        }
        return false;
    }
}