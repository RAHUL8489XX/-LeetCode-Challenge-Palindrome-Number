## 🔗 Problem Link
Palindrome Number – LeetCode  https://leetcode.com/problems/palindrome-number/submissions/1726320732/

## 📘 Problem Description
Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.

### Constraints:
Must handle 32-bit signed integers.

Negative numbers are not palindromes.

Follow-up: Solve without converting the integer to a string.

## ✅ Solution Summary
### ✔️ Approach 1: String Reversal
python
class Solution(object):
    def isPalindrome(self, x):
        if x < 0:
            return False
        return str(x) == str(x)[::-1]
Time Complexity: O(n) — where n is the number of digits.

Memory Usage: 12.37 MB (Beats 81.24%)

Runtime: 8 ms (Beats 69.76%)

### ✔️ Approach 2: Mathematical Reversal (No Strings)
python
class Solution(object):
    def isPalindrome(self, x):
        if x < 0:
            return False
        original = x
        reversed_num = 0
        while x != 0:
            reversed_num = reversed_num * 10 + x % 10
            x //= 10
        return original == reversed_num
Avoids string conversion.

Handles edge cases like trailing zeros and negatives.

## 🧪 Test Cases

| Input | Output | Explanation                          |
|-------|--------|--------------------------------------|
| 121   | True   | Reads same forward and backward      |
| -121  | False  | Negative sign breaks symmetry        |
| 10    | False  | Reversed is 01                       |
| 0     | True   | Single-digit palindromes are valid   |



## 🧠 Notes
Negative numbers are automatically excluded.

Trailing zeros (e.g., 100) are not palindromes.

Efficient for both small and large integers.

## 🏁 Submission Stats
✅ 11511 / 11511 test cases passed

⏱️ Time taken: 21 minutes 11 seconds

📈 Performance: Top 30% in runtime, top 20% in memory usage
