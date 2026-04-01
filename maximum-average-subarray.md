# Maximum Average Subarray I 🚀

## 🔗 Problem Link
https://leetcode.com/problems/maximum-average-subarray-i/description/

## 📝 Problem Description
Given an integer array `nums` and an integer `k`, find the contiguous subarray of length `k` that has the maximum average value. Return this maximum average.

The answer will be accepted if the error is within `10^-5`.

## 💡 Approach
- Instead of recalculating the sum of every subarray of size `k`, we use a **Sliding Window** approach.
- First, calculate the sum of the first `k` elements.
- Then, slide the window one step at a time:
    - Add the next element
    - Remove the element leaving the window
- Keep track of the maximum sum found.

**Why optimal?**
- Brute force would take `O(n * k)` time.
- Sliding Window reduces it to **O(n)** by avoiding repeated calculations.

## 💻 Java Code
```java
class Solution {
    public double findMaxAverage(int[] nums, int k) {
        int sum = 0;

        for(int i = 0; i < k; i++)
            sum += nums[i];
        
        int maxSum = sum;

        for(int i = k; i < nums.length; i++){
            sum += nums[i];
            sum -= nums[i - k];
            maxSum = Math.max(sum, maxSum);
        }

        return (double) maxSum / k;
    }
}