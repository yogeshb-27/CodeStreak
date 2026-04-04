# Remainder with 7 🔢

## 🔗 Problem Link
https://www.geeksforgeeks.org/problems/remainder-with-7/1

## 📝 Problem Description
Given a number represented as a string `n`, compute the remainder when the number is divided by 7.

The number can be very large, so it cannot be directly converted into an integer type.

## 💡 Approach
- Since the number can be very large, we process it digit by digit.
- Maintain a running remainder:
    - For each digit, update: `(remainder * 10 + digit) % 7`
- This avoids integer overflow and works efficiently for large inputs.

**Why optimal?**
- Direct conversion would fail for large numbers.
- This method processes the number in a single pass → **O(n)**.

## 💻 Java Code
```java
class Solution {
    int remainderWith7(String num) {
        int remainder = 0;
        
        for(int i = 0; i < num.length(); i++){
            int digit = num.charAt(i) - '0';
            remainder = (remainder * 10 + digit) % 7;
        }
        
        return remainder;
    }
}